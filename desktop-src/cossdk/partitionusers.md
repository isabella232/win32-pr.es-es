---
description: Contiene un objeto para cada usuario de partición.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Colección PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965135"
---
# <a name="partitionusers-collection"></a>Colección PartitionUsers

Contiene un objeto para cada usuario de partición.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección PartitionUsers** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [AccountName](#accountname)
-   [DefaultPartitionID](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la cuenta del usuario de la partición. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                                                                    |
| Tipo           | String                                                                                                                                                                                                       |
| Predeterminado        | "Nuevo usuario"                                                                                                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>DefaultPartitionID



| Entrada | Value |
|----------------|--------------------------------------------------------------------|
| Descripción    | Identificador único global de la partición de aplicación base. |
| Acceso         | ReadWrite                                                          |
| Tipo           | String                                                             |
| Predeterminado        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| Sistema mínimo | Windows Server 2003                                                |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
