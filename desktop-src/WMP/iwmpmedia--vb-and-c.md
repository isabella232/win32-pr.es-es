---
title: Interfaz IWMPMedia (VB y C) (Wmp.h)
description: Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia. La interfaz IWMPMedia expone las siguientes propiedades.
ms.assetid: 4f67336e-d1d3-4f18-b063-086edf9d9094
keywords:
- Interfaz IWMPMedia (VB y C) Reproductor de Windows Media
- Interfaz IWMPMedia (VB y C) Reproductor de Windows Media , descrito
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
ms.openlocfilehash: 8d36fc2a7c4f65856b68c00147e32f9b3af4cc3e649a9717e7734583d4516b44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572465"
---
# <a name="iwmpmedia-vb-and-c-interface"></a>Interfaz IWMPMedia (VB y C#)

Proporciona una manera de establecer y recuperar las propiedades de un elemento multimedia.

La **interfaz IWMPMedia** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPMedia (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPMedia (VB y C#)** tiene estos métodos.



| Método                                                                             | Descripción                                                                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**getAttributeName**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)   | Devuelve el nombre del atributo correspondiente al índice especificado.<br/>                            |
| [**getItemInfo**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)             | Devuelve el valor del atributo especificado para el elemento multimedia.<br/>                                   |
| [**getItemInfoByAtom**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md) | Devuelve el valor del atributo con el número de índice especificado.<br/>                                |
| [**getMarkerName**](wmplibiwmpmedia-iwmpmedia-getmarkername--vb-and-c.md)         | Devuelve el nombre del marcador en el índice especificado.<br/>                                             |
| [**getMarkerTime**](wmplibiwmpmedia-iwmpmedia-getmarkertime--vb-and-c.md)         | Devuelve la hora del marcador en el índice especificado.<br/>                                             |
| [**isMemberOf**](wmplibiwmpmedia-iwmpmedia-ismemberof--vb-and-c.md)               | Devuelve un valor que indica si el elemento multimedia especificado es miembro de la lista de reproducción especificada.<br/> |
| [**isReadOnlyItem**](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)       | Devuelve un valor que indica si se pueden editar los atributos del elemento multimedia especificado.<br/>       |
| [**setItemInfo**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)             | Establece el valor del atributo especificado para el elemento multimedia.<br/>                                      |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPMedia (VB y C#)** tiene estas propiedades.



| Propiedad                                                                                      | Tipo de acceso          | Descripción                                                                                                                                          |
|:----------------------------------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attributeCount**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.<br/>                                                          |
| [**Duración**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)<br/>                   | Solo lectura<br/> | Obtiene la duración en segundos del elemento multimedia actual.<br/>                                                                                   |
| [**durationString**](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)<br/>       | Solo lectura<br/> | Obtiene un valor que indica la duración del elemento multimedia actual en formato HH:MM:SS.<br/>                                                        |
| [**imageSourceHeight**](wmplibiwmpmedia-iwmpmedia-imagesourceheight--vb-and-c.md)<br/> | Solo lectura<br/> | Obtiene el alto del elemento multimedia actual en píxeles.<br/>                                                                                      |
| [**imageSourceWidth**](wmplibiwmpmedia-iwmpmedia-imagesourcewidth--vb-and-c.md)<br/>   | Solo lectura<br/> | Obtiene el ancho del elemento multimedia actual en píxeles.<br/>                                                                                       |
| [**isIdentical**](iwmpmedia-isidentical--vb-and-c.md)<br/>                             | Solo lectura<br/> | Obtiene un valor que indica si el elemento multimedia especificado es el mismo que el actual. En C#, este es el **método \_ get isIdentical.**<br/> |
| [**markerCount**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)<br/>             | Solo lectura<br/> | Obtiene el número de marcadores del elemento multimedia.<br/>                                                                                             |
| [**Nombre**](wmplibiwmpmedia-iwmpmedia-name--vb-and-c.md)<br/>                           | Solo lectura<br/> | Obtiene o establece el nombre del elemento multimedia.<br/>                                                                                                  |
| [**sourceURL**](wmplibiwmpmedia-iwmpmedia-sourceurl--vb-and-c.md)<br/>                 | Solo lectura<br/> | Obtiene la dirección URL del elemento multimedia.<br/>                                                                                                           |



 

Obtenga una **interfaz IWMPMedia** mediante las siguientes propiedades o métodos a los que se accede a través del siguiente objeto o interfaz.



| Objeto o interfaz                                               | Propiedad o método                                                                                                                       |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMPControls**](iwmpcontrols--vb-and-c.md)                    | [**Currentitem**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)                                                             |
| [AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**currentMedia**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md), [ **newMedia**](axwmplib-axwindowsmediaplayer-newmedia.md) |
| [**IWMPPlaylist**](iwmpplaylist--vb-and-c.md)                    | [**Elemento**](iwmpplaylist-item--vb-and-c.md) (obtener \_ elemento en C#)                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia2 (VB y C#)**](iwmpmedia2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> </dl>

 

 





