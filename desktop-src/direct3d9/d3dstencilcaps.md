---
description: Marcas de capacidad de estarcido de controlador.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423239"
---
# <a name="d3dstencilcaps"></a>D3DSTENCILCAPS

Marcas de capacidad de estarcido de controlador.



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| \#define                 | Value       | Descripción                                                                                           |
| D3DSTENCILCAPS \_ mantener     | 0x00000001L | No actualice la entrada en el búfer de estarcido. Este es el valor predeterminado.                             |
| D3DSTENCILCAPS \_ cero     | 0x00000002L | Establezca la entrada de búfer de estarcido en 0.                                                                    |
| D3DSTENCILCAPS \_ reemplazar  | 0x00000004L | Reemplace la entrada del búfer de estarcido por el valor de referencia.                                                |
| D3DSTENCILCAPS \_ INCRSAT  | 0x00000008L | Incremente la entrada del búfer de la galería de símbolos y la fijación al valor máximo.                                    |
| D3DSTENCILCAPS \_ DECRSAT  | 0x00000010L | Disminuya la entrada del búfer de la galería de símbolos, de la abrazadera a cero.                                                 |
| \_Invertir D3DSTENCILCAPS   | 0x00000020L | Invierta los bits en la entrada de búfer de la galería de símbolos.                                                          |
| D3DSTENCILCAPS \_ incr     | 0x00000040L | Incremente la entrada del búfer de la galería de símbolos, ajustándola a cero si el nuevo valor supera el valor máximo.      |
| D3DSTENCILCAPS \_ decr (     | 0x00000080L | Disminuye la entrada del búfer de estarcido, ajustándola al valor máximo si el nuevo valor es menor que cero. |
| D3DSTENCILCAPS \_ TWOSIDED | 0x00000100L | El dispositivo admite la galería de símbolos de dos caras.                                                                |



 

Las entradas de búfer de estarcido son valores enteros comprendidos entre 0 y 2 ⁿ-1, donde n es la profundidad de bits del búfer de estarcido.

El miembro StencilCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.

## <a name="constant-information"></a>Información constante



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3d9caps. h |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



