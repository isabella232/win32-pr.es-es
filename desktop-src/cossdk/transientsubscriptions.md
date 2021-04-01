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
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907308"
---
# <a name="transientsubscriptions-collection"></a>Colección TransientSubscriptions

Contiene un objeto para cada suscripción transitoria. Las suscripciones transitorias se pueden crear sobre la marcha para ejecutar instancias de objeto y desaparecen cuando se destruye el objeto.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **TransientSubscriptions** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientPublisherProperties**](transientpublisherproperties.md)
-   [**TransientSubscriberProperties**](transientsubscriberproperties.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Descripción](#description)
-   [Enabled](#enabled)
-   [EventClassPartitionID](#eventclasspartitionid)
-   [EventCLSID](#eventclsid)
-   [FilterCriteria](#filtercriteria)
-   [Id](#transientsubscriptions-collection)
-   [InterfaceID](#interfaceid)
-   [MethodName](#methodname)
-   [Nombre](#methodname)
-   [Perusuario](#peruser)
-   [PublisherID](#publisherid)
-   [SubscriberInterface](#subscriberinterface)
-   [SubscriberPartitionID](#subscriberpartitionid)
-   [UserName](#username)

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|-------------------------------------|
| Descripción    | Una descripción de la suscripción. |
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
| Valor predeterminado        | True                                                     |
| Sistema mínimo | Windows 2000                                             |



 

### <a name="eventclasspartitionid"></a>EventClassPartitionID



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Al suscribirse a una clase de eventos, se usa para representar el GUID del identificador de la partición que contiene la clase de eventos. Al suscribirse a las clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en otra diferente. |
| Access         | ReadWrite                                                                                                                                                                                                                                          |
| Tipo           | String                                                                                                                                                                                                                                             |
| Predeterminado        | NULL                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a>EventCLSID



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------|
| Descripción    | El CLSID de la clase de evento. Puede indicar un EventCLSID o un PublisherID, pero no ambos. |
| Access         | WriteOnce                                                                                    |
| Tipo           | String                                                                                       |
| Predeterminado        | N/D                                                                                          |
| Sistema mínimo | Windows 2000                                                                                 |



 

### <a name="filtercriteria"></a>FilterCriteria



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| Descripción    | Cadena que indica los criterios de filtro. Puede ser un CLSID para una clase [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) . |
| Access         | ReadWrite                                                                                                            |
| Tipo           | String                                                                                                               |
| Predeterminado        | N/D                                                                                                                  |
| Sistema mínimo | Windows 2000                                                                                                         |



 

### <a name="id"></a>id



| Entrada | Value |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Identificador de la suscripción. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | WriteOnce                                                                                                                                                        |
| Tipo           | String                                                                                                                                                           |
| Predeterminado        | <Generated>                                                                                                                                                |
| Sistema mínimo | Windows 2000                                                                                                                                                     |



 

### <a name="interfaceid"></a>InterfaceID



| Entrada | Value |
|----------------|----------------------------------|
| Descripción    | IID de la interfaz suscrita a. |
| Access         | WriteOnce                        |
| Tipo           | String                           |
| Predeterminado        | N/D                              |
| Sistema mínimo | Windows 2000                     |



 

### <a name="methodname"></a>MethodName



| Entrada | Value |
|----------------|----------------------------------------------|
| Descripción    | Método de la interfaz a la que se suscribe. |
| Access         | ReadWrite                                    |
| Tipo           | String                                       |
| Predeterminado        | N/D                                          |
| Sistema mínimo | Windows 2000                                 |



 

### <a name="name"></a>Nombre



| Entrada | Value |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre de la suscripción. Se quitan los espacios adicionales al principio y al final de la cadena. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadWrite                                                                                                                                                                                                                              |
| Tipo           | String                                                                                                                                                                                                                                 |
| Predeterminado        | "Nueva suscripción"                                                                                                                                                                                                                     |
| Sistema mínimo | Windows 2000                                                                                                                                                                                                                           |



 

### <a name="peruser"></a>Perusuario



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------|
| Descripción    | Indica si la suscripción se aplica solo a un usuario determinado, representado por la propiedad UserName. |
| Access         | ReadWrite                                                                                               |
| Tipo           | Bool                                                                                                    |
| Valor predeterminado        | False                                                                                                   |
| Sistema mínimo | Windows 2000                                                                                            |



 

### <a name="publisherid"></a>PublisherID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------|
| Descripción    | ID. del publicador. Puede indicar un EventCLSID o un PublisherID, pero no ambos. |
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
| Descripción    | Al suscribirse a una clase de eventos en la misma partición, se usa para representar el GUID del ID. de partición del suscriptor. Al suscribirse a las clases de eventos, el suscriptor tiene la opción de suscribirse a una clase de eventos en la misma partición o en otra diferente. |
| Access         | WriteOnce                                                                                                                                                                                                                                                       |
| Tipo           | String                                                                                                                                                                                                                                                          |
| Predeterminado        | <Generated>                                                                                                                                                                                                                                               |
| Sistema mínimo | Windows Server 2003                                                                                                                                                                                                                                             |



 

### <a name="username"></a>UserName



| Entrada | Value |
|----------------|-------------------------------------------------------------------------|
| Descripción    | Nombre del usuario al que se aplica la suscripción cuando peruser es true. |
| Access         | ReadWrite                                                               |
| Tipo           | String                                                                  |
| Predeterminado        | N/D                                                                     |
| Sistema mínimo | Windows 2000                                                            |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
