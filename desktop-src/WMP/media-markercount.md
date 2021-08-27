---
title: Media.markerCount
description: La propiedad markerCount recupera el número de marcadores del elemento multimedia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media.markerCount Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00206991f81c6a445648a063a37bcc45bf91f647b60317772478142eefd1b20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123355"
---
# <a name="mediamarkercount"></a>Media.markerCount

La **propiedad markerCount** recupera el número de marcadores del elemento multimedia.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **markerCount**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**) que especifica el número de marcadores en el archivo.

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve cero si un archivo no tiene marcadores o si el elemento multimedia no es el mismo que el *reproductor*. **currentMedia**.

Los números de marcador comienzan en 1.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **markerCount** para recuperar el número de marcadores en el elemento multimedia actual. A continuación, ese valor se usa como límite superior para una estructura de bucle, que recorre en iteración la lista de marcadores para recuperar cada nombre de marcador. Un elemento TEXTAREA HTML denominado MNAMES muestra los nombres de los marcadores en el elemento multimedia actual. El **objeto Player** se creó con id. = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





