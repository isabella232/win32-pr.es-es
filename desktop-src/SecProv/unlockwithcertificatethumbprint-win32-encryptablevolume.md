---
description: Usa la huella digital del certificado proporcionada para obtener la clave derivada y desbloquear el volumen cifrado.
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Método UnlockWithCertificateThumbprint de la Win32_EncryptableVolume clase
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
ms.openlocfilehash: 0ccf4a68f999bee1d32d8025759eb9625371b18fc5028b54e68e62df544bbd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891371"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithCertificateThumbprint de la clase EncryptableVolume de Win32 \_

El **método UnlockWithCertificateThumbprint** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) usa la huella digital del certificado proporcionada para obtener la clave derivada y desbloquear el volumen cifrado. [](../secgloss/c-gly.md)

> [!Note]  
> Si el disco admite el cifrado de hardware, esta función establece el estado de la banda en "desbloqueado""

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CertThumbprint* \[ En\]
</dt> <dd>

Tipo: **cadena**

Se acepta un valor de huella digital de 0 y se produce una búsqueda en el almacén local para el certificado adecuado. Si se encuentra un único certificado de BitLocker, la búsqueda se realiza correctamente. Si no se encuentra ninguno o más de un certificado, se produce un error en el método .

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
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | BitLocker no está habilitado en el volumen. Agregue un protector de clave para habilitar BitLocker. <br/>                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ ERROR \_ DE AUTENTICACIÓN**</dt> 2150694951 <dt>(0x80310027)</dt> </dl>   | El volumen no se puede desbloquear mediante la información proporcionada. <br/>                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ PROTECTOR \_ NO \_ ENCONTRADO**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | El protector de clave proporcionado no existe en el volumen. Debe escribir otro protector de clave.<br/>                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ PRIVATEKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt> </dl> | No [*se pudo*](../secgloss/p-gly.md) autorizar la clave privada asociada al certificado especificado. No se proporcionó la autorización de clave privada o la autorización proporcionada no era válida.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise, Windows 7 aplicaciones de \[ escritorio Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
