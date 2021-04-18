---
description: Recupera el valor de la clave pública.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Propiedad PublicKey. EncodedKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690934"
---
# <a name="publickeyencodedkey-property"></a>Propiedad PublicKey. EncodedKey

\[La propiedad **EncodedKey** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **EncodedKey** recupera el valor de la clave pública.

## <a name="syntax"></a>Sintaxis


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>Valor de propiedad

Un objeto [**EncodedData**](encodeddata.md) que proporciona acceso al valor de la clave pública.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
