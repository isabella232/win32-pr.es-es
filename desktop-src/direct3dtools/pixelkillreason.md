---
description: Enumeración usada para indicar por qué se rechazó un píxel.
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
ms.openlocfilehash: 15ad935ff5949c9f8de79aac55b339314c54ddf4
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623769"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumeración PIXELKILLREASON

Enumeración usada para indicar por qué se rechazó un píxel.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ NONE**  
Valor que indica que el píxel no se rechazó.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Valor que indica que el píxel se rechazó porque el sombreador no se ha ejecutado.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ DE LA PRUEBA DE DESERCIÓN**  
Valor que indica que el píxel se rechazó porque se ha dado error en la prueba de la lecha.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Valor que indica que el píxel se rechazó porque no se pudo realizar la prueba alfa.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Valor que indica que el píxel se rechazó porque no se pudo realizar la prueba de galería de símbolos.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**PKR \_ DEPTHTEST**  
Valor que indica que el píxel se rechazó porque no se pudo realizar la prueba de profundidad.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Valor que indica que no se puede calcular el historial de píxeles.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**PKR \_ ERROR**  
Valor que indica que el píxel se rechazó debido a un error general.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOINTERSECTION**  
Valor que indica que el píxel se rechazó porque la llamada a draw no forma una intersección con el píxel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ OCCLUDED**  
Valor que indica que el píxel se rechazó porque el dibujo se ha ocluido.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PKR \_ DEPTHSTENCILTEST**  
Valor que indica que el píxel se rechazó porque la prueba de profundidad y galería de símbolos no se pudo realizar.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



