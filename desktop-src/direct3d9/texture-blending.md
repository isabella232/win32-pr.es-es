---
description: Direct3D puede combinar hasta ocho texturas en primitivas en un solo paso.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Mezcla de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160422"
---
# <a name="texture-blending-direct3d-9"></a>Mezcla de textura (Direct3D 9)

Direct3D puede combinar hasta ocho texturas en primitivas en un solo paso. El uso de varias mezclas de textura puede aumentar considerablemente la velocidad de fotogramas de una aplicación Direct3D. Una aplicación emplea varias mezclas de texturas para aplicar texturas, sombras, iluminación especular, iluminación difusa y otros efectos especiales en un solo paso.

Para usar la combinación de texturas, la aplicación debe comprobar primero si el hardware del usuario la admite. Esta información se encuentra en el miembro TextureCaps de la [**estructura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Para obtener más información sobre cómo consultar las funcionalidades de combinación de texturas del hardware del usuario, vea [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Fases de textura y la cascada de mezcla de textura

Direct3D admite la combinación de varias texturas de paso único mediante el uso de fases de textura. Una fase de textura toma dos argumentos y realiza una operación de combinación en ellos, pasando el resultado para su posterior procesamiento o para la rasterización. Puede visualizar una fase de textura como se muestra en el diagrama siguiente.

![diagrama de una fase de textura](images/texstg.png)

Como se muestra en el diagrama anterior, las fases de textura mezclan dos argumentos mediante un operador especificado. Entre las operaciones comunes se incluyen la simple relación o la adición de los componentes alfa o de color de los argumentos, pero se admiten más de dos docenas de operaciones. Los argumentos de una fase pueden ser una textura asociada, el color iterado o alfa (iterado durante el sombreado de Gouraud), el color arbitrario y alfa, o el resultado de la fase de textura anterior. Para obtener más información, vea Operaciones y argumentos de mezcla [de textura (Direct3D 9).](texture-blending-operations-and-arguments.md)

> [!Note]  
> Direct3D distingue la combinación de colores de la combinación alfa. Las aplicaciones establecen operaciones y argumentos de combinación para color y alfa individualmente, y los resultados de esa configuración son independientes entre sí.

 

La combinación de argumentos y operaciones que usan varias fases de combinación definen un lenguaje de mezcla basado en flujo simple. Los resultados de una fase fluyen a otra fase, de esa fase a la siguiente, y así sucesivamente. El concepto de resultados que fluyen de una fase a otra para que finalmente se rasterizan en un polígono se suele denominar cascada de mezcla de textura. En el diagrama siguiente se muestra cómo las fases de textura individuales integran la cascada de mezcla de textura.

![diagrama de las fases de textura en la cascada de mezcla de textura](images/tcascade.png)

Cada fase de un dispositivo tiene un índice de base cero. Direct3D permite hasta ocho fases de combinación, aunque siempre debe comprobar las funcionalidades del dispositivo para determinar cuántas fases admite el hardware actual. La primera fase de mezcla está en el índice 0, la segunda está en 1, y así sucesivamente, hasta el índice 7. El sistema combina fases en orden de índice creciente.

Use solo el número de fases que necesita; las fases de combinación no utilizadas están deshabilitadas de forma predeterminada. Por lo tanto, si la aplicación solo usa las dos primeras fases, solo necesita establecer operaciones y argumentos para las fases 0 y 1. El sistema combina las dos fases y omite las fases deshabilitadas.

> [!Note]  
> Si la aplicación varía el número de fases que usa para diferentes situaciones (por ejemplo, cuatro fases para algunos objetos y solo dos para otras), no es necesario deshabilitar explícitamente todas las fases usadas anteriormente. Una opción es deshabilitar la operación de color para la primera fase sin usar y, a continuación, no se aplicarán todas las fases con un índice superior. Otra opción es deshabilitar por completo la asignación de textura estableciendo la operación de color de la primera fase de textura (fase 0) en D3DTOP \_ DISABLE. Una tercera opción es cuando una fase de textura tiene D3DTSS COLORARG1 igual a D3DTA TEXTURE y el puntero de textura de la fase es NULL, esta fase y todas las fases después de que no se \_ \_ procesen. 

 

En los temas siguientes se incluye información adicional.

-   [Operaciones y argumentos de mezcla de textura (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Asignar las texturas actuales (Direct3D 9)](assigning-the-current-textures.md)
-   [Crear fases de mezcla (Direct3D 9)](creating-blending-stages.md)
-   [Combinación de textura alfa (Direct3D 9)](alpha-texture-blending.md)
-   [Mezcla de textura multipass (Direct3D 9)](multipass-texture-blending.md)
-   [Asignación de luz con texturas (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
