---
description: Contiene una lista de los equipos servidor del clúster de aplicaciones. Contiene un objeto para cada servidor.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Colección ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 852f6f04147489336622a5c13e447bcb4fbfd7e20f580edcb5da8bdfadaa5e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991955"
---
# <a name="applicationcluster-collection"></a>Colección ApplicationCluster

Contiene una lista de los equipos servidor del clúster de aplicaciones. Contiene un objeto para cada servidor. Se trata de una colección de nivel superior.

El clúster de aplicaciones se define para fines del servicio de equilibrio de carga de componentes (CLB). Para que se utilice la colección de clústeres de aplicaciones, el servicio CLB debe estar instalado en el equipo.

Designa un enrutador en el clúster de aplicaciones con la propiedad IsRouter en el objeto de colección [**LocalComputer**](localcomputer.md) y designa que un componente determinado debe equilibrar la carga con la propiedad LoadBalancingSupported en un objeto de colección [**Components.**](components.md)

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección ApplicationCluster** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Nombre](#name)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre del servidor. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                                                                                                               |
| Predeterminado        | "Nuevo equipo"                                                                                                                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
