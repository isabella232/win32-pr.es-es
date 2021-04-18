---
title: CdromCollection. Item (método)
description: El método Item recupera el objeto CDROM en el índice especificado.
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- método de elemento Media Player de Windows
- método de elemento Windows Media Player, clase CdromCollection
- Clase CdromCollection Windows Media Player, método Item
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700310"
---
# <a name="cdromcollectionitem-method"></a>CdromCollection. Item (método)

El método **Item** recupera el objeto **CDROM** en el índice especificado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que contiene el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **CDROM** .

## <a name="remarks"></a>Observaciones

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *CdromCollection*. **elemento** para imprimir el nombre de la lista de reproducción de cada CD disponible en el equipo. Si la unidad contiene realmente contenido de DVD, se requiere Windows XP o posterior. Se creó un elemento TextArea HTML con el identificador = "listas de reproducción". El objeto **Player** se creó con ID = "Player".


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDROM. driveSpecifier**](cdrom-drivespecifier.md)
</dt> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**CdromCollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Playlist.name**](playlist-name.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





