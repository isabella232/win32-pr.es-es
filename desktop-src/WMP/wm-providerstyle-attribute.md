---
title: Atributo WM/ProviderStyle
description: El atributo WM/ProviderStyle es el estilo del elemento asignado por el proveedor de los valores de atributo.
ms.assetid: 43994d6b-0d71-4f2c-834a-47bbcd32b461
keywords:
- Media Player de Windows de atributos de WM/ProviderStyle
topic_type:
- apiref
api_name:
- WM/ProviderStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a18af02254e7ce476ffc9c1e427465966cd66c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718866"
---
# <a name="wmproviderstyle-attribute"></a>Atributo WM/ProviderStyle

El atributo **WM/ProviderStyle** es el estilo del elemento asignado por el proveedor de los valores de atributo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**Style** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProviderStyle.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





