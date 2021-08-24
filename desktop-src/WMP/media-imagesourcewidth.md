---
title: Media.imageSourceWidth
description: La propiedad imageSourceWidth recupera el ancho del elemento multimedia actual en píxeles.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media.imageSourceWidth Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710b6f0d91d7d734b12ad75f201fcd45037f67adf2c8ed3cb60f3ee5fcf6c222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508405"
---
# <a name="mediaimagesourcewidth"></a>Media.imageSourceWidth

La **propiedad imageSourceWidth** recupera el ancho del elemento multimedia actual en píxeles.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **imageSourceWidth**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Comentarios

Si el elemento multimedia no es el actual, esta propiedad devuelve cero.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **imageSourceWidth para** mostrar el tamaño de la imagen, en píxeles, del **elemento multimedia actual. La información se imprime en un elemento TEXTAREA HTML denominado VideoSize. El objeto Player** se creó con id. = "player".


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





