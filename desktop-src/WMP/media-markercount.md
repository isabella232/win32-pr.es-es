---
title: Media. markerCount
description: La propiedad markerCount recupera el número de marcadores en el elemento multimedia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media Player Windows Media. markerCount
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
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699815"
---
# <a name="mediamarkercount"></a>Media. markerCount

La propiedad **markerCount** recupera el número de marcadores en el elemento multimedia.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentMedia*. **markerCount**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**) que especifica el número de marcadores del archivo.

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve cero si un archivo no tiene ningún marcador o si el elemento multimedia no es igual que el *reproductor*. **currentMedia**.

Los números de marcador comienzan en 1.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **markerCount** para recuperar el número de marcadores en el elemento multimedia actual. Ese valor se usa como límite superior para una estructura de bucle, que recorre en iteración la lista de marcadores para recuperar cada nombre de marcador. Un elemento TEXTAREA HTML denominado MNAMES muestra los nombres de los marcadores en el elemento multimedia actual. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





