---
description: Usa el archivo de certificado proporcionado para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Método UnlockWithCertificateFile de la clase Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668472"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateFile de la \_ clase EncryptableVolume de Win32

El método **UnlockWithCertificateFile** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa el archivo de [*certificado*](../secgloss/c-gly.md) proporcionado para obtener la clave derivada y desbloquear el volumen cifrado.

> [!Note]  
> Si el disco es compatible con el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado" "

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de archivo* \[ de\]
</dt> <dd>

Tipo: **String**

Una cadena que especifica la ubicación y el nombre del archivo. cer que se usa para recuperar la huella digital del certificado. Se debe exportar un certificado de [*cifrado*](../secgloss/e-gly.md) en formato. cer ([*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) binario codificado [*x. 509*](../secgloss/x-gly.md) o x. 509 codificado en base-64). El certificado de cifrado se puede generar a partir de PKI de Microsoft, PKI de terceros o autofirmado.

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
| <dl> <dt>**Error \_ de \_No \_ se encontró el archivo**</dt> <dt>0000000002 (0X2)</dt> </dl>                 | El sistema no puede archivar el archivo especificado.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ no \_ activada**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ error de \_ autenticación**</dt> <dt>2150694951 (0x80310027)</dt> </dl>   | No se puede desbloquear el volumen con la información proporcionada. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ \_ \_ No \_ se encontró el protector E**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen. Debe especificar otro protector de clave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ Error de E \_ PRIVATEKEY \_ auth \_**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | No se pudo autorizar la [*clave privada*](../secgloss/p-gly.md)asociada con el certificado especificado. No se proporcionó la autorización de la clave privada o la autorización proporcionada no era válida.<br/> |



 

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

 

 
