---
description: Especifica las aplicaciones contenidas en cada partición.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Colección de particiones
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2f7ba43cbfd33736c9997adb4c312e044cf28e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965136"
---
# <a name="partitions-collection"></a>Colección de particiones

Especifica las aplicaciones contenidas en cada partición.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección Partitions** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**Aplicaciones**](applications.md)
-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**RolesForPartition**](rolesforpartition.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Cambiable](#changeable)
-   [Eliminable](#deleteable)
-   [Descripción](#description)
-   [ID](#partitions-collection)
-   [Nombre](#name)

### <a name="changeable"></a>Cambiable



| Entrada | Value |
|----------------|--------------------------------------------------|
| Descripción    | Determina si esta partición es modificable. |
| Acceso         | ReadWrite                                        |
| Tipo           | Bool                                             |
| Default        | True                                             |
| Sistema mínimo | Windows Server 2003                              |



 

### <a name="deleteable"></a>Eliminable



| Entrada | Value |
|----------------|---------------------------------------------------|
| Descripción    | Determina si se puede eliminar esta partición. |
| Acceso         | ReadWrite                                         |
| Tipo           | Bool                                              |
| Default        | True                                              |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|---------------------------------------------------------------------|
| Descripción    | Esta propiedad representa la descripción que identifica la partición. |
| Acceso         | ReadWrite                                                           |
| Tipo           | String                                                              |
| Predeterminado        | ""                                                                  |
| Sistema mínimo | Windows Server 2003                                                 |



 

### <a name="id"></a>ID



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID que representa la partición. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                          |
| Tipo           | String                                                                                                                                                             |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el nombre de la partición. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadWrite                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva partición"                                                                                                                                                                                                                        |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
