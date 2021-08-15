---
description: Recupera el valor de la clave pública.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Propiedad PublicKey.EncodedKey
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
ms.openlocfilehash: 0d4708461f5ff51d5f86170ba0f1df35669859149b4882f8fb86aafdbed5e436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901467"
---
# <a name="publickeyencodedkey-property"></a>Propiedad PublicKey.EncodedKey

\[La **propiedad EncodedKey** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad EncodedKey** recupera el valor de la clave pública.

## <a name="syntax"></a>Sintaxis


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**EncodedData**](encodeddata.md) que proporciona acceso al valor de la clave pública.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
