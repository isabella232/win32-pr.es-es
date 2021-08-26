---
title: Interfaz IResultsViewer (WdsSharedIDL.h)
description: Expone métodos y propiedades para la vista de resultados.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- IResultsViewer interface Legacy Windows Environment Features
- IResultsViewer interface Legacy Windows Environment Features , descrito
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
ms.openlocfilehash: c1528f5d6da779e49836b75027845d40c76a2d948a9eb51e78b2addcefc75085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963775"
---
# <a name="iresultsviewer-interface"></a>Interfaz IResultsViewer

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la API [Windows Search en](../search/-search-reference-entry-page.md) su lugar. 

Expone métodos y propiedades para la vista de resultados.

## <a name="members"></a>Miembros

La **interfaz IResultsViewer** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultsViewer** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IResultsViewer** tiene estos métodos.



| Método                                                   | Descripción                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Goback**](-search-2x-iresultsviewer-goback.md)       | Sin implementar.<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | Sin implementar.<br/>                                                            |
| [**Actualizar**](-search-2x-iresultsviewer-refresh.md)     | Sin implementar.<br/>                                                            |
| [**Stop**](-search-2x-iresultsviewer-stop.md)           | Sin implementar.<br/>                                                            |
| [**Actualizar**](-search-2x-iresultsviewer-update.md)       | Aplica los cambios de consulta y navega por la vista hasta el nuevo conjunto de resultados.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IResultsViewer** tiene estas propiedades.



| Propiedad                                                                            | Tipo de acceso           | Descripción                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Contenido**](-search-2x-iresultsviewer-contents.md)<br/>                   | Solo escritura<br/> | Esta propiedad realiza un seguimiento del tipo de contenido que se muestra en la vista de resultados. <br/>    |
| [**Displayname**](-search-2x-iresultsviewer-displayname.md)<br/>             | Solo lectura<br/>  | Nombre para mostrar localizado del tipo.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Solo escritura<br/> | Sin implementar.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lectura/escritura<br/> | Esta propiedad establecerá o devolverá el nombre del tipo preconcebido por el que filtrar los resultados.<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lectura/escritura<br/> | Estilo de encabezado que se muestra en la vista.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Solo escritura<br/> | Esto devuelve TRUE si la consulta de vistas se ha modificado y necesita actualizarse. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lectura/escritura<br/> | Esta propiedad establecerá o devolverá el nombre del almacén por el que filtrar los resultados.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lectura/escritura<br/> | Controla el modo de presentación del panel de vista previa.<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Solo escritura<br/> | Al llamar a la colección de filtros de propiedades, devolverá lo siguiente:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lectura/escritura<br/> | Obtiene o establece el texto de la consulta actual.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Solo escritura<br/> | Sin implementar.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lectura/escritura<br/> | Esta propiedad establecerá o devolverá el orden de las columnas por las que ordenar los resultados. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lectura/escritura<br/> | Esta propiedad establecerá o devolverá indexColumn de la propiedad por la que ordenar los resultados. <br/> |



 

## <a name="remarks"></a>Comentarios

Estos métodos y propiedades se usan para manipular la información vista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2003 solo con aplicaciones de escritorio sp1 \[\]<br/>                             |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

