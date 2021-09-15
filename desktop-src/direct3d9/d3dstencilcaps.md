---
description: Marcas de funcionalidad de galería de símbolos del controlador.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566121"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Marcas de funcionalidad de galería de símbolos del controlador.



| \#Definir                 | Value       | Descripción                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| D3DSTENCILCAPS \_ KEEP     | 0x00000001L | No actualice la entrada en el búfer de galería de símbolos. Este es el valor predeterminado.                             |
| D3DSTENCILCAPS \_ ZERO     | 0x00000002L | Establezca la entrada stencil-buffer en 0.                                                                    |
| D3DSTENCILCAPS \_ REPLACE  | 0x00000004L | Reemplace la entrada stencil-buffer por el valor de referencia.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Incremente la entrada stencil-buffer, fijando al valor máximo.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Decremento de la entrada stencil-buffer, fijando a cero.                                                 |
| D3DSTENCILCAPS \_ INVERT   | 0x00000020L | Invierta los bits de la entrada stencil-buffer.                                                          |
| D3DSTENCILCAPS \_ INCR     | 0x00000040L | Incremente la entrada stencil-buffer y ajuste a cero si el nuevo valor supera el valor máximo.      |
| D3DSTENCILCAPS \_ DECR     | 0x00000080L | Decremento de la entrada stencil-buffer, ajustando al valor máximo si el nuevo valor es menor que cero. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | El dispositivo admite galería de símbolos de dos lados.                                                                |



 

Las entradas de búfer de galería de símbolos son valores enteros comprendidos entre 0 y 2ⁿ - 1, donde n es la profundidad de bits del búfer de galería de símbolos.

El miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3d9caps.h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



