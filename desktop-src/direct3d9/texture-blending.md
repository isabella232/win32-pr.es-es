---
description: Direct3D puede mezclar hasta ocho texturas en primitivos en un solo paso.
ms.assetid: vs|directx_sdk|~\texture_blending.htm
title: Combinación de texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a89a87160bb85c1f62339380d46fa4b39736609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806865"
---
# <a name="texture-blending-direct3d-9"></a>Combinación de texturas (Direct3D 9)

Direct3D puede mezclar hasta ocho texturas en primitivos en un solo paso. El uso de varias combinaciones de texturas puede aumentar la velocidad de fotogramas de una aplicación Direct3D. Una aplicación emplea varias combinaciones de texturas para aplicar texturas, sombras, iluminación especular, iluminación difusa y otros efectos especiales en un solo paso.

Para usar la combinación de texturas, la aplicación debe comprobar primero si el hardware del usuario lo admite. Esta información se encuentra en el miembro TextureCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Para obtener más información sobre cómo consultar el hardware del usuario para ver las funcionalidades de combinación de texturas, vea [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="texture-stages-and-the-texture-blending-cascade"></a>Fases de textura y la combinación de texturas en cascada

Direct3D admite la combinación de varias texturas de un solo paso mediante el uso de fases de textura. Una fase de textura toma dos argumentos y realiza una operación de combinación en ellos, pasando el resultado para su posterior procesamiento o para la rasterización. Puede visualizar una fase de textura, tal como se muestra en el diagrama siguiente.

![diagrama de una fase de textura](images/texstg.png)

Como se muestra en el diagrama anterior, las fases de textura fusionan dos argumentos mediante el uso de un operador especificado. Las operaciones comunes incluyen una modulación simple o la adición de los componentes de color o alfa de los argumentos, pero se admiten más de dos docenas de operaciones. Los argumentos de una fase pueden ser una textura asociada, el color iterado o alfa (iterado durante el sombreado Gouraud), el color arbitrario y alfa, o el resultado de la fase de textura anterior. Para obtener más información, vea [operaciones y argumentos de combinación de texturas (Direct3D 9)](texture-blending-operations-and-arguments.md).

> [!Note]  
> Direct3D distingue la combinación de colores de la combinación alfa. Las aplicaciones establecen operaciones y argumentos de mezcla para el color y alfa individualmente, y los resultados de esos valores son independientes entre sí.

 

La combinación de argumentos y operaciones que se usan en varias fases de mezcla define un sencillo lenguaje de fusión basado en el flujo. Los resultados de una fase fluyen hacia abajo hasta otra fase, desde esa fase hasta el siguiente, y así sucesivamente. El concepto de los resultados que fluyen desde la fase hasta el final se rasteriza en un polígono a menudo se denomina cascada de fusión de texturas. En el diagrama siguiente se muestra cómo las fases de textura individuales componen la combinación de texturas en cascada.

![diagrama de fases de textura en cascada de fusión de texturas](images/tcascade.png)

Cada fase de un dispositivo tiene un índice basado en cero. Direct3D permite hasta ocho fases de fusión, aunque siempre debe comprobar las capacidades del dispositivo para determinar el número de fases que admite el hardware actual. La primera fase de mezcla está en el índice 0, la segunda está en 1, y así sucesivamente hasta el índice 7. El sistema combina las fases para aumentar el orden de los índices.

Use solo el número de fases que necesite; las fases de fusión no utilizadas están deshabilitadas de forma predeterminada. Por lo tanto, si la aplicación solo usa las dos primeras fases, solo necesita las operaciones y los argumentos establecidos para la fase 0 y 1. El sistema combina las dos fases y omite las fases deshabilitadas.

> [!Note]  
> Si la aplicación varía el número de fases que usa para diferentes situaciones, como cuatro fases para algunos objetos y solo dos para otros, no es necesario deshabilitar explícitamente todas las fases usadas previamente. Una opción es deshabilitar la operación de color de la primera fase sin usar; no se aplicarán todas las fases con un índice superior. Otra opción consiste en deshabilitar la asignación de texturas por completo estableciendo la operación de color de la primera fase de textura (fase 0) en D3DTOP \_ deshabilitar. Una tercera opción es cuando una fase de textura tiene D3DTSS \_ COLORARG1 igual a \_ textura D3DTA y el puntero de textura para la fase es **null**, esta fase y todas las fases después no se procesan.

 

En los temas siguientes se incluye información adicional.

-   [Operaciones y argumentos de combinación de texturas (Direct3D 9)](texture-blending-operations-and-arguments.md)
-   [Asignar las texturas actuales (Direct3D 9)](assigning-the-current-textures.md)
-   [Crear fases de fusión (Direct3D 9)](creating-blending-stages.md)
-   [Combinación de texturas alfa (Direct3D 9)](alpha-texture-blending.md)
-   [Combinación de texturas de Multipass (Direct3D 9)](multipass-texture-blending.md)
-   [Asignación de luz con texturas (Direct3D 9)](light-mapping-with-textures.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
