---
title: Método media. getMarkerName
description: El método getMarkerName recupera el nombre del marcador en el índice especificado.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- método getMarkerName de Windows Media Player
- método getMarkerName Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getMarkerName
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
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700232"
---
# <a name="mediagetmarkername-method"></a>Método media. getMarkerName

El método **getMarkerName** recupera el nombre del marcador en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*markerNum* \[ de\]
</dt> <dd>

**Número** (**largo**) que especifica un índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Este método devuelve **null** si el marcador especificado no existe.

Algunos elementos multimedia digitales no contienen marcadores. Use **markerCount** para averiguar el número de marcadores que hay en el clip actual.

Los números de índice de marcador empiezan en 1.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se utiliza el *medio*. **getMarkerName** para rellenar un elemento TEXTAREA HTML denominado MNAMES con los nombres de los marcadores en el elemento multimedia actual. El objeto **Player** se creó con ID = "Player".


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
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto multimedia**](media-object.md)
</dt> <dt>

[**Media. getMarkerTime**](media-getmarkertime.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





