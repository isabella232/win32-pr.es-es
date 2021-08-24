---
description: La colección RolesForPartition siempre está relacionada con un objeto de la colección Partitions. Contiene un objeto para cada rol asignado a la partición a la que está relacionado.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Colección RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6c1e64e314478793a5b421d1f0a6a76c2eb028708410a14ea426f52fbd41dfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637045"
---
# <a name="rolesforpartition-collection"></a>Colección RolesForPartition

La **colección RolesForPartition** siempre está relacionada con un objeto de la [**colección Partitions.**](partitions.md) Contiene un objeto para cada rol asignado a la partición a la que está relacionado.

Esta colección no admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección RolesForPartition** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInPartitionRole**](usersinpartitionrole.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Particiones**](partitions.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Descripción](#description)
-   [Nombre](#name)

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------|
| Descripción    | Descripción del rol. |
| Access         | ReadOnly                   |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows Server 2003        |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del rol. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                                                                                                    |
| Tipo           | String                                                                                                                                                                                                                                                      |
| Predeterminado        | ""                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
