---
title: Interfaz IWMPMedia (VB y C) (WMP. h)
description: Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia. La interfaz IWMPMedia expone las siguientes propiedades.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- IWMPMedia (VB y C) interfaz de Windows Media Player
- IWMPMedia (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPMedia (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c60a3396710ea4c426bd41c96db34e1e59cc690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690772"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Interfaz IWMPMedia (VB y C#)

Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia.

La interfaz **IWMPMedia** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPMedia (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPMedia (VB y C#)** tiene estos métodos.



| Método                                                                             | Descripción                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Devuelve el nombre del atributo correspondiente al índice especificado.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Devuelve el valor del atributo especificado para el elemento multimedia.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Devuelve el valor del atributo con el número de índice especificado.<br/>                                |
| [**getMarkerName**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Devuelve el nombre del marcador en el índice especificado.<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Devuelve la hora del marcador en el índice especificado.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Devuelve un valor que indica si el elemento multimedia especificado es un miembro de la lista de reproducción especificada.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Devuelve un valor que indica si se pueden editar los atributos del elemento multimedia especificado.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Establece el valor del atributo especificado para el elemento multimedia.<br/>                                      |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPMedia (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso          | Descripción                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.<br/>                                                          |
| [**Duration**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Solo lectura<br/> | Obtiene la duración en segundos del elemento multimedia actual.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor que indica la duración del elemento multimedia actual en formato HH: MM: SS.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el alto del elemento multimedia actual en píxeles.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Solo lectura<br/> | Obtiene el ancho del elemento multimedia actual en píxeles.<br/>                                                                                       |
| [**isIdentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Solo lectura<br/> | Obtiene un valor que indica si el elemento multimedia especificado es igual que el actual. En C#, este es el método **Get \_ isIdentical** .<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Solo lectura<br/> | Obtiene el número de marcadores del elemento multimedia.<br/>                                                                                             |
| [**name**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Solo lectura<br/> | Obtiene o establece el nombre del elemento multimedia.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Solo lectura<br/> | Obtiene la dirección URL del elemento multimedia.<br/>                                                                                                           |



 

Obtenga una interfaz **IWMPMedia** con las siguientes propiedades o métodos a los que se tiene acceso a través del objeto o la interfaz siguientes.



| Objeto o interfaz                                               | Propiedad o método                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**CurrentItem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Elemento**](iwmpplaylist-item--vb-and-c.md) (obtener \_ elemento en C#)                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia2 (VB y C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





