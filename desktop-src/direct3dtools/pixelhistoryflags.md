---
description: Una enumeración que contiene marcas que se usan para describir un resultado del historial de píxeles. Vea PixelHistoryOperation.
MS-HAID: vspixengine.PIXELHISTORYFLAGS
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PIXELHISTORYFLAGS
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BDB88A2D-016A-4E15-B47A-870A2959E943
api_name:
- PIXELHISTORYFLAGS
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a1b4b0e5b3df84af04d5533ec9d53b15ebe5057
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152215"
---
# <a name="span-idvspixenginepixelhistoryflagsspanpixelhistoryflags-enumeration"></a><span id="vspixengine.pixelhistoryflags"></span>Enumeración PIXELHISTORYFLAGS

Una enumeración que contiene marcas que se usan para describir un resultado del historial de píxeles. Vea PixelHistoryOperation.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PHF_INITIALVALUE"></span><span id="phf_initialvalue"></span>**PHF \_ INITIALVALUE**  
Marca que corresponde al valor de color inicial (antes del marco).

<span id="PHF_CLEAR"></span><span id="phf_clear"></span>**PHF \_ borrar**  
Marca que corresponde al resultado de color no cifrado.

<span id="PHF_DRAW"></span><span id="phf_draw"></span>**PHF \_ Draw**  
Marca que corresponde al resultado del color de dibujo.

<span id="PHF_FINALVALUE"></span><span id="phf_finalvalue"></span>**PHF \_ FINALVALUE**  
Marca que corresponde al resultado final del color.

<span id="PHF_HASCOLOR"></span><span id="phf_hascolor"></span>**PHF \_ HASCOLOR**  
Marca que corresponde a si el resultado del color está presente en el struct PixelHistoryOperation.

<span id="PHF_HASFBCOLOR"></span><span id="phf_hasfbcolor"></span>**PHF \_ HASFBCOLOR**  
Marca que corresponde a si el resultado del color final del búfer está presente en el struct PixelHistoryOperation.

<span id="PHF_ERROR"></span><span id="phf_error"></span>**\_error PHF**  

<span id="PHF_VERTEXPROCESSINGSKIPPED"></span><span id="phf_vertexprocessingskipped"></span>**PHF \_ VERTEXPROCESSINGSKIPPED**  
No se utiliza.

<span id="PHF_MODIFYRESOURCE"></span><span id="phf_modifyresource"></span>**PHF \_ MODIFYRESOURCE**  

<span id="PHF_CANNOTRUNFULLDEPTHSTENCILTEST"></span><span id="phf_cannotrunfulldepthstenciltest"></span>**PHF \_ CANNOTRUNFULLDEPTHSTENCILTEST**  
Marca que corresponde a no poder ejecutar la prueba de profundidad o de estarcido.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



