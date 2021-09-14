---
description: Contiene un objeto para cada interfaz expuesta por el componente al que está relacionada la colección.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Colección InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361699"
---
# <a name="interfacesforcomponent-collection"></a>Colección InterfacesForComponent

Contiene un objeto para cada interfaz expuesta por el componente al que está relacionada la colección.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección InterfacesForComponent** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**MethodsForInterface**](methodsforinterface.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForInterface**](rolesforinterface.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Componentes**](components.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [CLSID](#clsid)
-   [Descripción](#description)
-   [IID](#iid)
-   [Nombre](#name)
-   [QueuingEnabled](#queuingenabled)
-   [QueueingSupported](#queueingsupported)

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | GUID para el componente. |
| Acceso         | ReadOnly                  |
| Tipo           | String                    |
| Predeterminado        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------------|
| Descripción    | Descripción de la interfaz. |
| Acceso         | ReadWrite                        |
| Tipo           | String                           |
| Predeterminado        | ""                               |
| Sistema mínimo | Windows 2000                     |



 

### <a name="iid"></a>IID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID para la interfaz. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la interfaz. Esta propiedad se devuelve cuando se [**llama al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                    |
| Tipo           | String                                                                                                                                                      |
| Predeterminado        | N/D                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                |



 

### <a name="queuingenabled"></a>QueuingEnabled



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Marca la interfaz como queuable y se puede establecer mediante el SDK de administración o la herramienta administrativa Servicios de componentes. Sin embargo, solo una interfaz que tenga establecida la marca **Queuing Supported** puede tener establecida la marca **Cola** habilitada. |
| Acceso         | ReadWrite                                                                                                                                                                                                                          |
| Tipo           | Bool                                                                                                                                                                                                                               |
| Valor predeterminado        | False                                                                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a>QueueingSupported



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | La interfaz admite la cola. Para que una interfaz admita la cola, todos los métodos solo deben tener parámetros en . **La cola admitida se** expone como una propiedad de solo lectura. |
| Acceso         | ReadOnly                                                                                                                                                               |
| Tipo           | Bool                                                                                                                                                                   |
| Valor predeterminado        | False                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                           |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
