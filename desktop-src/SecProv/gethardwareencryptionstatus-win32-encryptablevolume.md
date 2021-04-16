---
description: Determina si el volumen se encuentra en una unidad que admite o puede admitir el cifrado de hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Método GetHardwareEncryptionStatus de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686652"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetHardwareEncryptionStatus de la \_ clase EncryptableVolume de Win32

El método **GetHardwareEncryptionStatus** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) determina si el volumen se encuentra en una unidad que admita o admita el cifrado de hardware.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HardwareEncryptionStatus* \[ enuncia\]
</dt> <dd>

Especifica si la unidad puede admitir el cifrado de hardware. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                               | Significado                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**No compatible**</dt> <dt>0</dt> </dl> | No se admite el cifrado de hardware.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Sin protección**</dt> <dt>1</dt> </dl> | No se admite el cifrado de unidad.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Utiliza el software**</dt> <dt>2</dt> </dl> | El método de cifrado está basado en software.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Usa hardware**</dt> <dt>3</dt> </dl> | La unidad admite el cifrado de hardware.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve cero (0) si el volumen es compatible con el cifrado de hardware de BitLocker. De lo contrario, la función devuelve un error.



| Código o valor devuelto                                                                                                                                 | Descripción                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | El volumen es compatible con el cifrado de hardware de BitLocker.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]<br/>                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




