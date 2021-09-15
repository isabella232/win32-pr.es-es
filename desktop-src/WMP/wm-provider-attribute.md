---
title: Atributo WM/Provider
description: El atributo WM/Provider es el nombre del proveedor de los valores de atributo.
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- Atributo WM/Provider Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466387"
---
# <a name="wmprovider-attribute"></a>Atributo WM/Provider

El **atributo WM/Provider** es el nombre del proveedor de los valores de atributo.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Listas de reproducción de CD](cd-playlist-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)
-   [Elementos de radio](radio-item-attributes.md)
-   [Elementos de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca (o caché) como en el archivo multimedia digital.

**MetadataSource** es un alias para este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMProvider.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior (el elemento de foto solo se admite en Reproductor de Windows Media 10 o posterior)<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





