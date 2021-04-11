---
description: Recupera información sobre otras colecciones relacionadas con la colección desde la que se llama.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Colección RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274947"
---
# <a name="relatedcollectioninfo-collection"></a>Colección RelatedCollectionInfo

Recupera información sobre otras colecciones relacionadas con la colección desde la que se llama. Se puede acceder a la colección **RelatedCollectionInfo** desde cualquier objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) . La colección **RelatedCollectionInfo** contiene un objeto para cada colección que es accesible desde la colección original. Las colecciones relacionadas siguen la jerarquía de colecciones de herramientas de administración de servicios de componentes.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **RelatedCollectionInfo** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**PropertyInfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

Puede navegar a esta colección desde cada colección.

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Nombre](#name)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la colección relacionada. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                     |
| Valor predeterminado        | None                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
