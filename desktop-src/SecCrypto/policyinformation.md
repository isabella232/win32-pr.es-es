---
description: Proporciona acceso a la información de directiva de una extensión.
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
ms.openlocfilehash: fa717361ac5cb270eb61f0199b92cb801a46fabd143a9dd1ed26e43e23383657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978576"
---
# <a name="policyinformation-object"></a>Objeto PolicyInformation

\[El **objeto PolicyInformation** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar información de directiva en la extensión Directivas de certificado.\]

El **objeto PolicyInformation** proporciona acceso a la información de directiva de una extensión.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto PolicyInformation** se usa para realizar las tareas siguientes:

-   Recupere el OID de directiva.
-   Recuperar una colección de calificadores de la directiva.

## <a name="members"></a>Miembros

El **objeto PolicyInformation** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto PolicyInformation** tiene estas propiedades.



| Propiedad                                                      | Descripción                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Oid**](policyinformation-oid.md)<br/>               | Recupera el OID de la directiva, como un [**objeto OID.**](oid.md) Esta es la propiedad predeterminada.<br/>       |
| [**Calificadores**](policyinformation-qualifiers.md)<br/> | Recupera una colección de calificadores de la directiva, como un [**objeto Qualifiers.**](qualifiers.md)<br/> |



 

## <a name="remarks"></a>Comentarios

No se puede crear el objeto **PolicyInformation.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
