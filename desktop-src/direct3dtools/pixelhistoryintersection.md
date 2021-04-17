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
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705247"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>Estructura PixelHistoryIntersection

Representa información sobre un determinado

## <a name="syntax"></a>Sintaxis


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>Miembros

**Númeromarco**  
El marco del evento de gráficos asociada con esta operación.

**Eid**  
IDENTIFICADOR del evento de gráficos asociado a esta operación.

**renderTargetPtr**  
Destino de representación asociado originalmente (dentro de la aplicación capturada) con esta operación.

**eventType**  
El tipo de evento asociado a esta operación (en concreto, si este evento es una llamada a Draw).

**Elija**  
Coordenadas del píxel en el fotogramas.

**bAssemblerStageGeneratesInstanceID**  
True si el ensamblador de entrada genera identificadores de instancia; en caso contrario, false.

**flags**  
Combinación de valores de PIXELHISTORYFLAGS. Para obtener más información, consulte la enumeración PIXELHISTORYFLAGS.

**fbInitialRed**  
Fotogramas: valor del componente de color rojo de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**fbInitialGreen**  
Fotogramas: valor del componente de color verde de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**fbInitialBlue**  
Fotogramas: valor del componente de color azul de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**fbInitialAlpha**  
Fotogramas: valor del componente de color alfa de fotogramas antes de que se combine cualquier salida del sombreador de píxeles; es decir, al principio de este marco.

**LabelFBInitialRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.

**LabelFBInitialGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.

**LabelFBInitialBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.

**LabelFBInitialAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del fotogramas antes de cualquier sombreado de píxeles. es decir, al principio de este marco.

**fbRed**  
Fotogramas: valor del componente de color rojo de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.

**fbGreen**  
Fotogramas: valor del componente de color verde de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.

**fbBlue**  
Fotogramas: valor del componente de color azul de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.

**fbAlpha**  
Fotogramas: valor del componente de color alfa de fotogramas después de mezclar todos los resultados del sombreador de píxeles; es decir, el color fotogramas final.

**LabelFBRed**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color rojo del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.

**LabelFBGreen**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color verde del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.

**LabelFBBlue**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color azul del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.

**LabelFBAlpha**  
Cadena COM que contiene el nombre de la etiqueta asociada al componente de color alfa del fotogramas después de todos los sombreados de píxeles. es decir, el color fotogramas final.

**pixelKillReason**  
Especifica la razón por la que se ha eliminado la contribución de color del píxel.

**HResult**  
Si se produjo un error, contiene el valor HRESULT de DirectX que especifica el error.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



