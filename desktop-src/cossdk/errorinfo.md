---
description: Recupera información de error extendida con respecto a métodos que se ocupan de varios objetos, como rellenar y SaveChanges en el objeto COMAdminCatalogCollection, y métodos para instalar, importar o exportar aplicaciones o componentes en el objeto COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Colección ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496457"
---
# <a name="errorinfo-collection"></a>Colección ErrorInfo

Recupera información de error extendida con respecto a métodos que se ocupan de varios objetos, como [**rellenar**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , y métodos para instalar, importar o exportar aplicaciones o componentes en el objeto [**COMAdminCatalog**](comadmincatalog.md) .

Use el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en un [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para tener acceso a la colección **errorInfo** asociada a la colección original que tiene un error.

Debe llamar a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en **errorInfo** inmediatamente después de que se produzca un error. de lo contrario, se pierde la información de error.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **errorInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde cada colección, excepto por **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)y [**WOWInprocServers**](wowinprocservers.md).

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Nombre](#name)

### <a name="errorcode"></a>ErrorCode



| Entrada | Value |
|----------------|----------------------------------------|
| Descripción    | Código de error para el objeto o archivo. |
| Access         | ReadOnly                               |
| Tipo           | String                                 |
| Valor predeterminado        | None                                   |
| Sistema mínimo | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Valor de la propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) para el objeto que tiene un error. Por ejemplo, si se produce un error en una llamada a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para una colección en un objeto determinado de la colección, el valor de la propiedad **clave** para ese objeto se muestra como el valor de MajorRef. Utilice esta propiedad para ver el elemento que no se puede actualizar o para buscar el componente o DLL que no se puede instalar. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Valor predeterminado        | None                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Una especificación precisa del elemento que tiene un error, como un nombre de propiedad. Si se producen varios errores o en contextos en los que no se aplica, MinorRef es <Invalid> . |
| Access         | ReadOnly                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                            |
| Valor predeterminado        | None                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del objeto o archivo que tiene un error. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| Tipo           | String                                                                                                                                                                                                                   |
| Valor predeterminado        | None                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
