---
title: Media. durationString
description: La propiedad durationString recupera un valor de cadena que indica la duración del elemento multimedia actual en formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media Player Windows Media. durationString
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709097"
---
# <a name="mediadurationstring"></a>Media. durationString

La propiedad **durationString** recupera un valor de **cadena** que indica la duración del elemento multimedia actual en formato HH: mm: SS.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentMedia*. **durationString**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Si esta propiedad se utiliza con un elemento multimedia distinto del especificado en el *reproductor*. **currentMedia**, puede que no contenga un valor válido. Si el elemento multimedia tiene una longitud inferior a una hora, se omite la parte HH: del valor devuelto.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **durationString** para mostrar la duración del elemento multimedia actual como texto con formato. Un elemento HTML DIV denominado MediaInfo muestra la información de duración. El objeto **Player** se creó con ID = "Player".


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. Duration**](media-duration.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





