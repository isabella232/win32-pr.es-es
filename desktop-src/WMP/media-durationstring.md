---
title: Media.durationString
description: La propiedad durationString recupera un valor String que indica la duración del elemento multimedia actual en formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media.durationString Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967499"
---
# <a name="mediadurationstring"></a>Media.durationString

La **propiedad durationString** recupera un valor **String** que indica la duración del elemento multimedia actual en formato HH:MM:SS.

## <a name="syntax"></a>Sintaxis

*player*. *currentMedia*. **durationString**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Observaciones

Si esta propiedad se usa con un elemento multimedia distinto del especificado en el *Reproductor de*. **currentMedia**, puede que no contenga un valor válido. Si el elemento multimedia tiene menos de una hora de duración, se omite la parte HH: del valor devuelto.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **durationString** para mostrar la duración del elemento multimedia actual como texto con formato. Un elemento DIV HTML denominado MediaInfo muestra la información de duración. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media.duration**](media-duration.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





