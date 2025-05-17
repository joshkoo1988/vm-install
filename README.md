# ProxMox VM Install Guide

## Description
A full guide on installing a VM in the ProxMox environment.

---

## Program Walk-through

1. **Log into your ProxMox homepage.**

2. **Download an ISO file** from a trusted source *or* upload an existing ISO file from your own computer.

   - **If downloading an ISO file**:
     - Click on the **ProxMox node** in the left sidebar.
     - Navigate to `local` → `ISO Images`.
     - Click **Download from URL**, then provide the ISO link.

   - **If uploading an existing ISO file**:
     - Navigate to `local` → `ISO Images`.
     - Click **Upload**, then choose your ISO from your machine.

   - **Having issues with unsupported format types or disk volumes?**
     - Click the link below to learn more about supported storage types and volume configuration:
     - [ProxMox Post-Install Storage Guide](https://github.com/joshkoo1988/ProxMox-postinstall)

3. **Click "Create VM"** on the top-right corner of the ProxMox dashboard.

4. **Follow the prompts** and adjust settings according to your usage needs. Here's a breakdown of the key pages:

   - **Page 1 – General**:
     - Name your VM.
     - Set the VM ID (optional, auto-filled).

   - **Page 2 – OS**:
     - Select the ISO image you uploaded/downloaded.
     - Choose the appropriate guest OS type.

   - **Page 3 – System**:
     - Set BIOS (typically `OVMF` for UEFI or `SeaBIOS` for legacy).
     - Configure SCSI controller and display options.

   - **Page 4 – Hard Disk**:
     - Select storage type (e.g., `local-lvm`).
     - Set disk size according to your needs.

   - **Page 5 – CPU**:
     - Assign number of cores.
     - (Optional) Enable CPU type emulation.

   - **Page 6 – Memory**:
     - Allocate RAM.
     - Optionally set minimum and maximum memory for ballooning.

   - **Page 7 – Network**:
     - Attach to a virtual bridge (e.g., `vmbr0`).
     - Set model type (e.g., `VirtIO` or `E1000`).

5. **Click "Finish"** to create the VM.

6. **Start the VM** and begin the OS installation process.

7. **Spin up more VMs** using the same steps as needed.


