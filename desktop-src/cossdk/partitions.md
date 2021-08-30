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
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882522"
---
# <a name="partitions-collection"></a>Colección de particiones

Especifica las aplicaciones contenidas en cada partición.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

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

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [Cambiable](#changeable)
-   [Eliminable](#deleteable)
-   [Descripción](#description)
-   [ID](#partitions-collection)
-   [Nombre](#name)

### <a name="changeable"></a>Cambiable



| Entrada | Valor |
|----------------|--------------------------------------------------|
| Descripción    | Determina si esta partición es modificable. |
| Access         | ReadWrite                                        |
| Tipo           | Bool                                             |
| Valor predeterminado        | True                                             |
| Sistema mínimo | Windows Server 2003                              |



 

### <a name="deleteable"></a>Eliminable



| Entrada | Valor |
|----------------|---------------------------------------------------|
| Descripción    | Determina si se puede eliminar esta partición. |
| Access         | ReadWrite                                         |
| Tipo           | Bool                                              |
| Valor predeterminado        | True                                              |
| Sistema mínimo | Windows Server 2003                               |



 

### <a name="description"></a>Descripción



| Entrada | Valor |
|----------------|---------------------------------------------------------------------|
| Descripción    | Esta propiedad representa la descripción que identifica la partición. |
| Access         | ReadWrite                                                           |
| Tipo           | String                                                              |
| Predeterminado        | ""                                                                  |
| Sistema mínimo | Windows Server 2003                                                 |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID que representa la partición. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                          |
| Tipo           | String                                                                                                                                                             |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                  |
| Sistema mínimo | Windows Server 2003                                                                                                                                                |



 

### <a name="name"></a>Nombre



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el nombre de la partición. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se [**llama al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva partición"                                                                                                                                                                                                                        |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                    |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
