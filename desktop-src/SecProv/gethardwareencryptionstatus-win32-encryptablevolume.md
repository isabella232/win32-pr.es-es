---
description: Determina si el volumen se encuentra en una unidad que admite o puede admitir el cifrado de hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Método GetHardwareEncryptionStatus de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 434c074260a07a251ac81148616c434cb9f7de74d799a42c71bd81451a1bd3b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668005"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetHardwareEncryptionStatus de la clase EncryptableVolume de Win32 \_

El **método GetHardwareEncryptionStatus** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) determina si el volumen se encuentra en una unidad que admite o puede admitir el cifrado de hardware.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HardwareEncryptionStatus* \[ out\]
</dt> <dd>

Especifica si la unidad puede admitir el cifrado de hardware. Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                               | Significado                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**No compatible con**</dt> <dt>0</dt> </dl> | No se admite el cifrado de hardware.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Sin protección**</dt> <dt>1</dt> </dl> | No se admite el cifrado de unidades.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Usa software**</dt> <dt>2</dt> </dl> | El método de cifrado está basado en software.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Usa hardware**</dt> <dt>3</dt> </dl> | La unidad admite el cifrado de hardware.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función devuelve cero (0) si el volumen es compatible con el cifrado de hardware de BitLocker. De lo contrario, la función devuelve un error.



| Código o valor devuelto                                                                                                                                 | Descripción                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | El volumen es compatible con el cifrado de hardware de BitLocker.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 Enterprise, solo Windows 8 Pro \[ aplicaciones de escritorio\]<br/>                                    |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




