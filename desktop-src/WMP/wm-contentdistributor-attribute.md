---
title: Atributo WM/ContentDistributor
description: El atributo WM/ContentDistributor es el nombre del distribuidor del elemento.
ms.assetid: 45f548a4-4059-464c-af93-1ba09e6b8d1e
keywords:
- Media Player de Windows de atributos de WM/ContentDistributor
topic_type:
- apiref
api_name:
- WM/ContentDistributor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 420e3e05a68f89d8e37b8ef95dd1247802442700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708731"
---
# <a name="wmcontentdistributor-attribute"></a>Atributo WM/ContentDistributor

El atributo **WM/ContentDistributor** es el nombre del distribuidor del elemento.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Reproducción](playlist-attributes-ref.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

**ContentDistributor** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMContentDistributor.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





