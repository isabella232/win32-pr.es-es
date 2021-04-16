---
title: Atributo WM/TrackNumber
description: El atributo WM/TrackNumber es el número de pista del elemento en el álbum en el que se liberó originalmente.
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- Media Player de Windows de atributos de WM/TrackNumber
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690566"
---
# <a name="wmtracknumber-attribute"></a>Atributo WM/TrackNumber

El atributo **WM/TrackNumber** es el número de pista del elemento en el álbum en el que se liberó originalmente.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca y en el archivo multimedia digital.

Los números de seguimiento de un álbum empiezan en 1.

**OriginalIndex** y **OriginalIndexLeft** son alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMTrackNumber.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





