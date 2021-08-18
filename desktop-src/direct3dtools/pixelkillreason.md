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
ms.openlocfilehash: 58ead08f81c8dee1644e431ae100c5100551e9907ab9a9d5bf00f6aae3532abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119329"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumeración PIXELKILLREASON

Enumeración usada para indicar por qué se rechazó un píxel.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ NONE**  
Valor que indica que el píxel no se rechazó.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Valor que indica que el píxel se rechazó porque el sombreador no se ha ejecutado.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ DE LA PRUEBA DE DESERCIÓN**  
Valor que indica que el píxel se rechazó porque se ha dado error en la prueba de examen.

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

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



