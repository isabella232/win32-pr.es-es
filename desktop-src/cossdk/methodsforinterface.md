---
description: Contiene un objeto para cada método de la interfaz con la que está relacionada la colección.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Colección MethodsForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423495"
---
# <a name="methodsforinterface-collection"></a>Colección MethodsForInterface

Contiene un objeto para cada método de la interfaz con la que está relacionada la colección.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **MethodsForInterface** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForMethod**](rolesformethod.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**InterfacesForComponent**](interfacesforcomponent.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Autocompletar](#autocomplete)
-   [CLSID](#clsid)
-   [Descripción](#description)
-   [IID](#iid)
-   [Index](#index)
-   [Nombre](#name)

### <a name="autocomplete"></a>Autocompletar



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si el objeto se desactiva automáticamente cuando se completa el método, sin que se llame necesariamente a SetComplete o SetAbort. Esto solo afecta a la configuración predeterminada del bit de activación JIT "Done" en el inicio del método; este bit se puede restablecer (como con SetComplete o SetAbort) dentro del método para reemplazar el valor predeterminado. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                       |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | GUID del componente. |
| Access         | ReadOnly                  |
| Tipo           | String                    |
| Predeterminado        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|------------------------------|
| Descripción    | Descripción del método. |
| Access         | ReadWrite                    |
| Tipo           | String                       |
| Predeterminado        | ""                           |
| Sistema mínimo | Windows 2000                 |



 

### <a name="iid"></a>IID



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | Un GUID para la interfaz. |
| Access         | ReadOnly                  |
| Tipo           | String                    |
| Predeterminado        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

### <a name="index"></a>Índice



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador de envío del método. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                        |
| Tipo           | **DWORD**                                                                                                                                                       |
| Valor predeterminado        | N/D                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre del método. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                           |
| Tipo           | String                                                                                                                                             |
| Predeterminado        | N/D                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
