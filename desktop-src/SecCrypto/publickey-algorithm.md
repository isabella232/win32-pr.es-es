---
description: La propiedad Algorithm recupera el objeto OID que identifica el algoritmo utilizado por la clave pública. Esta es la propiedad predeterminada.
ms.assetid: f804ac4b-6a33-4f25-950b-6b6838bcc638
title: PublicKey. algorithm (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98e955279646306b1484dcd0674cf735680d44e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671054"
---
# <a name="publickeyalgorithm-property"></a>PublicKey. algorithm (propiedad)

\[La propiedad **algorithm** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **algorithm** recupera el objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
PublicKey.Algorithm As OID
```



## <a name="property-value"></a>Valor de propiedad

Objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
