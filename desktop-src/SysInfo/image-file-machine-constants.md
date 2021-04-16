---
description: Describe las posibles arquitecturas de máquina.
ms.assetid: 1E5E4F98-925B-424D-9B3D-BC6716FBF990
title: Constantes del equipo de archivos de imagen (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c43767ce0d86edf2285241772ea060573efc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542670"
---
# <a name="image-file-machine-constants"></a>Constantes del equipo de archivos de imagen

Describe las posibles arquitecturas de máquina. Se usa en [**GetSystemWow64Directory2**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directory2a), [**IsWow64GuestMachineSupported**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64guestmachinesupported) y [**IsWow64Process2**](/windows/win32/api/wow64apiset/nf-wow64apiset-iswow64process2).

<dl> <dt>

<span id="IMAGE_FILE_MACHINE_UNKNOWN"></span><span id="image_file_machine_unknown"></span>**máquina de archivo de imagen \_ \_ \_ desconocida**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Unknown


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TARGET_HOST"></span><span id="image_file_machine_target_host"></span>**\_host de \_ destino del equipo de archivos de imagen \_ \_**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Interactúa con el host y no con un invitado WOW64

> [!Note]  
> Esta constante está disponible a partir de Windows 10, la versión 1607 y Windows Server 2016.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_I386"></span><span id="image_file_machine_i386"></span>**Máquina de archivos de imagen \_ \_ \_ i386**
</dt> <dd> <dl> <dt>

0x014c
</dt> <dt>



Intel 386


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R3000"></span><span id="image_file_machine_r3000"></span>**Máquina de archivos de imagen \_ \_ \_ R3000**
</dt> <dd> <dl> <dt>

0x0162
</dt> <dt>



Little-Endian de MIPS, 0x160 Big-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R4000"></span><span id="image_file_machine_r4000"></span>**Máquina de archivos de imagen \_ \_ \_ R4000**
</dt> <dd> <dl> <dt>

0x0166
</dt> <dt>



Little-Endian de MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_R10000"></span><span id="image_file_machine_r10000"></span>**Máquina de archivos de imagen \_ \_ \_ R10000**
</dt> <dd> <dl> <dt>

0x0168
</dt> <dt>



Little-Endian de MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_WCEMIPSV2"></span><span id="image_file_machine_wcemipsv2"></span>**Máquina de archivos de imagen \_ \_ \_ WCEMIPSV2**
</dt> <dd> <dl> <dt>

0x0169
</dt> <dt>



MIPS Little-endian, WCE V2


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA"></span><span id="image_file_machine_alpha"></span>**\_alfa del \_ equipo de archivos de imagen \_**
</dt> <dd> <dl> <dt>

0x0184
</dt> <dt>



Alpha \_ AXP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3"></span><span id="image_file_machine_sh3"></span>**Máquina de archivos de imagen \_ \_ \_ SH3**
</dt> <dd> <dl> <dt>

0x01a2
</dt> <dt>



SH3 Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3DSP"></span><span id="image_file_machine_sh3dsp"></span>**Máquina de archivos de imagen \_ \_ \_ SH3DSP**
</dt> <dd> <dl> <dt>

0x01a3
</dt> <dt>



SH3DSP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH3E"></span><span id="image_file_machine_sh3e"></span>**Máquina de archivos de imagen \_ \_ \_ SH3E**
</dt> <dd> <dl> <dt>

0x01a4
</dt> <dt>



SH3E Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH4"></span><span id="image_file_machine_sh4"></span>**Máquina de archivos de imagen \_ \_ \_ SH4**
</dt> <dd> <dl> <dt>

0x01a6
</dt> <dt>



SH4 Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_SH5"></span><span id="image_file_machine_sh5"></span>**Máquina de archivos de imagen \_ \_ \_ SH5**
</dt> <dd> <dl> <dt>

0x01a8
</dt> <dt>



SH5


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM"></span><span id="image_file_machine_arm"></span>**\_ARM del \_ equipo de archivos de imagen \_**
</dt> <dd> <dl> <dt>

0x01c0
</dt> <dt>



Little-Endian ARM


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_THUMB"></span><span id="image_file_machine_thumb"></span>**\_control de \_ equipo de archivo de imagen \_**
</dt> <dd> <dl> <dt>

0x01c2
</dt> <dt>



Thumb Thumb/Thumb-2 Little-Endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARMNT"></span><span id="image_file_machine_armnt"></span>**máquina de archivos de imagen \_ \_ \_ ARMNT**
</dt> <dd> <dl> <dt>

0x01c4
</dt> <dt>



Control de ARM: 2 Little-Endian

> [!Note]  
> Esta constante está disponible a partir de Windows 7 y Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AM33"></span><span id="image_file_machine_am33"></span>**Máquina de archivos de imagen \_ \_ \_ AM33**
</dt> <dd> <dl> <dt>

0x01d3
</dt> <dt>



TAM33BD


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPC"></span><span id="image_file_machine_powerpc"></span>**máquina de archivos de imagen \_ \_ \_ POWERPC**
</dt> <dd> <dl> <dt>

0x01F0
</dt> <dt>



Little-Endian de IBM PowerPC


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_POWERPCFP"></span><span id="image_file_machine_powerpcfp"></span>**máquina de archivos de imagen \_ \_ \_ POWERPCFP**
</dt> <dd> <dl> <dt>

0x01f1
</dt> <dt>



POWERPCFP


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_IA64"></span><span id="image_file_machine_ia64"></span>**Máquina de archivos de imagen \_ \_ \_ ia64**
</dt> <dd> <dl> <dt>

0x0200
</dt> <dt>



Intel 64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPS16"></span><span id="image_file_machine_mips16"></span>**Máquina de archivos de imagen \_ \_ \_ MIPS16**
</dt> <dd> <dl> <dt>

0x0266
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ALPHA64"></span><span id="image_file_machine_alpha64"></span>**Máquina de archivos de imagen \_ \_ \_ ALPHA64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



ALPHA64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU"></span><span id="image_file_machine_mipsfpu"></span>**máquina de archivos de imagen \_ \_ \_ MIPSFPU**
</dt> <dd> <dl> <dt>

0x0366
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_MIPSFPU16"></span><span id="image_file_machine_mipsfpu16"></span>**Máquina de archivos de imagen \_ \_ \_ MIPSFPU16**
</dt> <dd> <dl> <dt>

0x0466
</dt> <dt>



MIPS


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AXP64"></span><span id="image_file_machine_axp64"></span>**Máquina de archivos de imagen \_ \_ \_ AXP64**
</dt> <dd> <dl> <dt>

0x0284
</dt> <dt>



AXP64


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_TRICORE"></span><span id="image_file_machine_tricore"></span>**máquina de archivos de imagen de \_ \_ \_ trinúcleo**
</dt> <dd> <dl> <dt>

0x0520
</dt> <dt>



Infineon


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEF"></span><span id="image_file_machine_cef"></span>**máquina de archivos de imagen \_ \_ \_ CEF**
</dt> <dd> <dl> <dt>

0x0CEF
</dt> <dt>



CEF


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_EBC"></span><span id="image_file_machine_ebc"></span>**archivo de imagen del \_ \_ sistema \_ EBC**
</dt> <dd> <dl> <dt>

0x0EBC
</dt> <dt>



Código de byte EFI


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_AMD64"></span><span id="image_file_machine_amd64"></span>**Máquina de archivos de imagen \_ \_ \_ AMD64**
</dt> <dd> <dl> <dt>

0x8664
</dt> <dt>



AMD64 (K8)


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_M32R"></span><span id="image_file_machine_m32r"></span>**Máquina de archivos de imagen \_ \_ \_ M32R**
</dt> <dd> <dl> <dt>

0x9041
</dt> <dt>



M32R Little-endian


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_ARM64"></span><span id="image_file_machine_arm64"></span>**Máquina de archivos de imagen \_ \_ \_ ARM64**
</dt> <dd> <dl> <dt>

0xAA64
</dt> <dt>



Little-Endian ARM64

> [!Note]  
> Esta constante está disponible a partir de Windows 8.1 y Windows Server 2012 R2.

 


</dt> </dl> </dd> <dt>

<span id="IMAGE_FILE_MACHINE_CEE"></span><span id="image_file_machine_cee"></span>**máquina del archivo de imagen \_ \_ \_ CEE**
</dt> <dd> <dl> <dt>

0xC0EE
</dt> <dt>



CEE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




