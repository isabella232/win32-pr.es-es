---
description: Copia de seguridad de los datos de recuperación en Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Método BackupRecoveryInformationToActiveDirectory de la Win32_EncryptableVolume clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265252"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a>Método BackupRecoveryInformationToActiveDirectory de la clase EncryptableVolume de Win32 \_

El **método BackupRecoveryInformationToActiveDirectory** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) hace una copia de seguridad de los datos de recuperación en Active Directory. Este método requiere que un protector numérico de contraseña esté presente en el volumen. directiva de grupo debe configurarse para habilitar la copia de seguridad de la información de recuperación en Active Directory.

## <a name="syntax"></a>Sintaxis


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*VolumeKeyProtectorID* \[ En\]
</dt> <dd>

Tipo: **cadena**

Identificador de cadena único que se usa para administrar un protector de clave de volumen cifrado. Este protector de clave debe ser un protector numérico de contraseña.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                    |
| <dl> <dt>**S \_ FALSE**</dt> <dt>1 (0x1)</dt> </dl>                                         | directiva de grupo no permite que el almacenamiento de información de recuperación Active Directory.<br/>                         |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                             |
| <dl> <dt>**FVE \_ E \_ TIPO DE PROTECTOR \_ \_ NO**</dt> <dt>VÁLIDO 2150694970 (0x8031003A)</dt> </dl> | El protector de clave especificado no es un protector numérico de clave. Debe escribir un protector numérico de contraseña. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




