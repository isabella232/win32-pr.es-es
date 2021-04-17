---
title: Atributo WM/MCDI
description: El atributo WM/MCDI es el identificador del CD de música desde el que se copió el archivo o la pista.
ms.assetid: f0bec14d-416c-477f-98df-dece0bf85ea4
keywords:
- Media Player de Windows de atributos de WM/MCDI
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec51c306f94e25acb94155c4d87f1f1a8b95866
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708714"
---
# <a name="wmmcdi-attribute"></a>Atributo WM/MCDI

El atributo **WM/MCDI** es el identificador del CD de música desde el que se copió el archivo o la pista.

## <a name="applies-to"></a>Se aplica a

-   [Elementos de audio](audio-item-attributes.md)
-   [Pistas de CD](cd-track-attributes.md)
-   [Atributos de archivo de Windows Media de uso frecuente](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Observaciones

Este atributo se almacena en la biblioteca (o caché) y en el archivo multimedia digital.

**TOC** es un alias para este atributo.

La constante del SDK de Windows Media Format para este atributo es g \_ wszWMMCDI.

Para determinar si puede cambiar el valor de este atributo, use el método [media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> </dl>

 

 





