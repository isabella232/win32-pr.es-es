---
description: La colección Roles siempre está relacionada con un objeto de la colección Applications. Contiene un objeto para cada rol asignado a la aplicación a la que está relacionado.
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
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973513"
---
# <a name="roles-collection"></a>Colección de roles

La **colección Roles** siempre está relacionada con un objeto de la colección [**Applications.**](applications.md) Contiene un objeto para cada rol asignado a la aplicación a la que está relacionado.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección Roles** hereda de la interfaz [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Aplicaciones**](applications.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Descripción](#description)
-   [Nombre](#name)

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------|
| Descripción    | Descripción del rol. |
| Acceso         | ReadWrite                  |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows 2000               |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del rol. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                                                                      |
| Predeterminado        | "Nuevo rol"                                                                                                                                                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
