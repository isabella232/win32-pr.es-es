---
description: Contiene una lista de los protocolos que DCOM va a usar. Contiene un objeto para cada protocolo.
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
ms.openlocfilehash: f387c9ba1d46b99c44a3d6616df95f7b6f9cece959a943b63ed12ce6fe8af900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548024"
---
# <a name="dcomprotocols-collection"></a>Colección DCOMProtocols

Contiene una lista de los protocolos que DCOM va a usar. Contiene un objeto para cada protocolo.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección DCOMProtocols** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

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
-   [Pedido](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | El nombre del protocolo Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadWrite                                                                                                                                                   |
| Tipo           | String                                                                                                                                                      |
| Predeterminado        | "Nuevo protocolo"                                                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Pedido



| Entrada | Value |
|----------------|-----------------------------------------|
| Descripción    | Orden en el que se va a probar el protocolo. |
| Acceso         | ReadWrite                               |
| Tipo           | Long (0-65000)                          |
| Valor predeterminado        | 0                                       |
| Sistema mínimo | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Código que especifica la secuencia del protocolo RPC. Los códigos de protocolo admitidos incluyen lo siguiente: ncacn \_ ip \_ tcp, ncacn \_ http, ncacn \_ spx. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                                                                                                                                   |
| Tipo           | String                                                                                                                                                                                                                                                                      |
| Predeterminado        | ""                                                                                                                                                                                                                                                                          |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
