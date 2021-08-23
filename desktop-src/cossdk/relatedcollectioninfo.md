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
ms.openlocfilehash: 45e9e0f0e251bc9b0772d5def40fec148d541964d34e4f1dda954825f456468b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637095"
---
# <a name="relatedcollectioninfo-collection"></a>Colección RelatedCollectionInfo

Recupera información sobre otras colecciones relacionadas con la colección desde la que se llama. La **colección RelatedCollectionInfo** es accesible desde cualquier [**objeto COMAdminCatalogCollection**](comadmincatalogcollection.md) mediante el [**método GetCollection.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) La **colección RelatedCollectionInfo** contiene un objeto para cada colección a la que se puede acceder desde la colección original. Las colecciones relacionadas siguen la jerarquía de recopilación de herramientas de administración de Servicios de componentes.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección RelatedCollectionInfo** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**Propertyinfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

Puede navegar a esta colección desde cada colección.

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [Nombre](#name)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la colección relacionada. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                     |
| Predeterminado        | None                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                               |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
