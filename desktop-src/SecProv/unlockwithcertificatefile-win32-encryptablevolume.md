---
description: Usa el archivo de certificado proporcionado para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Método UnlockWithCertificateFile de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 576de5820e5b16b59a0b77659a4833a261ecd9ef8445306ce3d6f320c664f833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004233"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateFile de la clase EncryptableVolume de Win32 \_

El **método UnlockWithCertificateFile** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa el archivo de certificado proporcionado para obtener la clave derivada y desbloquear el volumen cifrado. [](../secgloss/c-gly.md)

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FileName* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la ubicación y el nombre del archivo .cer usado para recuperar la huella digital del certificado. Un [*certificado*](../secgloss/e-gly.md) de cifrado debe exportarse en formato .cer [*(reglas de codificación distinguida*](../secgloss/d-gly.md) (DER) binario codificado [*X.509*](../secgloss/x-gly.md) o X.509 codificado en Base-64). El certificado de cifrado se puede generar a partir de PKI de Microsoft, PKI de terceros o autofirmado.

</dd> <dt>

*PIN* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena de identificación personal especificada por el usuario. Esta cadena debe constar de una secuencia de 4 a 20 dígitos. Esta cadena se usa para autenticar de forma silenciosa el proveedor [*de almacenamiento de*](../secgloss/k-gly.md) claves (KSP) cuando se usa con una tarjeta [*inteligente*](../secgloss/s-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                            | Descripción                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                            | Método realizado correctamente.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**ERROR \_ ARCHIVO \_ NO \_ ENCONTRADO**</dt> <dt>0000000002 (0x2)</dt> </dl>                 | El sistema no puede presentar el archivo especificado.<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ ERROR \_ DE AUTENTICACIÓN**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>   | El volumen no se puede desbloquear con la información proporcionada. <br/>                                                                                                                                                                                                 |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NO \_ ENCONTRADO**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen. Debe escribir otro protector de clave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | No [*se pudo*](../secgloss/p-gly.md)autorizar la clave privada asociada al certificado especificado. No se proporcionó la autorización de clave privada o la autorización proporcionada no era válida.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
