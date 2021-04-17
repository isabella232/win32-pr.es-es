---
description: Recupera los parámetros del algoritmo de clave pública.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Propiedad PublicKey. EncodedParameters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671053"
---
# <a name="publickeyencodedparameters-property"></a>Propiedad PublicKey. EncodedParameters

\[La propiedad **EncodedParameters** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **EncodedParameters** recupera los parámetros del algoritmo de clave pública.

## <a name="syntax"></a>Sintaxis


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a>Valor de propiedad

Un objeto [**EncodedData**](encodeddata.md) que proporciona acceso a los parámetros del algoritmo de clave pública.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PublicKey**](publickey.md)
</dt> </dl>

 

 
