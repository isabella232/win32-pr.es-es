---
description: Proporciona acceso a la información de la Directiva de una extensión.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Objeto PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670431"
---
# <a name="policyinformation-object"></a>Objeto PolicyInformation

\[El objeto **PolicyInformation** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar la información de la Directiva en la extensión de directivas de certificado.\]

El objeto **PolicyInformation** proporciona acceso a la información de la Directiva de una extensión.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **PolicyInformation** se usa para realizar las siguientes tareas:

-   Recupere el OID de la Directiva.
-   Recupera una colección de los calificadores de la Directiva.

## <a name="members"></a>Miembros

El objeto **PolicyInformation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **PolicyInformation** tiene estas propiedades.



| Propiedad                                                      | Descripción                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**OID**](policyinformation-oid.md)<br/>               | Recupera el OID de la Directiva, como un objeto [**OID**](oid.md) . Esta es la propiedad predeterminada.<br/>       |
| [**Calificadores**](policyinformation-qualifiers.md)<br/> | Recupera una colección de los calificadores de la Directiva, como un objeto [**calificadores**](qualifiers.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **PolicyInformation** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
