---
description: Contiene un objeto para cada método de la interfaz a la que está relacionada la colección.
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
ms.openlocfilehash: be182d237c1c46ed816c0b413bef7b0aa10ce6c290bd0da0f53153db7c0520cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916304"
---
# <a name="methodsforinterface-collection"></a>Colección MethodsForInterface

Contiene un objeto para cada método de la interfaz a la que está relacionada la colección.

Esta colección no admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección MethodsForInterface** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForMethod**](rolesformethod.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**InterfacesForComponent**](interfacesforcomponent.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [AutoComplete](#autocomplete)
-   [Clsid](#clsid)
-   [Descripción](#description)
-   [IID](#iid)
-   [Index](#index)
-   [Nombre](#name)

### <a name="autocomplete"></a>Autocompletar



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Determina si el objeto se desactiva automáticamente cuando se completa el método, sin que se llame necesariamente a SetComplete o SetAbort. Esto solo afecta a la configuración predeterminada del bit "Listo" de activación JIT al iniciar el método; Este bit se puede restablecer (como con SetComplete o SetAbort) dentro del método para invalidar el valor predeterminado. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                                                                                                                  |
| Tipo           | Bool                                                                                                                                                                                                                                                                                                                                       |
| Valor predeterminado        | False                                                                                                                                                                                                                                                                                                                                      |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                               |



 

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
|----------------|------------------------------|
| Descripción    | Descripción del método. |
| Acceso         | ReadWrite                    |
| Tipo           | String                       |
| Predeterminado        | ""                           |
| Sistema mínimo | Windows 2000                 |



 

### <a name="iid"></a>IID



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | GUID para la interfaz. |
| Acceso         | ReadOnly                  |
| Tipo           | String                    |
| Predeterminado        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

### <a name="index"></a>Índice



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador de distribución del método. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                        |
| Tipo           | **DWORD**                                                                                                                                                       |
| Valor predeterminado        | N/D                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                    |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre del método. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                           |
| Tipo           | String                                                                                                                                             |
| Predeterminado        | N/D                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
