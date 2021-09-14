---
description: Contiene un objeto para cada rol asignado al componente al que está relacionada la colección. Los roles ya deben estar asignados en el nivel de aplicación.
ms.assetid: c253c72f-908e-4990-ac1a-27e32c99283c
title: Colección RolesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 701921f8f88656753857707c045da0c8e231e1a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973508"
---
# <a name="rolesforcomponent-collection"></a>Colección RolesForComponent

Contiene un objeto para cada rol asignado al componente al que está relacionada la colección. Los roles ya deben estar asignados en el nivel de aplicación.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección RolesForComponent** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Componentes**](components.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [Nombre](#name)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del rol. Ya debe ser un rol asignado a la aplicación (que aparece en la colección Roles). Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                                                                                                                                                                                                           |
| Tipo           | String                                                                                                                                                                                                                                                                                                                                              |
| Predeterminado        | "Nuevo rol"                                                                                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
