---
description: Usa la huella digital de certificado proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Método UnlockWithCertificateThumbprint de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809271"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateThumbprint de la \_ clase EncryptableVolume de Win32

El método **UnlockWithCertificateThumbprint** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la huella digital de [*certificado*](../secgloss/c-gly.md) proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CertThumbprint* \[ de\]
</dt> <dd>

Tipo: **String**

Se acepta un valor de huella digital de 0 y se produce una búsqueda del certificado adecuado en el almacén local. Si se encuentra un solo certificado de BitLocker, la búsqueda se realizará correctamente. Si no se encuentra ninguno o más de un certificado, se produce un error en el método.

</dd> <dt>

*Código PIN* \[ de\]
</dt> <dd>

Tipo: **String**

Cadena de identificación personal especificada por el usuario. Esta cadena debe estar formada por una secuencia de 4 a 20 dígitos. Esta cadena se usa para autenticar de forma silenciosa el [*proveedor de almacenamiento de claves*](../secgloss/k-gly.md) (KSP) cuando se usa con una [*tarjeta inteligente*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | No se puede desbloquear el volumen con la información proporcionada. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen. Debe especificar otro protector de clave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ Error de E \_ PRIVATEKEY \_ auth \_**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | No se pudo autorizar la [*clave privada*](../secgloss/p-gly.md) asociada al certificado especificado. No se proporcionó la autorización de clave privada o la autorización proporcionada no era válida.<br/> |



 

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

 

 
