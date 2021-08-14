---
description: Recupera información para las aplicaciones que se importan.
ms.assetid: 9ed4bc3f-3490-4c36-ba94-bc803886a4d2
title: Colección FilesForImport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilesForImport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3b6351edd58691db3a499a6c0512e76fe87167f888289b8a2d2a947fe1304cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307332"
---
# <a name="filesforimport-collection"></a>Colección FilesForImport

Recupera información para las aplicaciones que se importan.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección FilesForImport** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [ApplicationFileName](#applicationfilename)
-   [ApplicationName](#applicationname)
-   [Descripción](#partitiondescription)
-   [FileName](#applicationfilename)
-   [HasUsers](#hasusers)
-   [IsProxy](#isproxy)
-   [IsService](#isservice)
-   [PartitionDescription](#partitiondescription)
-   [PartitionID](#partitionid)
-   [PartitionName](#partitionname)

### <a name="applicationfilename"></a>ApplicationFileName



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------|
| Descripción    | Nombre del archivo MSI que contiene la aplicación que se puede importar. |
| Access         | ReadOnly                                                                     |
| Tipo           | String                                                                       |
| Predeterminado        | N/D                                                                          |
| Sistema mínimo | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Entrada | Valor |
|----------------|------------------------------|
| Descripción    | Nombre de la aplicación. |
| Access         | ReadOnly                     |
| Tipo           | String                       |
| Predeterminado        | ""                           |
| Sistema mínimo | Windows XP                   |



 

### <a name="description"></a>Descripción



| Entrada | Valor |
|----------------|-----------------------------------|
| Descripción    | Descripción de la aplicación. |
| Access         | ReadOnly                          |
| Tipo           | String                            |
| Predeterminado        | ""                                |
| Sistema mínimo | Windows XP                        |



 

### <a name="filename"></a>FileName



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del archivo DLL o EXE que contiene la aplicación. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                |
| Predeterminado        | ""                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| Entrada | Valor |
|----------------|--------------------------------------------------|
| Descripción    | Indica si la aplicación tiene usuarios. |
| Access         | ReadOnly                                         |
| Tipo           | Bool                                             |
| Valor predeterminado        | False                                            |
| Sistema mínimo | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Entrada | Valor |
|----------------|-----------------------------------------------|
| Descripción    | Indica si la aplicación es un proxy. |
| Access         | ReadOnly                                      |
| Tipo           | Bool                                          |
| Valor predeterminado        | False                                         |
| Sistema mínimo | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Entrada | Valor |
|----------------|-------------------------------------------------|
| Descripción    | Indica si la aplicación es un servicio. |
| Access         | ReadOnly                                        |
| Tipo           | Bool                                            |
| Valor predeterminado        | False                                           |
| Sistema mínimo | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Entrada | Valor |
|----------------|-----------------------------------------------|
| Descripción    | Descripción de la partición de la aplicación. |
| Access         | ReadOnly                                      |
| Tipo           | String                                        |
| Predeterminado        | ""                                            |
| Sistema mínimo | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Entrada | Valor |
|----------------|------------------------------------------|
| Descripción    | GUID de la partición de la aplicación. |
| Access         | ReadOnly                                 |
| Tipo           | String                                   |
| Predeterminado        | ""                                       |
| Sistema mínimo | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Entrada | Valor |
|----------------|------------------------------------------|
| Descripción    | Nombre de la partición de la aplicación. |
| Access         | ReadOnly                                 |
| Tipo           | String                                   |
| Predeterminado        | ""                                       |
| Sistema mínimo | Windows Server 2003                      |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
