---
description: Determina si las firmas de los datos firmados en el objeto SignedData son válidas.
ms.assetid: 920ac235-0c1a-4b15-9cdd-c7e0c3ea6107
title: Método SignedData.Verify
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
ms.openlocfilehash: ccda81fc3640d4d09f9644bdf0d84a18a68b743397e1578a5ad434349893e893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898979"
---
# <a name="signeddataverify-method"></a>Método SignedData.Verify

\[El **método Verify** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Verify** determina si las firmas de los datos [*firmados*](../secgloss/d-gly.md) en el [**objeto SignedData**](signeddata.md) son válidas. Para comprobar una firma, el [*hash*](../secgloss/h-gly.md) cifrado del contenido se descifra mediante la clave pública del firmante del certificado del firmante. El hash descifrado se compara con un nuevo hash del contenido de datos. Una firma es válida si los valores hash coinciden. Además, este método también compila una cadena de certificados para determinar [](../secgloss/p-gly.md) la validez del certificado que proporciona la clave pública utilizada para descifrar el hash.

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

*SignedMessage* \[ En\]
</dt> <dd>

Cadena que contiene el mensaje firmado que se va a comprobar.

</dd> <dt>

*bDetached* \[ in, opcional\]
</dt> <dd>

Si **es True**, se desasocian los datos que se firmarán; Es decir, el contenido firmado no se incluye como parte del objeto firmado. Para comprobar la firma en el contenido desasociado, una aplicación debe tener una copia del contenido original. El contenido desasociado se suele usar para reducir el tamaño de un objeto firmado que se va a enviar a través de la web, si el destinatario del mensaje firmado tiene una copia original de los datos firmados. El valor predeterminado es **False**.

</dd> <dt>

*VerifyFlag* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG](capicom-signed-data-verify-flag.md) que indica la directiva de comprobación. El valor predeterminado es CAPICOM \_ VERIFY \_ SIGNATURE AND \_ \_ CERTIFICATE. Con este valor, se comprueba la validez del certificado y la validez de la firma. Este parámetro se puede establecer para comprobar la firma y no el certificado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                             | Significado                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_VERIFY_SIGNATURE_ONLY"></span><span id="capicom_verify_signature_only"></span><dl> <dt>**CAPICOM \_ VERIFY \_ SIGNATURE \_ ONLY**</dt> </dl>                                   | Solo se comprueba la firma.<br/>                                                                   |
| <span id="CAPICOM_VERIFY_SIGNATURE_AND_CERTIFICATE"></span><span id="capicom_verify_signature_and_certificate"></span><dl> <dt>**CAPICOM \_ VERIFY \_ SIGNATURE \_ AND \_ CERTIFICATE**</dt> </dl> | Se comprueban tanto la firma como la validez del certificado usado para crear la firma.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene los datos codificados y firmados.

Si se produce un error en este método, se producirá un error. El **objeto Err** contendrá información adicional sobre el error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
