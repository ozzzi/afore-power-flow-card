# Solarman integration

1. Obtaining Wi-Fi data logger IP address

- MacOs, Linux: `nmap 192.168.1.0/24`
- Windows: any IP scanner software
- Python: [https://pysolarmanv5.readthedocs.io/en/stable/utilities.html](https://pysolarmanv5.readthedocs.io/en/stable/utilities.html)

2. On your router (DHCP settings), reserve the IP for the Wi-Fi data logger so that it will not change.

3. Get S/N of your Wi-Fi data logger
- from Solarman 
- or from data logger web page (IP data logger). User/pass: `admin/admin`

4. Install Solaram by HACS

[https://github.com/StephanJoubert/home_assistant_solarman](https://github.com/StephanJoubert/home_assistant_solarman)

5. Config Solaramn for V1.5.1 (or old)

Create file: `/config/custom_components/solarman/inverter_definitions/afore.yaml` with content: [https://github.com/ozzzi/afore-power-flow-card/blob/main/afore.yaml](https://github.com/ozzzi/afore-power-flow-card/blob/main/afore.yaml)

Change file: `/config/custom_components/solarman/const.py`

```
LOOKUP_FILES = [
    'afore.yaml',
    'deye_2mppt.yaml',
    ...
```

6. Install dashboard card

Afore Power Card: [https://github.com/ozzzi/afore-power-flow-card](https://github.com/ozzzi/afore-power-flow-card)
