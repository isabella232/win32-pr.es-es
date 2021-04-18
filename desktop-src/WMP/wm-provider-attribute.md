---
title: Atributo WM/proveedor
description: El atributo WM/Provider es el nombre del proveedor de los valores de atributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Media Player de Windows de atributo de WM/proveedor
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718743"
---
# <a name="wmprovider-attribute"></a>Atributo WM/proveedor

El atributo **WM/Provider** es el nombre del proveedor de los valores de atributo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**Metadatasource** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMProvider.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior (el elemento de fotografía solo se admite en Windows Media Player 10 o posterior)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





