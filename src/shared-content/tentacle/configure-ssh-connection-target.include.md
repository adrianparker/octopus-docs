1. In the **Octopus Web Portal**, navigate to the **Infrastructure** tab, select **Deployment Targets** and click **ADD DEPLOYMENT TARGET**.
2. Choose either **LINUX** or **MAC** and click **ADD** on the SSH Connection card.
3. Enter the DNS or IP address of the deployment target, i.e., `example.com` or `10.0.1.23`.
4. Enter the port (port 22 by default) and click **NEXT**.

Make sure the target server is accessible by the port you specify.

The Octopus Server will attempt to perform the required protocol handshakes and obtain the remote endpoint's public key fingerprint automatically rather than have you enter it manually. This fingerprint is stored and verified by the server on all subsequent connections.

If this discovery process is not successful, you will need to click **ENTER DETAILS MANUALLY**.

5. Give the target a name.
6. Select which environment the deployment target will be assigned to.
7. Choose or create at least one target role for the deployment target and click **Save**. Learn about [target tags](/docs/infrastructure/deployment-targets/target-tags).
8. Select the account that will be used for the Octopus Server and the SSH target to communicate.
9. If entering the details manually, enter the **Host**, **Port** and the host's fingerprint.

:::div{.hint}
From Octopus Server **2024.2.6856** both SHA256 and MD5 fingerprints are supported. We recommend using SHA256 fingerprints.
:::

You can retrieve the fingerprint of the default key configured in your sshd\_config file from the target server with the following command:

```bash
ssh-keygen -E sha256 -lf /etc/ssh/ssh_host_ed25519_key.pub | awk '{ print $2 }'
```

For Octopus Server prior to **2024.2.6856** use the following:

```bash
ssh-keygen -E md5 -lf /etc/ssh/ssh_host_ed25519_key.pub | awk '{ print $2 }' | cut -d':' -f2-
```

10. Select the **Platform** (OS and architecture) of the target server.

11. Click **Save**.