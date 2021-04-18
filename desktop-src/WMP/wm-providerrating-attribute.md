---
title: Atributo WM/ProviderRating
description: El atributo WM/ProviderRating es la clasificación del elemento asignado por el proveedor de los valores de atributo.
ms.assetid: a1a76560-a8d9-486a-badc-56d7bf488c10
keywords:
- Media Player de Windows de atributos de WM/ProviderRating
topic_type:
- apiref
api_name:
- WM/ProviderRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc0f71985d948e59b8c0f98d50445a48263d67cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718742"
---
# <a name="wmproviderrating-attribute"></a>Atributo WM/ProviderRating

El atributo **WM/ProviderRating** es la clasificación del elemento asignado por el proveedor de los valores de atributo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**Rating** es un alias de este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProviderRating.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





