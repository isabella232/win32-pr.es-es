---
description: Habilita o reanuda todos los protectores de clave deshabilitados o suspendidos.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Método EnableKeyProtectors de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d90e37f800a9c224abefb21253f7e74c2bc08401
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253431"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método EnableKeyProtectors de la clase EncryptableVolume de Win32 \_

El **método EnableKeyProtectors** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) habilita o reanuda todos los protectores de clave deshabilitados o suspendidos. Puede usar este método para volver a habilitar o reanudar la protección de BitLocker en un volumen cifrado. Este método garantiza que la clave de cifrado del volumen no se expone sin cifrar en el disco duro.

> [!Note]  
> Si el disco admite el cifrado de hardware, el estado de la banda pasa a "desbloqueado" desde "siempre desbloqueado".

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.

Si los protectores de clave ya están habilitados y no se producen otros errores, este método devuelve cero.




| Código o valor devuelto | Descripción | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | Método realizado correctamente.<br /> | 
| <dl><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt><dt>2150694919 (0x80310007)</dt></dl> | No existen protectores de clave en el volumen. Use uno de los métodos siguientes para especificar protectores de clave para el volumen:<br /><ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul> | 
| <dl><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt><dt>2150694920 (0x80310008)</dt></dl> | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br /> | 




 

## <a name="remarks"></a>Observaciones

Si el volumen está totalmente cifrado, la ejecución correcta de este método garantiza que el volumen está protegido. Si el volumen está cifrado parcialmente, ejecutar correctamente este método implica que el volumen se protegerá cuando se cifra completamente. Para obtener más información, vea el [**método GetProtectionStatus.**](getprotectionstatus-win32-encryptablevolume.md)

Si existen protectores de clave basados en TPM para el volumen, la ejecución correcta de este método también actualiza estos protectores para que el TPM se valide con los servicios de inicio actuales de la plataforma. En otras palabras, está afirmando que el estado actual del equipo es el correcto que el TPM comprobará en futuros reinicios del equipo.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista Enterprise, Windows solo aplicaciones de escritorio de Vista Ultimate \[\]<br/>                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> <dt>

[**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
