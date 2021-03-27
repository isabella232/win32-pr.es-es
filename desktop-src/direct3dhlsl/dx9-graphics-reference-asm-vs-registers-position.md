---
title: Registro de posición
description: Este registro de salida del sombreador de vértices contiene datos de posición por vértice.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89470bb920db7c612b21cefb2c44c2c89d48ce28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776621"
---
# <a name="position-register"></a>Registro de posición

Este registro de salida del sombreador de vértices contiene datos de posición por vértice.



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro de posición      | x    | x    | x     | x    | x    | x     |



 

Un registro consta de propiedades que determinan el comportamiento de cada registro.



| Propiedad        | Descripción |
|-----------------|-------------|
| Nombre            | oPos        |
| Count           | 1 Vector    |
| Permisos de e/s | De solo escritura. |



 

El valor es la posición en el espacio de recorte homogéneo. Este valor debe escribirse en el sombreador de vértices.

Ejemplo


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros del sombreador de vértices](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




