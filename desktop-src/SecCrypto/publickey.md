---
description: El objeto PublicKey representa una clave pública en un objeto Certificate.
title: Objeto PublicKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d27a89d51840e70563854b3cc7f9084b6bd42cb5707630755e771d610c64a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901352"
---
# <a name="publickey-object"></a>Objeto PublicKey

\[El **objeto PublicKey** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **objeto PublicKey** representa una clave pública en un [**objeto Certificate.**](certificate.md)

## <a name="when-to-use"></a>Cuándo se usa

El **objeto PublicKey** se usa para recuperar datos sobre la clave pública.

## <a name="members"></a>Miembros

El **objeto PublicKey** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto PublicKey** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso          | Descripción                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](publickey-algorithm.md)<br/>                 | Solo lectura<br/> | Recupera el objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública. Esta es la propiedad predeterminada.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Solo lectura<br/> | Recupera un [**objeto EncodedData**](encodeddata.md) que proporciona acceso al valor de la clave pública.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Solo lectura<br/> | Recupera un objeto [**EncodedData**](encodeddata.md) que proporciona acceso a los parámetros del algoritmo de clave pública.<br/>  |
| [**Longitud**](publickey-length.md)<br/>                       | Solo lectura<br/> | Recupera la longitud de la clave pública en bits.<br/>                                                                             |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **PublicKey.**

El método [**Certificate.PublicKey**](certificate-publickey.md) usa el objeto **PublicKey.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
