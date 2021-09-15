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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568489"
---
# <a name="eventclassesforiid-collection"></a>Colección EventClassesForIID

Recupera información relacionada con las clases de eventos.

La conexión entre el publicador y los suscriptores se administra mediante un objeto [**EventClass,**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) que es un componente COM+ que contiene las interfaces y los métodos usados por un publicador para activa eventos.

Esta colección admite los [**métodos Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**y Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del [**objeto COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Members

La **colección EventClassesForIID** hereda de la [**interfaz IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección a cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las siguientes colecciones:

-   [**Raíz**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) de la colección admite las siguientes propiedades:

-   [Aplicación](#application)
-   [Bitness](#bitness)
-   [CLSID](#clsid)
-   [Descripción](#description)
-   [IsPrivateComponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>Application



| Entrada | Value |
|----------------|----------------------------------------------------------|
| Descripción    | GUID de la aplicación que contiene la clase de eventos . |
| Acceso         | ReadOnly                                                 |
| Tipo           | String                                                   |
| Predeterminado        | N/D                                                      |
| Sistema mínimo | Windows XP                                               |



 

### <a name="bitness"></a>Valor de bits



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Representa el tipo de bits binario de la clase de eventos. En sistemas que usan componentes de 64 Windows, esta propiedad distingue entre componentes de 64 bits y componentes de 32 bits. |
| Acceso         | ReadOnly                                                                                                                                                                |
| Tipo           | Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)                                                                                           |
| Valor predeterminado        | N/D                                                                                                                                                                     |
| Sistema mínimo | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID de la clase de eventos. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) de propiedad Key en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                      |
| Tipo           | String                                                                                                                                                        |
| Predeterminado        | N/D                                                                                                                                                           |
| Sistema mínimo | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>Descripción



| Entrada | Value |
|----------------|----------------------------|
| Descripción    | Describe la clase de eventos . |
| Acceso         | ReadOnly                   |
| Tipo           | String                     |
| Predeterminado        | ""                         |
| Sistema mínimo | Windows XP                 |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Entrada | Value |
|----------------|---------------------------------------------------------|
| Descripción    | Indica si el componente de la clase de eventos es privado. |
| Acceso         | ReadOnly                                                |
| Tipo           | Bool                                                    |
| Valor predeterminado        | False                                                   |
| Sistema mínimo | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre descriptivo que se usa para identificar la clase de eventos. Esta propiedad se devuelve cuando se llama [**al método**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) de propiedad Name en un objeto de esta colección. |
| Acceso         | ReadOnly                                                                                                                                                                            |
| Tipo           | String                                                                                                                                                                              |
| Predeterminado        | ""                                                                                                                                                                                  |
| Sistema mínimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
