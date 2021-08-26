---
description: La colección Roles siempre está relacionada con un objeto de la colección Applications. Contiene un objeto para cada rol asignado a la aplicación con la que está relacionado.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Colección de roles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: 133477d82f718b992a628bde8af58f22d8d50a9e4974816c7c8f56be7ba8e33f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029475"
---
# <a name="roles-collection"></a>Colección de roles

La **colección Roles** siempre está relacionada con un objeto de la [**colección**](applications.md) Applications. Contiene un objeto para cada rol asignado a la aplicación con la que está relacionado.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección Roles** hereda de la interfaz [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**APLICACIONES**](applications.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [Descripción](#description)
-   [Nombre](#name)

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------|
| Descripción    | Descripción del rol. |
| Access         | ReadWrite                  |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows 2000               |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del rol. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                                                                      |
| Predeterminado        | "Nuevo rol"                                                                                                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
