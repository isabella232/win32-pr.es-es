---
description: Recupera información relacionada con las aplicaciones en ejecución.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Colección ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465580"
---
# <a name="applicationinstances-collection"></a>Colección ApplicationInstances

Recupera información relacionada con las aplicaciones en ejecución.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección ApplicationInstances** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Aplicaciones**](applications.md)
-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Aplicación](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Application



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | Identificador de la aplicación en ejecución. |
| Acceso         | ReadOnly                            |
| Tipo           | String                              |
| Predeterminado        | N/D                                 |
| Sistema mínimo | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| Entrada | Value |
|----------------|---------------------------------------------------------------|
| Descripción    | Indica si se ha reciclado la instancia de la aplicación. |
| Acceso         | ReadOnly                                                      |
| Tipo           | Bool                                                          |
| Valor predeterminado        | False                                                         |
| Sistema mínimo | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador único global de la instancia de la aplicación. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                                                                              |
| Predeterminado        | N/D                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Entrada | Value |
|----------------|-----------------------------------------------------------------|
| Descripción    | Indica si la instancia de la aplicación está actualmente en pausa. |
| Acceso         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Valor predeterminado        | False                                                           |
| Sistema mínimo | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| Entrada | Value |
|----------------|-------------------------------------------------|
| Descripción    | Identificador de partición que usa la aplicación. |
| Acceso         | ReadOnly                                        |
| Tipo           | String                                          |
| Predeterminado        | N/D                                             |
| Sistema mínimo | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Entrada | Value |
|----------------|---------------------------------------------|
| Descripción    | Identificador de proceso de la instancia de la aplicación. |
| Acceso         | ReadOnly                                    |
| Tipo           | String                                      |
| Predeterminado        | N/D                                         |
| Sistema mínimo | Windows XP                                  |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
