---
description: 'Colección UsersInPartitionRole: contiene un objeto para cada usuario del rol al que está relacionada la colección.'
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Colección UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: d07c62fc6c6cc871f803b1f752201bd500e2705c3cfca272ff350ffd018f6018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499655"
---
# <a name="usersinpartitionrole-collection"></a>Colección UsersInPartitionRole

Contiene un objeto para cada usuario del rol con el que está relacionada la colección.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección UsersInPartitionRole** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [User](#usersinpartitionrole-collection)

### <a name="user"></a>Usuario



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de usuario. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                                             |
| Tipo           | String                                                                                                                                                                                |
| Predeterminado        | "Nuevo usuario"                                                                                                                                                                            |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
