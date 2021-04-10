---
description: Recupera información de las aplicaciones que se importan.
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
ms.openlocfilehash: 8e7ba3b0bd44cf2f6bb40ecf89f86dd68c21cf3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153259"
---
# <a name="filesforimport-collection"></a>Colección FilesForImport

Recupera información de las aplicaciones que se importan.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **FilesForImport** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

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



| Entrada | Value |
|----------------|------------------------------------------------------------------------------|
| Descripción    | Nombre del archivo MSI que contiene la aplicación que se puede importar. |
| Access         | ReadOnly                                                                     |
| Tipo           | String                                                                       |
| Predeterminado        | N/D                                                                          |
| Sistema mínimo | Windows XP                                                                   |



 

### <a name="applicationname"></a>ApplicationName



| Entrada | Value |
|----------------|------------------------------|
| Descripción    | Nombre de la aplicación. |
| Access         | ReadOnly                     |
| Tipo           | String                       |
| Predeterminado        | ""                           |
| Sistema mínimo | Windows XP                   |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|-----------------------------------|
| Descripción    | Una descripción de la aplicación. |
| Access         | ReadOnly                          |
| Tipo           | String                            |
| Predeterminado        | ""                                |
| Sistema mínimo | Windows XP                        |



 

### <a name="filename"></a>FileName



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del archivo DLL o EXE que contiene la aplicación. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                |
| Predeterminado        | ""                                                                                                                                                                                                                                    |
| Sistema mínimo | Windows XP                                                                                                                                                                                                                            |



 

### <a name="hasusers"></a>HasUsers



| Entrada | Value |
|----------------|--------------------------------------------------|
| Descripción    | Indica si la aplicación tiene algún usuario. |
| Access         | ReadOnly                                         |
| Tipo           | Bool                                             |
| Valor predeterminado        | False                                            |
| Sistema mínimo | Windows XP                                       |



 

### <a name="isproxy"></a>IsProxy



| Entrada | Value |
|----------------|-----------------------------------------------|
| Descripción    | Indica si la aplicación es un proxy. |
| Access         | ReadOnly                                      |
| Tipo           | Bool                                          |
| Valor predeterminado        | False                                         |
| Sistema mínimo | Windows XP                                    |



 

### <a name="isservice"></a>IsService



| Entrada | Value |
|----------------|-------------------------------------------------|
| Descripción    | Indica si la aplicación es un servicio. |
| Access         | ReadOnly                                        |
| Tipo           | Bool                                            |
| Valor predeterminado        | False                                           |
| Sistema mínimo | Windows XP                                      |



 

### <a name="partitiondescription"></a>PartitionDescription



| Entrada | Value |
|----------------|-----------------------------------------------|
| Descripción    | Una descripción de la partición de la aplicación. |
| Access         | ReadOnly                                      |
| Tipo           | String                                        |
| Predeterminado        | ""                                            |
| Sistema mínimo | Windows Server 2003                           |



 

### <a name="partitionid"></a>PartitionID



| Entrada | Value |
|----------------|------------------------------------------|
| Descripción    | GUID de la partición de la aplicación. |
| Access         | ReadOnly                                 |
| Tipo           | String                                   |
| Predeterminado        | ""                                       |
| Sistema mínimo | Windows Server 2003                      |



 

### <a name="partitionname"></a>PartitionName



| Entrada | Value |
|----------------|------------------------------------------|
| Descripción    | Nombre de la partición de la aplicación. |
| Access         | ReadOnly                                 |
| Tipo           | String                                   |
| Predeterminado        | ""                                       |
| Sistema mínimo | Windows Server 2003                      |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
