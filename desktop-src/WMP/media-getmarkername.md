---
title: Método Media.getMarkerName
description: El método getMarkerName recupera el nombre del marcador en el índice especificado.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- Método getMarkerName Reproductor de Windows Media
- Método getMarkerName Reproductor de Windows Media , clase Media
- Clase media Reproductor de Windows Media método , getMarkerName
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1ace88a7012ec59bf4dcae32c5c2f51f240dd1e59c58408165392a6fc1e616
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123405"
---
# <a name="mediagetmarkername-method"></a>Método Media.getMarkerName

El **método getMarkerName** recupera el nombre del marcador en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*markerNum* \[ En\]
</dt> <dd>

**Number** (**long**) que especifica un índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Comentarios

Este método devuelve **NULL** si el marcador especificado no existe.

Algunos elementos multimedia digitales no contienen marcadores. Use **markerCount** para averiguar cuántos marcadores hay en el clip actual.

Los números de índice de marcador comienzan en 1.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se usa *Media*. **getMarkerName para** rellenar un elemento TEXTAREA HTML denominado MNAMES con los nombres de los marcadores del elemento multimedia actual. El **objeto Player** se creó con id. = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
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

[**Media.getMarkerTime**](media-getmarkertime.md)
</dt> <dt>

[**Media.markerCount**](media-markercount.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





