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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496126"
---
# <a name="applicationinstances-collection"></a>Colección ApplicationInstances

Recupera información relacionada con las aplicaciones en ejecución.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **ApplicationInstances** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**APLICACIONES**](applications.md)
-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Aplicación](#applicationinstances-collection)
-   [HasRecycled](#hasrecycled)
-   [InstanceID](#instanceid)
-   [IsPaused](#ispaused)
-   [PartitionID](#partitionid)
-   [ProcessID](#processid)

### <a name="application"></a>Application



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | IDENTIFICADOR de la aplicación en ejecución. |
| Access         | ReadOnly                            |
| Tipo           | String                              |
| Predeterminado        | N/D                                 |
| Sistema mínimo | Windows XP                          |



 

### <a name="hasrecycled"></a>HasRecycled



| Entrada | Value |
|----------------|---------------------------------------------------------------|
| Descripción    | Indica si se ha reciclado la instancia de la aplicación. |
| Access         | ReadOnly                                                      |
| Tipo           | Bool                                                          |
| Valor predeterminado        | False                                                         |
| Sistema mínimo | Windows XP                                                    |



 

### <a name="instanceid"></a>InstanceID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador único global de la instancia de la aplicación. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                                                                              |
| Predeterminado        | N/D                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a>IsPaused



| Entrada | Value |
|----------------|-----------------------------------------------------------------|
| Descripción    | Indica si la instancia de la aplicación está en pausa actualmente. |
| Access         | ReadOnly                                                        |
| Tipo           | Bool                                                            |
| Valor predeterminado        | False                                                           |
| Sistema mínimo | Windows XP                                                      |



 

### <a name="partitionid"></a>PartitionID



| Entrada | Value |
|----------------|-------------------------------------------------|
| Descripción    | El identificador de partición que utiliza la aplicación. |
| Access         | ReadOnly                                        |
| Tipo           | String                                          |
| Predeterminado        | N/D                                             |
| Sistema mínimo | Windows XP                                      |



 

### <a name="processid"></a>ProcessID



| Entrada | Value |
|----------------|---------------------------------------------|
| Descripción    | Identificador de proceso de la instancia de la aplicación. |
| Access         | ReadOnly                                    |
| Tipo           | String                                      |
| Predeterminado        | N/D                                         |
| Sistema mínimo | Windows XP                                  |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
