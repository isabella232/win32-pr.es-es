---
title: Playlist.attributeCount
description: La propiedad attributeCount recupera el número de atributos asociados a la lista de reproducción.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Lista de reproducción.atributoCount Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359536"
---
# <a name="playlistattributecount"></a>Playlist.attributeCount

La **propiedad attributeCount** recupera el número de atributos asociados a la lista de reproducción.

## <a name="syntax"></a>Sintaxis

*player*. *currentPlaylist*. **attributeCount**

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de solo **lectura** (**long**).

## <a name="remarks"></a>Observaciones

Dado que las listas de reproducción pueden proceden de muchos orígenes diferentes, pueden tener varios conjuntos de propiedades diferentes. Este método recupera el número total de propiedades disponibles para que los demás métodos del objeto **Lista** de reproducción puedan acceder a ellas.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la referencia Reproductor de Windows Media [atributo](attribute-reference.md).

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se muestra cómo se usan varias propiedades y métodos de los objetos **Playlist** y **Media.**


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de lista de reproducción**](playlist-object.md)
</dt> <dt>

[**Playlist.attributeName**](playlist-attributename.md)
</dt> <dt>

[**Playlist.getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Playlist.setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





