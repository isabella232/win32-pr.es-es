---
description: Realiza una copia de seguridad de los datos de recuperación en Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Método BackupRecoveryInformationToActiveDirectory de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688666"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>Método BackupRecoveryInformationToActiveDirectory de la \_ clase EncryptableVolume de Win32

El método **BackupRecoveryInformationToActiveDirectory** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) realiza copias de seguridad de los datos de recuperación en Active Directory. Este método requiere que haya un protector de contraseña numérica en el volumen. También se debe configurar directiva de grupo para habilitar la copia de seguridad de la información de recuperación en Active Directory.

## <a name="syntax"></a>Sintaxis


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ de\]
</dt> <dd>

Tipo: **String**

Un identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado. Este protector de clave debe ser un protector de contraseña numérica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                    |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                                         | Directiva de grupo no permite el almacenamiento de la información de recuperación en Active Directory.<br/>                         |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                             |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protector**</dt> <dt>2150694970 (0x8031003A)</dt> no válido </dl> | El protector de clave especificado no es un protector de clave numérico. Debe especificar un protector de contraseña numérica. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




