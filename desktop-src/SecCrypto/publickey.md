---
description: El objeto PublicKey representa una clave pública en un objeto de certificado.
title: PublicKey (objeto)
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
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650185"
---
# <a name="publickey-object"></a>PublicKey (objeto)

\[El objeto **publicKey** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El objeto **publicKey** representa una clave pública en un objeto de [**certificado**](certificate.md) .

## <a name="when-to-use"></a>Cuándo se usa

El objeto **publicKey** se utiliza para recuperar datos sobre la clave pública.

## <a name="members"></a>Miembros

El objeto **publicKey** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **publicKey** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso          | Descripción                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](publickey-algorithm.md)<br/>                 | Solo lectura<br/> | Recupera el objeto [**OID**](oid.md) que identifica el algoritmo utilizado por la clave pública. Esta es la propiedad predeterminada.<br/> |
| [**EncodedKey**](publickey-encodedkey.md)<br/>               | Solo lectura<br/> | Recupera un objeto [**EncodedData**](encodeddata.md) que proporciona acceso al valor de la clave pública.<br/>                 |
| [**EncodedParameters**](publickey-encodedparameters.md)<br/> | Solo lectura<br/> | Recupera un objeto [**EncodedData**](encodeddata.md) que proporciona acceso a los parámetros del algoritmo de clave pública.<br/>  |
| [**Length**](publickey-length.md)<br/>                       | Solo lectura<br/> | Recupera la longitud de la clave pública en bits.<br/>                                                                             |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **publicKey** .

El método [**Certificate. publickey**](certificate-publickey.md) utiliza el objeto **publicKey** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
