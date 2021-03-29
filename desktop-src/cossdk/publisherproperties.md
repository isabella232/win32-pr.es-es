---
description: Contiene un objeto para cada propiedad de publicador para la colección SubscriptionsForComponent primaria.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Colección PublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153195"
---
# <a name="publisherproperties-collection"></a>Colección PublisherProperties

Contiene un objeto para cada propiedad de publicador para la colección [**SubscriptionsForComponent**](subscriptionsforcomponent.md) primaria.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **PublisherProperties** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**SubscriptionsForComponent**](subscriptionsforcomponent.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Nombre](#name)
-   [Valor](#value)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la propiedad. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva propiedad"                                                                                                                                                                                                                                                         |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Value



| Entrada | Value |
|----------------|---------------------------|
| Descripción    | Valor de la propiedad. |
| Access         | ReadWrite                 |
| Tipo           | Variante                   |
| Valor predeterminado        | N/D                       |
| Sistema mínimo | Windows 2000              |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
