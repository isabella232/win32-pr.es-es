---
title: Atributo WM/EncodingTime
description: El atributo WM/EncodingTime es la fecha y la hora en que se ha codificado el contenido.
ms.assetid: 264f379a-0bec-4143-bc23-ab45fb725af6
keywords:
- Media Player de Windows de atributos de WM/EncodingTime
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659a1ec5b192782370804745da3f232db6e439dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708724"
---
# <a name="wmencodingtime-attribute"></a>Atributo WM/EncodingTime

El atributo **WM/EncodingTime** es la fecha y la hora en que se ha codificado el contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

**CreationDate** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMEncodingTime.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





