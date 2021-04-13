---
description: Enumeración que se usa para indicar por qué se rechazó un píxel.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359963"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumeración PIXELKILLREASON

Enumeración que se usa para indicar por qué se rechazó un píxel.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ ninguno**  
Valor que indica que no se rechazó el píxel.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Valor que indica que se rechazó el píxel porque no se ejecutó el sombreador.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
Valor que indica que se rechazó el píxel porque se produjo un error en la prueba de tijera.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Valor que indica que se rechazó el píxel porque se produjo un error en la prueba alfa.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Valor que indica que se rechazó el píxel porque se produjo un error en la prueba de estarcido.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
Valor que indica que se rechazó el píxel porque se produjo un error en la prueba de profundidad.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Valor que indica que no se puede calcular el historial de píxeles.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_error PKR**  
Valor que indica que el píxel se rechazó debido a un error general.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ Intersection**  
Valor que indica que se rechazó el píxel porque la llamada a Draw no forma una intersección con el píxel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ ocluidos**  
Valor que indica que se rechazó el píxel porque se ocluidos el dibujo.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
Valor que indica que se rechazó el píxel porque no se pudo realizar la prueba de profundidad y de estarcido.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



