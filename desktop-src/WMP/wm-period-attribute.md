---
title: Atributo WM/period
description: El atributo WM/period es el período del contenido.
ms.assetid: fb154ef7-c8bc-4468-8f3f-4b716291fd0a
keywords:
- Atributo WM/period Windows Media Player
topic_type:
- apiref
api_name:
- WM/Period
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d528780b8dc0f51f9072a0ca0a2cfb7095104
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708269"
---
# <a name="wmperiod-attribute"></a>Atributo WM/period

El atributo **WM/period** es el período del contenido.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**Period** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMPeriod.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





