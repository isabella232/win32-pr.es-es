---
description: Contiene una lista de los protocolos que va a utilizar DCOM. Contiene un objeto para cada protocolo.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Colección DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496163"
---
# <a name="dcomprotocols-collection"></a>Colección DCOMProtocols

Contiene una lista de los protocolos que va a utilizar DCOM. Contiene un objeto para cada protocolo.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **DCOMProtocols** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Nombre](#name)
-   [Pedido](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre del protocolo Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                   |
| Tipo           | String                                                                                                                                                      |
| Predeterminado        | "Nuevo protocolo"                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Pedido



| Entrada | Value |
|----------------|-----------------------------------------|
| Descripción    | El orden en el que se va a probar el protocolo. |
| Access         | ReadWrite                               |
| Tipo           | Long (0-65000)                          |
| Valor predeterminado        | 0                                       |
| Sistema mínimo | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Código que especifica la secuencia de protocolo RPC. Entre los códigos de protocolo admitidos se incluyen los siguientes: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                                                                                      |
| Predeterminado        | ""                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
