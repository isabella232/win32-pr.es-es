---
title: Atributo WM/TrackNumber
description: El atributo WM/TrackNumber es el número de pista del elemento del álbum en el que se publicó originalmente.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Atributo WM/TrackNumber Reproductor de Windows Media
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249506"
---
# <a name="wmtracknumber-attribute"></a>Atributo WM/TrackNumber

El **atributo WM/TrackNumber** es el número de pista del elemento del álbum en el que se publicó originalmente.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo multimedia Windows uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena tanto en la biblioteca como en el archivo multimedia digital.

Los números de seguimiento de un álbum comienzan en 1.

**OriginalIndex** y **OriginalIndexLeft son** alias de este atributo.

La Windows SDK de formato multimedia para este atributo es g \_ wszWMTrackNumber.

Para determinar si puede cambiar el valor de este atributo, use el [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> </dl>

 

 





