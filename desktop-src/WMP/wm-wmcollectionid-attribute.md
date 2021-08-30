---
title: Atributo WM/WMCollectionID
description: El atributo WM/WMCollectionID es un GUID que identifica la colección a la que pertenece el elemento.
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- Atributo WM/WMCollectionID Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623961ea069f5c01ba187b706a4590926f8e2670773d3d66618fa40c063e61c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900305"
---
# <a name="wmwmcollectionid-attribute"></a>Atributo WM/WMCollectionID

El **atributo WM/WMCollectionID** es un GUID que identifica la colección a la que pertenece el elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentarios

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia.

**WMCollectionID es** un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMCollectionID.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





