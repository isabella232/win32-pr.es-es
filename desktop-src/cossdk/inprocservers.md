---
description: Contiene una lista de los servidores en proceso registrados con el sistema. Contiene un objeto para cada componente que se registra como un servidor en proceso.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Colección InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714795"
---
# <a name="inprocservers-collection"></a>Colección InprocServers

Contiene una lista de los servidores en proceso registrados con el sistema. Contiene un objeto para cada componente que se registra como un servidor en proceso.

Esta colección admite el método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , pero no el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) . Para instalar o importar componentes en una aplicación, use métodos en el objeto [**COMAdminCatalog**](comadmincatalog.md) .

## <a name="members"></a>Miembros

La colección **InprocServers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="related-collections"></a>Colecciones relacionadas

Puede navegar desde esta colección hasta cualquiera de las siguientes colecciones:

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Puede navegar a esta colección desde las colecciones siguientes:

-   [**Raíces**](root.md)

## <a name="properties"></a>Propiedades

El objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) admite las siguientes propiedades en la colección:

-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [ProgID](#progid)

### <a name="clsid"></a>CLSID



| Entrada | Value |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | GUID del componente. Esta propiedad se devuelve cuando se llama al método de propiedad de [**clave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                  |
| Tipo           | String                                                                                                                                                    |
| Predeterminado        | N/D                                                                                                                                                       |
| Sistema mínimo | Windows 2000                                                                                                                                              |



 

### <a name="inprocserver32"></a>InprocServer32



| Entrada | Value |
|----------------|----------------------------------|
| Descripción    | Ruta de acceso de archivo para el componente. |
| Access         | ReadOnly                         |
| Tipo           | String                           |
| Predeterminado        | N/D                              |
| Sistema mínimo | Windows 2000                     |



 

### <a name="progid"></a>ProgID



| Entrada | Value |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción    | Nombre que identifica el componente. Esta propiedad se devuelve cuando se llama al método de la propiedad [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) en un objeto de esta colección. |
| Access         | ReadOnly                                                                                                                                                            |
| Tipo           | String                                                                                                                                                              |
| Predeterminado        | N/D                                                                                                                                                                 |
| Sistema mínimo | Windows 2000                                                                                                                                                        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Colecciones de administración de COM+](com--administration-collections.md)
</dt> </dl>

 

 
