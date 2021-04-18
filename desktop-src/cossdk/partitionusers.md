---
description: Contiene un objeto para cada usuario de la partición.
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705361"
---
# <a name="partitionusers-collection"></a>Colección PartitionUsers

Contiene un objeto para cada usuario de la partición.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **PartitionUsers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [AccountName](#accountname)
-   [DefaultPartitionID](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Entrada | Value |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la cuenta del usuario de la partición. Esta propiedad se devuelve cuando se llama al método de propiedad [**key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                    |
| Tipo           | String                                                                                                                                                                                                       |
| Predeterminado        | "Nuevo usuario"                                                                                                                                                                                                   |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>DefaultPartitionID



| Entrada | Value |
|----------------|--------------------------------------------------------------------|
| Descripción    | Identificador único global de la partición de aplicación base. |
| Access         | ReadWrite                                                          |
| Tipo           | String                                                             |
| Predeterminado        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| Sistema mínimo | Windows Server 2003                                                |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
