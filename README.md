This guide helps you download `main.py` and configure it within Marzban.

## Steps

1. **Download `main.py`**  
   Download `main.py` from the repository to your Marzban directory:

   ```bash
   sudo wget -P /opt/marzban/ https://github.com/erfjab/notforced/blob/master/main.py
   ```

2. **Edit `docker-compose.yml`**  
   Open your `docker-compose.yml` file in the editor:

   ```bash
   nano /opt/marzban/docker-compose.yml
   ```

3. **Add Volume Configuration**  
   In the `volumes` section, add the following lines to link `main.py`:

   ```yaml
   volumes:
     - /var/lib/marzban:/var/lib/marzban   
     - /opt/marzban/main.py:/code/main.py
   ```

4. **Restart Marzban**  
   To apply changes, restart Marzban:

   ```bash
   marzban restart
   ```

All done! Marzban is now configured with the `main.py` file.