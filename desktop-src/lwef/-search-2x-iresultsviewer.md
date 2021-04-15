---
title: Interfaz IResultsViewer (WdsSharedIDL. h)
description: Expone métodos y propiedades para la vista de resultados.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Interfaz IResultsViewer características del entorno heredado de Windows
- Interfaz IResultsViewer características del entorno heredado de Windows, descritas
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534510"
---
# <a name="iresultsviewer-interface"></a>Interfaz IResultsViewer

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar. 

Expone métodos y propiedades para la vista de resultados.

## <a name="members"></a>Miembros

La interfaz **IResultsViewer** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultsViewer** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IResultsViewer** tiene estos métodos.



| Método                                                   | Descripción                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Goback**](-search-2x-iresultsviewer-goback.md)       | Sin implementar.<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | Sin implementar.<br/>                                                            |
| [**Actualizaciones**](-search-2x-iresultsviewer-refresh.md)     | Sin implementar.<br/>                                                            |
| [**Stop**](-search-2x-iresultsviewer-stop.md)           | Sin implementar.<br/>                                                            |
| [**Update**](-search-2x-iresultsviewer-update.md)       | Aplica cualquier cambio en la consulta y navega por la vista al nuevo conjunto de resultados.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IResultsViewer** tiene estas propiedades.



| Propiedad                                                                            | Tipo de acceso           | Descripción                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Contenido**](-search-2x-iresultsviewer-contents.md)<br/>                   | Solo escritura<br/> | Esta propiedad realiza un seguimiento del tipo de contenido que se muestra en la vista de resultados. <br/>    |
| [**DisplayName**](-search-2x-iresultsviewer-displayname.md)<br/>             | Solo lectura<br/>  | Nombre para mostrar localizado del tipo.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Solo escritura<br/> | Sin implementar.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lectura/escritura<br/> | Esta propiedad establece o devuelve el nombre del tipo preceived por el que se van a filtrar los resultados.<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lectura/escritura<br/> | Estilo del encabezado que se muestra en la vista.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Solo escritura<br/> | Esto devuelve TRUE si se ha modificado la consulta views y necesita actualizarse. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lectura/escritura<br/> | Esta propiedad establece o devuelve el nombre del almacén en el que se van a filtrar los resultados.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lectura/escritura<br/> | Controla el modo de presentación del panel de vista previa.<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Solo escritura<br/> | Al llamar a la colección de filtros de propiedades, devolverá lo siguiente:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el texto de la consulta actual.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Solo escritura<br/> | Sin implementar.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lectura/escritura<br/> | Esta propiedad establece o devuelve el orden de las columnas por las que se van a ordenar los resultados. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lectura/escritura<br/> | Esta propiedad establece o devuelve el IndexColumn de la propiedad por la que se van a ordenar los resultados. <br/> |



 

## <a name="remarks"></a>Observaciones

Estos métodos y propiedades se usan para manipular la información que se ve.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 con \[ solo aplicaciones de escritorio de SP1\]<br/>                             |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>                                               |
| Encabezado<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

