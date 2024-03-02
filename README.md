Template for Magento Open Source and Platform.sh

1. `platform get <project_id>`
2. `cd <project directory>`
3. Download this template into the new project directory.
```
wget https://github.com/wagento/platform.sh-magento-template/archive/refs/heads/main.zip && \
unzip main.zip && \
rm main.zip && \
rsync -r platform.sh-magento-template-main/ . && \
rm -rf platform.sh-magento-template-main
```
4. Provide Magento product key in auth.json
5. `platform push`

Login to the environment and configure Varnish

6. `platform ssh`
7. `bin/magento config:set --lock-env system/full_page_cache/caching_application 2`
