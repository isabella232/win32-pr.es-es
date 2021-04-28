---
description: 'Método ProtectKeyWithCertificateFile de la clase Win32_EncryptableVolume : valida el identificador de objeto (OID) uso mejorado de clave (EKU) del certificado proporcionado.'
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Método ProtectKeyWithCertificateFile de la Win32_EncryptableVolume clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110572"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithCertificateFile de la clase EncryptableVolume de Win32 \_

El **método ProtectKeyWithCertificateFile** de la clase [**\_ EncryptableVolume de Win32**](win32-encryptablevolume.md) valida el identificador de objeto (EKU) uso mejorado de clave (EKU) del certificado proporcionado. [](../secgloss/o-gly.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FriendlyName* \[ en, opcional\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica un identificador de cadena asignado por el usuario para este protector de clave. Si no se especifica este parámetro, el *parámetro FriendlyName* se crea mediante el nombre del sujeto en el certificado.

</dd> <dt>

*FileName* \[ En\]
</dt> <dd>

Tipo: **cadena**

Cadena que especifica la ubicación y el nombre del archivo .cer usado para habilitar BitLocker. Un certificado de cifrado debe exportarse en formato .cer ([*reglas de codificación distinguida*](../secgloss/d-gly.md) (DER) binario codificado [*X.509*](../secgloss/x-gly.md) o X.509 codificado en Base-64). El certificado de cifrado se puede generar a partir de PKI de Microsoft, PKI de terceros o autofirmado.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: **cadena**

Cadena que identifica de forma única el protector de clave creado que se puede usar para administrar este protector de clave.

Si la unidad admite el cifrado de hardware y BitLocker no ha tomado posesión de la banda, la cadena de identificador se establece en "BitLocker" y el protector de clave se escribe en los metadatos por banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los códigos siguientes u otro código de error si se produce un error.



| Código o valor devuelto                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl>                                                           | Método realizado correctamente.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ NON \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | El atributo EKU del certificado especificado no permite que se utilice para Cifrado de unidad BitLocker. BitLocker no requiere que un certificado tenga un atributo EKU, pero si uno está configurado, debe establecerse en un OID que coincida con el OID configurado para BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT \_ \_ \_ \_ ALLOWED**</dt> <dt>2150695026 (0X80310072)</dt> </dl> | directiva de grupo no permite que los certificados de usuario, como las tarjetas inteligentes, se utilicen con BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERT DEBE SER \_ \_ \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | directiva de grupo requiere que proporcione una tarjeta inteligente para usar BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ E \_ POLICY PROHÍBE LA FIRMA \_ \_ PROPIA**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | directiva de grupo no permite el uso de certificados autofirmados.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERROR \_ ARCHIVO \_ NO \_ ENCONTRADO**</dt> <dt>0000000002 (0x2)</dt> </dl>                                | El sistema no puede encontrar el archivo especificado.<br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentarios

Si el OID no coincide con el asociado al controlador de servicio en el Registro, se produce un error en este método. Esto evita que el usuario ajuste los protectores del agente de recuperación de datos (DRA) manualmente en el volumen. Los DRA solo los establecerá el servicio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 Enterprise, Windows 7 \[ Ultimate\]<br/>                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
