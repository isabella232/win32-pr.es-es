---
description: Representa información sobre un determinado.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura PixelHistoryIntersection
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58583e7d3a6d273163c28eed7a4edce08bb7d83f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624791"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>Estructura PixelHistoryIntersection

Representa información sobre un determinado

## <a name="syntax"></a>Sintaxis


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>Miembros

**frameNumber**  
Marco del evento gráfico con el que se ha acomodo esta operación.

**Eid**  
Identificador del evento gráfico asociado a esta operación.

**renderTargetPtr**  
Destino de representación asociado originalmente (dentro de la aplicación capturada) a esta operación.

**eventType**  
Tipo de evento asociado a esta operación (en concreto, si este evento es una llamada a draw).

**Punto**  
Coordenadas del píxel en el búfer de fotogramas.

**bAssemblerStageGeneratesInstanceID**  
true si el ensamblador de entrada genera los iDs de instancia; en caso contrario, false.

**flags**  
Combinación de valores PIXELHISTORYFLAGS. Para obtener más información, vea la enumeración PIXELHISTORYFLAGS.

**fbInitialRed**  
Framebuffer: valor del componente de color rojo del búfer de fotogramas antes de combinar cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**fbInitialGreen**  
Framebuffer: valor del componente de color verde del búfer de fotogramas antes de combinar cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**fbInitialBlue**  
Framebuffer: valor del componente de color azul del búfer de fotogramas antes de combinar cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**fbInitialAlpha**  
Framebuffer: valor del componente de color alfa del búfer de fotogramas antes de combinar cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**LabelFBInitialRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del búfer de fotogramas antes de cualquier sombreado de píxeles; es decir, al principio de este marco.

**LabelFBInitialGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del búfer de fotogramas antes de cualquier sombreado de píxeles; es decir, al principio de este marco.

**LabelFBInitialBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del búfer de fotogramas antes de cualquier sombreado de píxeles; es decir, al principio de este marco.

**LabelFBInitialAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del búfer de fotogramas antes de cualquier sombreado de píxeles; es decir, al principio de este marco.

**fbRed**  
Framebuffer: valor del componente de color rojo del búfer de fotogramas después de combinar toda la salida del sombreador de píxeles; es decir, el color final del búfer de fotogramas.

**fbGreen**  
Framebuffer: valor del componente de color verde del búfer de fotogramas después de combinar toda la salida del sombreador de píxeles; es decir, el color final del búfer de fotogramas.

**fbBlue**  
Framebuffer: valor del componente de color azul del búfer de fotogramas después de combinar toda la salida del sombreador de píxeles; es decir, el color final del búfer de fotogramas.

**fbAlpha**  
Framebuffer: valor del componente de color alfa del búfer de fotogramas después de combinar toda la salida del sombreador de píxeles; es decir, el color final del búfer de fotogramas.

**LabelFBRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del búfer de fotogramas después de todo el sombreado de píxeles; es decir, el color final del búfer de fotogramas.

**LabelFBGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del búfer de fotogramas después de todo el sombreado de píxeles; es decir, el color final del búfer de fotogramas.

**LabelFBBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del búfer de fotogramas después de todo el sombreado de píxeles; es decir, el color final del búfer de fotogramas.

**LabelFBAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del búfer de fotogramas después de todo el sombreado de píxeles; es decir, el color final del búfer de fotogramas.

**pixelKillReason**  
Especifica el motivo por el que se ha detenido la contribución de color del píxel.

**Hresult**  
Si se produjo un error, contiene el HRESULT de DirectX que especifica el error.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



