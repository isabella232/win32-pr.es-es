---
description: Contiene un objeto para cada suscripción transitoria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Colección TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5053a4fd488ed38a637b4296f94caf20887f3ed924ae6d11b8f6a242669eccad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853935"
---
# <a name="transientsubscriptions-collection"></a>Colección TransientSubscriptions

Contiene un objeto para cada suscripción transitoria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Miembros

La **colección TransientSubscriptions** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientPublisherProperties**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades dentro de la colección:

-   [Descripción](#description)
-   [Habilitado](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [Id](#transientsubscriptions-collection)
-   [InterfaceID](#interfaceid)
-   [MethodName](#methodname)
-   [Nombre](#methodname)
-   [PerUser](#peruser)
-   [PublisherID](#publisherid)
-   [SubscriberInterface](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | Descripción de la suscripción. |
| Access         | ReadWrite                           |
| Tipo           | String                              |
| Predeterminado        | ""                                  |
| Sistema mínimo | Windows 2000                        |



 

### <a name="enabled"></a>habilitado



| Entrada | Value |
|----------------|----------------------------------------------------------|
| Descripción    | Indica si la suscripción está habilitada actualmente. |
| Access         | ReadWrite                                                |
| Tipo           | Bool                                                     |
| Valor predeterminado        | Verdadero                                                     |
| Sistema mínimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos, se usa para representar el GUID del identificador de partición que contiene la clase de evento. Al suscribirse a clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de evento en la misma partición o en una partición diferente. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                                                             |
| Predeterminado        | NULL                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------|
| Descripción    | CLSID de la clase de eventos. Puede indicar un EventCLSID o publisherID, pero no ambos. |
| Access         | WriteOnce                                                                                    |
| Tipo           | String                                                                                       |
| Predeterminado        | N/D                                                                                          |
| Sistema mínimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena que indica los criterios de filtro. Puede ser un CLSID para una [**clase PublisherFilter.**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) |
| Access         | ReadWrite                                                                                                            |
| Tipo           | String                                                                                                               |
| Predeterminado        | N/D                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                         |



 

### <a name="id"></a>ID



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador de la suscripción. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                        |
| Tipo           | String                                                                                                                                                           |
| Predeterminado        | <Generated>                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrada | Value |
|----------------|----------------------------------|
| Descripción    | IID de la interfaz a la que se ha suscrito. |
| Access         | WriteOnce                        |
| Tipo           | String                           |
| Predeterminado        | N/D                              |
| Sistema mínimo | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Entrada | Value |
|----------------|----------------------------------------------|
| Descripción    | Método en la interfaz a la que se va a suscribir. |
| Access         | ReadWrite                                    |
| Tipo           | String                                       |
| Predeterminado        | N/D                                          |
| Sistema mínimo | Windows 2000                                 |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la suscripción. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva suscripción"                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>PerUser



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si la suscripción solo se aplica a un usuario determinado, representado por la propiedad UserName. |
| Access         | ReadWrite                                                                                               |
| Tipo           | Bool                                                                                                    |
| Valor predeterminado        | False                                                                                                   |
| Sistema mínimo | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------|
| Descripción    | Identificador del publicador. Puede indicar un EventCLSID o publisherID, pero no ambos. |
| Access         | WriteOnce                                                                           |
| Tipo           | String                                                                              |
| Predeterminado        | ""                                                                                  |
| Sistema mínimo | Windows 2000                                                                        |



 

### <a name="subscriberinterface"></a>SubscriberInterface



| Entrada | Value |
|----------------|------------------------------------------|
| Descripción    | Puntero a la interfaz del suscriptor. |
| Access         | ReadWrite                                |
| Tipo           | Variante                                  |
| Valor predeterminado        | N/D                                      |
| Sistema mínimo | Windows 2000                             |



 

### <a name="subscriberpartitionid"></a>SubscriberPartitionID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos en la misma partición, se usa para representar el GUID del identificador de partición del suscriptor. Al suscribirse a clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en una partición diferente. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Tipo           | String                                                                                                                                                                                                                                                          |
| Predeterminado        | <Generated>                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrada | Value |
|----------------|-------------------------------------------------------------------------|
| Descripción    | Nombre del usuario al que se aplica la suscripción cuando PerUser es True. |
| Access         | ReadWrite                                                               |
| Tipo           | String                                                                  |
| Predeterminado        | N/D                                                                     |
| Sistema mínimo | Windows 2000                                                            |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
