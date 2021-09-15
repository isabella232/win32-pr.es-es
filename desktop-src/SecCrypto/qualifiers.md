---
description: Representa una colección de calificadores.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Objeto Qualifiers (Iads.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476393"
---
# <a name="qualifiers-object"></a>Objeto Qualifiers

\[El **objeto Calificadores** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la clase [**X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que forman parte de la información de directiva en la extensión Directivas de certificado.\]

El **objeto Qualifiers** representa una colección de calificadores.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto Qualifiers** se usa para realizar las tareas siguientes:

-   Recupere una propiedad extendida específica de la colección.
-   Recupere el número de propiedades extendidas de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Members

El **objeto Qualifiers** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto Qualifiers** tiene estas propiedades.



| Propiedad.                                           | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Count**](qualifiers-count.md)<br/>       | Solo lectura<br/> | Recupera el número de calificadores de la colección.<br/>                                                                                                                                                                |
| [**Artículo**](qualifiers-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**Qualifier**](qualifier.md) que representa el calificador indexado de la colección. Esta es la propiedad predeterminada.<br/>                                                                             |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **Qualifiers.**

La propiedad de objeto CAPICOM [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) devuelve un **objeto Qualifiers.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Encabezado<br/>          | <dl> <dt>Iads.h</dt> </dl>      |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
