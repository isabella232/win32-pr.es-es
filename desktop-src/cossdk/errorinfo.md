---
description: Recupera información de error extendida sobre los métodos que tratan con varios objetos, como Populate y SaveChanges en el objeto COMAdminCatalogCollection, y los métodos para instalar, importar o exportar aplicaciones o componentes en el objeto COMAdminCatalog.
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
ms.openlocfilehash: 9953bc1119d7e203936ca7e78048a4083a996ec2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160499"
---
# <a name="errorinfo-collection"></a>Colección ErrorInfo

Recupera información de error extendida sobre los métodos que tratan con varios objetos, como [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) y [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) en el objeto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) y los métodos para instalar, importar o exportar aplicaciones o componentes en el objeto [**COMAdminCatalog.**](comadmincatalog.md)

Use el [**método GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en [**COMAdminCatalogCollection para**](comadmincatalogcollection.md) tener acceso a la colección **ErrorInfo** asociada a la colección original que tiene un error.

Debe llamar a [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) en **ErrorInfo inmediatamente** después de que se produzca un error. De lo contrario, se pierde la información de error.

Esta colección no admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección ErrorInfo** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde todas las colecciones excepto **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md)y [**WOWInprocServers.**](wowinprocservers.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Nombre](#name)

### <a name="errorcode"></a>ErrorCode



| Entrada | Value |
|----------------|----------------------------------------|
| Descripción    | Código de error para el objeto o archivo. |
| Acceso         | ReadOnly                               |
| Tipo           | String                                 |
| Valor predeterminado        | None                                   |
| Sistema mínimo | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Valor [**de**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) propiedad Key para el objeto que tiene un error. Por ejemplo, si se produce un error en una llamada [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para una colección en un objeto determinado de la colección, el valor de la propiedad **Key** de ese objeto se notifica como el valor MajorRef. Use esta propiedad para ver el elemento que no se puede actualizar o para buscar el componente o dll que no se puede instalar. |
| Acceso         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Valor predeterminado        | None                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Especificación precisa del elemento que tiene un error, como un nombre de propiedad. Si se producen varios errores o en contextos en los que esto no se aplica, MinorRef no &lt; es &gt; válido. |
| Acceso         | ReadOnly                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                            |
| Valor predeterminado        | None                                                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del objeto o archivo que tiene un error. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                                                                                 |
| Tipo           | String                                                                                                                                                                                                                   |
| Valor predeterminado        | None                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
