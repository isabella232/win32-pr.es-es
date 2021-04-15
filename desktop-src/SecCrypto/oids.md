---
description: Representa una colección de objetos OID.
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Objeto OID
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
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690060"
---
# <a name="oids-object"></a>Objeto OID

\[El objeto **OID** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase OidCollection**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **OID** representa una colección de objetos [**OID**](oid.md) . Cada objeto [**OID**](oid.md) representa un único identificador de objeto.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **OID** se usa para realizar las siguientes tareas:

-   Agregue o quite un objeto [**OID**](oid.md) de la colección.
-   Borre todos los objetos [**OID**](oid.md) de la colección.
-   Recupere el número de identificadores de objeto de la colección.
-   Recupera un objeto [**OID**](oid.md) específico de la colección.
-   Recorrer en iteración la colección.

## <a name="members"></a>Miembros

El objeto **OID** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **OID** tiene estos métodos.



| Método                        | Descripción                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**Agréguela**](oids-add.md)       | Agrega un objeto [**OID**](oid.md) a la colección.<br/>              |
| [**Claridad**](oids-clear.md)   | Borra todos los objetos [**OID**](oid.md) de la colección.<br/>        |
| [**Retirar**](oids-remove.md) | Quita un objeto [**OID**](oid.md) indizado de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **OID** tiene estas propiedades.



| Propiedad                                     | Tipo de acceso          | Descripción                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | Solo lectura<br/> | Recupera una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en un objeto que se puede utilizar para enumerar la colección. Esta propiedad está oculta en Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contabiliza**](oids-count.md)<br/>       | Solo lectura<br/> | Recupera el número de objetos [**OID**](oid.md) de la colección.<br/>                                                                                                                                                |
| [**Elemento**](oids-item.md)<br/>         | Solo lectura<br/> | Recupera un objeto [**OID**](oid.md) indizado de la colección. Esta es la propiedad predeterminada.<br/>                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

No se puede crear el objeto **OID** .

Las siguientes propiedades utilizan el objeto **OID** :

-   [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus.CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
