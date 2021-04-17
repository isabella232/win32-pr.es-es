---
title: Atributo WM/compositor
description: El atributo WM/compositor es el nombre del compositor de la música.
ms.assetid: 48459027-ed80-46a2-ad5c-ace602144150
keywords:
- Media Player de Windows de atributo de WM/compositor
topic_type:
- apiref
api_name:
- WM/Composer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f206b1a23126612f3f7c875b9a9b4badca8339
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708735"
---
# <a name="wmcomposer-attribute"></a>Atributo WM/compositor

El atributo **WM/compositor** es el nombre del compositor de la música.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

Este atributo puede tener varios valores. Para recuperar todos los valores de un atributo con varios valores, debe usar el método **media. getItemInfoByType** , no el método **media. getItemInfo** .

**Composer** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMComposer.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





