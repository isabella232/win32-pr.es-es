---
description: Determina si las firmas de los datos firmados en el objeto SignedData son válidas.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: SignedData. verify (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3cb48943a826296c13df80130171442fc29435f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670503"
---
# <a name="signeddataverify-method"></a>SignedData. verify (método)

\[El método **Verify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Verify** determina si las [*firmas*](../secgloss/d-gly.md) de los datos firmados en el objeto [**SignedData**](signeddata.md) son válidas. Para comprobar una firma, el [*hash*](../secgloss/h-gly.md) cifrado del contenido se descifra mediante la clave pública del firmante del certificado del firmante. El hash descifrado se compara con un nuevo hash del contenido de los datos. Una firma es válida si los valores hash coinciden. Además, este método también crea una cadena de certificados para determinar la validez del certificado que proporciona la [*clave pública*](../secgloss/p-gly.md) utilizada para descifrar el hash.

## <a name="syntax"></a>Sintaxis


```VB
SignedData.Verify( _
  ByVal SignedMessage, _
  [ ByVal bDetached ], _
  [ ByVal VerifyFlag ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SignedMessage* \[ de\]
</dt> <dd>

Cadena que contiene el mensaje firmado que se va a comprobar.

</dd> <dt>

*bDetached* \[ en, opcional\]
</dt> <dd>

Si es **true**, se desasocian los datos que se van a firmar; es decir, el contenido que está firmado no se incluye como parte del objeto firmado. Para comprobar la firma en el contenido separado, una aplicación debe tener una copia del contenido original. El contenido separado se usa a menudo para reducir el tamaño de un objeto firmado que se va a enviar a través de la web, si el destinatario del mensaje firmado tiene una copia original de los datos firmados. El valor predeterminado es **False**.

</dd> <dt>

*VerifyFlag* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de la marca de comprobación de [ \_ \_ datos \_ \_ firmados de CAPICOM](capicom-signed-data-verify-flag.md) que indica la Directiva de comprobación. El valor predeterminado es CAPICOM \_ Verify \_ Signature \_ and \_ Certificate. Con este valor, se comprueba la validez del certificado y la validez de la firma. Este parámetro se puede establecer para comprobar la firma y no el certificado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                             | Significado                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**CAPICOM \_ comprobar \_ solo la firma \_**</dt> </dl>                                   | Solo se comprueba la firma.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**CAPICOM \_ comprobar la \_ firma \_ y el \_ certificado**</dt> </dl> | Se comprueban tanto la firma como la validez del certificado utilizado para crear la firma.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene los datos firmados y codificados.

Si se produce un error en este método, se producirá un error. El objeto **Err** contendrá información adicional sobre el error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
