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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361639"
---
# <a name="subscriptionsforcomponent-collection"></a>Colección SubscriptionsForComponent

Contiene un objeto para cada suscripción de la colección [**components**](components.md) primaria.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

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
-   [Enabled](#enabled)
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



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | Descripción de la suscripción. |
| Acceso         | ReadWrite                           |
| Tipo           | String                              |
| Predeterminado        | ""                                  |
| Sistema mínimo | Windows 2000                        |



 

### <a name="enabled"></a>habilitado



| Entrada | Value |
|----------------|----------------------------------------------------------|
| Descripción    | Indica si la suscripción está habilitada actualmente. |
| Acceso         | ReadWrite                                                |
| Tipo           | Bool                                                     |
| Valor predeterminado        | True                                                     |
| Sistema mínimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos, se usa para representar el GUID del identificador de partición que contiene la clase de evento. Al suscribirse a clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en una partición diferente. |
| Acceso         | ReadWrite                                                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                                                             |
| Predeterminado        | NULL                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------|
| Descripción    | CLSID de la clase de eventos. Puede indicar un EventCLSID o publisherID, pero no ambos. |
| Acceso         | WriteOnce                                                                                    |
| Tipo           | String                                                                                       |
| Predeterminado        | N/D                                                                                          |
| Sistema mínimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena que indica los criterios de filtro. Puede ser un CLSID para una [**clase PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Acceso         | ReadWrite                                                                                                        |
| Tipo           | String                                                                                                           |
| Predeterminado        | N/D                                                                                                              |
| Sistema mínimo | Windows 2000                                                                                                     |



 

### <a name="id"></a>id



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador de la suscripción. Esta propiedad se devuelve cuando se llama al método de propiedad [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Acceso         | WriteOnce                                                                                                                                                        |
| Tipo           | String                                                                                                                                                           |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrada | Value |
|----------------|------------------------------------------|
| Descripción    | El IID de la interfaz a la que se suscribió. |
| Acceso         | ReadWrite                                |
| Tipo           | String                                   |
| Predeterminado        | N/D                                      |
| Sistema mínimo | Windows 2000                             |



 

### <a name="machinename"></a>MachineName



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------|
| Descripción    | Nombre de equipo remoto para las suscripciones a clases de eventos en un equipo remoto. |
| Acceso         | ReadWrite                                                                       |
| Tipo           | String                                                                          |
| Predeterminado        | ""                                                                              |
| Sistema mínimo | Windows 2000                                                                    |



 

### <a name="methodname"></a>MethodName



| Entrada | Value |
|----------------|----------------------------------------------|
| Descripción    | Método en la interfaz a la que se va a suscribir. |
| Acceso         | ReadWrite                                    |
| Tipo           | String                                       |
| Predeterminado        | N/D                                          |
| Sistema mínimo | Windows 2000                                 |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la suscripción. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se [**llama al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadWrite                                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                                             |
| Predeterminado        | "Nueva suscripción"                                                                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                       |



 

### <a name="peruser"></a>PerUser



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------|
| Descripción    | Indica si la suscripción solo se aplica a un usuario determinado, UserName. |
| Acceso         | ReadWrite                                                                   |
| Tipo           | Bool                                                                        |
| Valor predeterminado        | False                                                                       |
| Sistema mínimo | Windows 2000                                                                |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------|
| Descripción    | Identificador del publicador. Puede indicar un EventCLSID o publisherID, pero no ambos. |
| Acceso         | WriteOnce                                                                               |
| Tipo           | String                                                                                  |
| Predeterminado        | ""                                                                                      |
| Sistema mínimo | Windows 2000                                                                            |



 

### <a name="queued"></a>En cola



| Entrada | Value |
|----------------|-----------------------------------------------|
| Descripción    | Indica si la suscripción está en cola. |
| Acceso         | ReadWrite                                     |
| Tipo           | Bool                                          |
| Valor predeterminado        | False                                         |
| Sistema mínimo | Windows 2000                                  |



 

### <a name="subscribermoniker"></a>SubscriberMoniker



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| Descripción    | Moniker para un suscriptor marcado como En cola. Se genera un valor predeterminado cuando Queued se establece inicialmente en True. |
| Acceso         | ReadWrite                                                                                                       |
| Tipo           | String                                                                                                          |
| Predeterminado        | N/D                                                                                                             |
| Sistema mínimo | Windows 2000                                                                                                    |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos en la misma partición, se usa para representar el GUID del identificador de partición del suscriptor. Al suscribirse a clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en una partición diferente. |
| Acceso         | WriteOnce                                                                                                                                                                                                                                                       |
| Tipo           | String                                                                                                                                                                                                                                                          |
| Predeterminado        | &lt;Generado&gt;                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrada | Value |
|----------------|--------------------------------------------------------------------------|
| Descripción    | Nombre del usuario al que se aplica la suscripción, cuando PerUser es True. |
| Acceso         | ReadWrite                                                                |
| Tipo           | String                                                                   |
| Predeterminado        | N/D                                                                      |
| Sistema mínimo | Windows 2000                                                             |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
