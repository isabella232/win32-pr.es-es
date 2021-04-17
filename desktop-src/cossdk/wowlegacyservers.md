---
description: Las propiedades expuestas de la colección WOWLegacyServers están diseñadas para ser idénticas a la colección LegacyServers, salvo que la colección WOWLegacyServers se extrae del registro de 32 bits en equipos de 64 bits.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Colección WOWLegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705285"
---
# <a name="wowlegacyservers-collection"></a>Colección WOWLegacyServers

Las propiedades expuestas de la colección **WOWLegacyServers** están diseñadas para ser idénticas a la colección [**LegacyServers**](legacyservers.md) , salvo que la colección **WOWLegacyServers** se extrae del registro de 32 bits en equipos de 64 bits.

Esta colección no admite los métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) y [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Miembros

La colección **WOWLegacyServers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Entrada | Value |
|----------------|------------------------|
| Descripción    | Nombre de la clase. |
| Access         | ReadOnly               |
| Tipo           | String                 |
| Predeterminado        | N/D                    |
| Sistema mínimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID del componente. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Value |
|----------------|----------------------------------|
| Descripción    | Ruta de acceso de archivo para el componente. |
| Access         | ReadOnly                         |
| Tipo           | String                           |
| Predeterminado        | N/D                              |
| Sistema mínimo | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Entrada | Value |
|----------------|---------------------------------------------------------------|
| Descripción    | Especifica la ruta de acceso completa a una aplicación de servidor local de 32 bits. |
| Access         | ReadOnly                                                      |
| Tipo           | String                                                        |
| Predeterminado        | N/D                                                           |
| Sistema mínimo | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre que identifica el componente. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                            |
| Tipo           | String                                                                                                                                                              |
| Predeterminado        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
