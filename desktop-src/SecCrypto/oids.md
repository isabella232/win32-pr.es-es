---
description: Representa una colección de objetos OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objeto OIDs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32b6e2847a3e9848a67f0b96724e8883e2857d63abbaecc0a071f1a03eb03d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979187"
---
# <a name="oids-object"></a>Objeto OIDs

\[El **objeto OIDs** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase OidCollection en**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) el espacio de nombres [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto OID representa** una colección de objetos [**OID.**](oid.md) Cada [**objeto OID**](oid.md) representa un único identificador de objeto.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto OIDs** se usa para realizar las siguientes tareas:

-   Agregue o quite un [**objeto OID**](oid.md) de la colección.
-   Borre todos los [**objetos OID**](oid.md) de la colección.
-   Recupere el número de identificadores de objeto de la colección.
-   Recupere un objeto [**OID**](oid.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El **objeto OIDs** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto OIDs** tiene estos métodos.



| Método                        | Descripción                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Añadir**](oids-add.md)       | Agrega un [**objeto OID**](oid.md) a la colección.<br/>              |
| [**Borrar**](oids-clear.md)   | Borra todos los [**objetos OID**](oid.md) de la colección.<br/>        |
| [**Quitar**](oids-remove.md) | Quita un objeto [**OID indexado**](oid.md) de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto OIDs** tiene estas propiedades.



| Propiedad                                     | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | Solo lectura<br/> | Recupera una [**interfaz IEnumVARIANT en**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) un objeto que se puede usar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](oids-count.md)<br/>       | Solo lectura<br/> | Recupera el número de [**objetos OID**](oid.md) de la colección.<br/>                                                                                                                                                |
| [**Elemento**](oids-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**OID indexado**](oid.md) de la colección. Esta es la propiedad predeterminada.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Comentarios

No **se puede crear el objeto OIDs.**

Las propiedades siguientes usan el objeto **OIDs:**

-   [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus.CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
