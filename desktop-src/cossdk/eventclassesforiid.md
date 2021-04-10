---
description: Recupera información relacionada con las clases de eventos.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Colección EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153025"
---
# <a name="eventclassesforiid-collection"></a>Colección EventClassesForIID

Recupera información relacionada con las clases de eventos.

La conexión entre el publicador y el suscriptor se administra mediante un objeto [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , que es un componente com+ que contiene las interfaces y los métodos utilizados por un publicador para activar los eventos.

Esta colección admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **EventClassesForIID** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [Aplicación](#application)
-   [Bits](#bitness)
-   [CLSID](#clsid)
-   [Descripción](#description)
-   [IsPrivateComponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>Application



| Entrada | Value |
|----------------|----------------------------------------------------------|
| Descripción    | GUID de la aplicación que contiene la clase de eventos. |
| Access         | ReadOnly                                                 |
| Tipo           | String                                                   |
| Predeterminado        | N/D                                                      |
| Sistema mínimo | Windows XP                                               |



 

### <a name="bitness"></a>Valor de bits



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el tipo de bits binario de la clase de evento. En los sistemas que usan Windows de 64 bits, esta propiedad distingue entre los componentes de 64 bits y los componentes de 32 bits. |
| Access         | ReadOnly                                                                                                                                                                |
| Tipo           | Valores posibles largos: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)                                                                                           |
| Valor predeterminado        | N/D                                                                                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID para la clase de evento. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                      |
| Tipo           | String                                                                                                                                                        |
| Predeterminado        | N/D                                                                                                                                                           |
| Sistema mínimo | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------|
| Descripción    | Describe la clase de eventos. |
| Access         | ReadOnly                   |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows XP                 |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrada | Value |
|----------------|---------------------------------------------------------|
| Descripción    | Indica si el componente de clase de eventos es privado. |
| Access         | ReadOnly                                                |
| Tipo           | Bool                                                    |
| Valor predeterminado        | False                                                   |
| Sistema mínimo | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre descriptivo que se usa para identificar la clase de eventos. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                              |
| Predeterminado        | ""                                                                                                                                                                                  |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
