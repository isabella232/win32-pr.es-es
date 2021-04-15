---
title: Lista de reproducción. attributeCount
description: La propiedad attributeCount recupera el número de atributos asociados a la lista de reproducción.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Windows Media Player de lista de reproducción. attributeCount
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708970"
---
# <a name="playlistattributecount"></a>Lista de reproducción. attributeCount

La propiedad **attributeCount** recupera el número de atributos asociados a la lista de reproducción.

## <a name="syntax"></a>Sintaxis

*reproductor*. *currentPlaylist*. **attributeCount**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de solo lectura (**Long**).

## <a name="remarks"></a>Observaciones

Dado que las listas de reproducción pueden provienen de muchos orígenes diferentes, pueden tener varios conjuntos de propiedades. Este método recupera el número total de propiedades disponibles para que los demás métodos del objeto de **lista de reproducción** puedan tener acceso a ellas.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.

## <a name="examples"></a>Ejemplos

En el ejemplo de JScript siguiente se muestra cómo se utilizan varias propiedades y métodos de la **lista de reproducción** y los objetos **multimedia** .


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Lista de reproducción. attributeName**](playlist-attributename.md)
</dt> <dt>

[**Lista de reproducción. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Lista de reproducción. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





