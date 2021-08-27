---
description: Contiene un objeto para cada suscripción de la colección components primaria.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: Colección SubscriptionsForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8c07162fc20788545b38b8fae4be245b9a1ebbff
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886196"
---
# <a name="subscriptionsforcomponent-collection"></a>Colección SubscriptionsForComponent

Contiene un objeto para cada suscripción de la colección [**components**](components.md) primaria.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección SubscriptionsForComponent** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**PublisherProperties**](publisherproperties.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**SubscriberProperties**](subscriberproperties.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Componentes**](components.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Descripción](#description)
-   [Habilitado](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [ID](#subscriptionsforcomponent-collection)
-   [InterfaceID](#interfaceid)
-   [MachineName](#machinename)
-   [MethodName](#methodname)
-   [Nombre](#machinename)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [En cola](#queued)
-   [SubscriberMoniker](#subscribermoniker)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descripción



| Entrada | Valor |
|----------------|-------------------------------------|
| Descripción    | Descripción de la suscripción. |
| Access         | ReadWrite                           |
| Tipo           | String                              |
| Predeterminado        | ""                                  |
| Sistema mínimo | Windows 2000                        |



 

### <a name="enabled"></a>habilitado



| Entrada | Valor |
|----------------|----------------------------------------------------------|
| Descripción    | Indica si la suscripción está habilitada actualmente. |
| Access         | ReadWrite                                                |
| Tipo           | Bool                                                     |
| Valor predeterminado        | True                                                     |
| Sistema mínimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos, se usa para representar el GUID del identificador de partición que contiene la clase de evento. Al suscribirse a clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en una partición diferente. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                                                             |
| Predeterminado        | NULL                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrada | Valor |
|----------------|----------------------------------------------------------------------------------------------|
| Descripción    | CLSID de la clase de eventos. Puede indicar un EventCLSID o publisherID, pero no ambos. |
| Access         | WriteOnce                                                                                    |
| Tipo           | String                                                                                       |
| Predeterminado        | N/D                                                                                          |
| Sistema mínimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena que indica los criterios de filtro. Puede ser un CLSID para una [**clase PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Access         | ReadWrite                                                                                                        |
| Tipo           | String                                                                                                           |
| Predeterminado        | N/D                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                     |



 

### <a name="id"></a>ID



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador de la suscripción. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                        |
| Tipo           | String                                                                                                                                                           |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrada | Valor |
|----------------|------------------------------------------|
| Descripción    | El IID de la interfaz a la que se ha suscrito. |
| Access         | ReadWrite                                |
| Tipo           | String                                   |
| Predeterminado        | N/D                                      |
| Sistema mínimo | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Entrada | Valor |
|----------------|---------------------------------------------------------------------------------|
| Descripción    | Nombre de equipo remoto para suscripciones a clases de eventos en un equipo remoto. |
| Access         | ReadWrite                                                                       |
| Tipo           | String                                                                          |
| Predeterminado        | ""                                                                              |
| Sistema mínimo | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Entrada | Valor |
|----------------|----------------------------------------------|
| Descripción    | Método en la interfaz a la que se va a suscribir. |
| Access         | ReadWrite                                    |
| Tipo           | String                                       |
| Predeterminado        | N/D                                          |
| Sistema mínimo | Windows 2000                                 |



 

### <a name="name"></a>Nombre



| Entrada | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la suscripción. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                                             |
| Predeterminado        | "Nueva suscripción"                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------|
| Descripción    | Indica si la suscripción solo se aplica a un usuario determinado, UserName. |
| Access         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Valor predeterminado        | False                                                                       |
| Sistema mínimo | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| Descripción    | Identificador del publicador. Puede indicar un EventCLSID o publisherID, pero no ambos. |
| Access         | WriteOnce                                                                               |
| Tipo           | String                                                                                  |
| Predeterminado        | ""                                                                                      |
| Sistema mínimo | Windows 2000                                                                            |



 

### <a name="queued"></a>En cola



| Entrada | Valor |
|----------------|-----------------------------------------------|
| Descripción    | Indica si la suscripción está en cola. |
| Access         | ReadWrite                                     |
| Tipo           | Bool                                          |
| Valor predeterminado        | False                                         |
| Sistema mínimo | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| Descripción    | Moniker para un suscriptor marcado como En cola. Se genera un valor predeterminado cuando Queued se establece inicialmente en True. |
| Access         | ReadWrite                                                                                                       |
| Tipo           | String                                                                                                          |
| Predeterminado        | N/D                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrada | Valor |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos en la misma partición, se usa para representar el GUID del identificador de partición del suscriptor. Al suscribirse a clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en una partición diferente. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Tipo           | String                                                                                                                                                                                                                                                          |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrada | Valor |
|----------------|--------------------------------------------------------------------------|
| Descripción    | Nombre del usuario al que se aplica la suscripción, cuando PerUser es True. |
| Access         | ReadWrite                                                                |
| Tipo           | String                                                                   |
| Predeterminado        | N/D                                                                      |
| Sistema mínimo | Windows 2000                                                             |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
