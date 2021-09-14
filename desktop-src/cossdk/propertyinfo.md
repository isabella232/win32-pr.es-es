---
description: Recupera información sobre las propiedades que admite una colección especificada.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Colección PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063895"
---
# <a name="propertyinfo-collection"></a>Colección PropertyInfo

Recupera información sobre las propiedades que admite una colección especificada. La **colección PropertyInfo** es accesible desde cualquier [**objeto COMAdminCatalogCollection**](comadmincatalogcollection.md) mediante el [**método GetCollection.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) La **colección PropertyInfo** contiene un objeto para cada propiedad admitida por la colección original.

## <a name="members"></a>Members

La **colección PropertyInfo** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   **Propertyinfo**
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde cada colección.

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Nombre](#name)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre de la propiedad. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                                                         |
| Tipo           | String                                                                                                                                                                                           |
| Valor predeterminado        | None                                                                                                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                                                                                                     |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
