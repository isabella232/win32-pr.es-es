---
title: Método media. getMarkerTime
description: El método getMarkerTime recupera la hora del marcador en el índice especificado.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- método getMarkerTime de Windows Media Player
- método getMarkerTime Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getMarkerTime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700144"
---
# <a name="mediagetmarkertime-method"></a>Método media. getMarkerTime

El método **getMarkerTime** recupera la hora del marcador en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*markerNum* \[ de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice del marcador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Double**) que especifica la ubicación del marcador en segundos desde el principio del clip.

## <a name="remarks"></a>Observaciones

Este método devuelve **null** si el marcador especificado no existe.

Algunos elementos multimedia digitales no contienen marcadores. Use **markerCount** para averiguar el número de marcadores que hay en el clip actual.

Los números de índice de marcador empiezan en 1.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **getMarkerTime** para rellenar un elemento TEXTAREA HTML denominado MTIMES con la ubicación de cada marcador. El objeto **Player** se creó con ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
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

[**Media. getMarkerName**](media-getmarkername.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





