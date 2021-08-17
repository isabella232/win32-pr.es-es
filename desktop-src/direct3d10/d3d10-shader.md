---
description: Opciones de compilación HLSL.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: D3D10_SHADER constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e965c050d3643e80b493875b27ba5a9b774b351487e191584f40297819758f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118303528"
---
# <a name="d3d10_shader-constants"></a>Constantes SHADER de D3D10 \_

Opciones de compilación HLSL.



| \#Definir                                        | Descripción                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SOMBREADOR D3D10 \_ EVITE EL CONTROL DE \_ \_ \_ FLUJO             | Diga al compilador que no permita el control de flujo (cuando sea posible).                                                                                                                                                                                       |
| DEPURACIÓN DEL SOMBREADOR D3D10 \_ \_                            | Inserte la información del archivo de depuración, la línea, el tipo o el símbolo.                                                                                                                                                                                                |
| EL SOMBREADOR D3D10 \_ \_ HABILITA LA \_ STRICTNESS               | De forma predeterminada, el compilador HLSL deshabilita el estricto en la sintaxis en desuso. Si se especifica esta marca, se habilita la estrictaza, lo que puede no permitir la sintaxis heredada.                                                                                         |
| EL SOMBREADOR D3D10 \_ HABILITA LA COMPATIBILIDAD CON VERSIONES \_ \_ \_ ANTERIORES | Esto permite que los sombreadores más antiguos se compilen en 4 \_ 0 destinos.                                                                                                                                                                                         |
| D3D10 \_ SHADER \_ FORCE \_ VS \_ SOFTWARE \_ NO \_ OPT     | Compile un sombreador de vértices para el siguiente perfil de sombreador más alto. Esta opción activa la depuración (y las optimizaciones se desactivan).                                                                                                                           |
| D3D10 \_ SHADER \_ FORCE \_ PS \_ SOFTWARE \_ NO \_ OPT     | Compile un sombreador de píxeles para el siguiente perfil de sombreador más alto. Esta opción activa la depuración (y las optimizaciones se desactivan).                                                                                                                            |
| ESTRICTAD10 DEL \_ SOMBREADOR D3D10 \_ IEEE \_                 | Habilita la integridad de IEEE.                                                                                                                                                                                                                       |
| SOMBREADOR D3D10 \_ \_ SIN \_ PRESHADER                    | Deshabilita los preshaders. El uso de esta marca hará que el compilador no extraiga la expresión estática para la evaluación.                                                                                                                                 |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL0             | Nivel de optimización más bajo. Puede generar código más lento, pero lo hará más rápidamente. Esto puede ser útil en un ciclo de desarrollo de sombreador muy iterativo.                                                                                             |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL1             | Segundo nivel de optimización más bajo.                                                                                                                                                                                                              |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL2             | Segundo nivel de optimización más alto.                                                                                                                                                                                                             |
| D3D10 \_ SHADER \_ OPTIMIZATION \_ LEVEL3             | Nivel de optimización más alto. Producirá el mejor código posible, pero puede tardar mucho más tiempo en hacerlo. Esto será útil para las compilaciones finales de una aplicación donde el rendimiento es el factor más importante.                                 |
| D3D10 \_ SHADER \_ PACK \_ MATRIX \_ ROW \_ MAJOR         | A menos que se especifique explícitamente, las matrices se empaquetarán en orden de fila principal en la entrada y salida del sombreador.                                                                                                                                   |
| COLUMNA PRINCIPAL DE LA MATRIZ DEL \_ \_ PAQUETE DE SOMBRAS \_ \_ D3D10 \_      | A menos que se especifique explícitamente, las matrices se empaquetarán en orden de columna principal en la entrada y salida del sombreador. Por lo general, esto es más eficaz, ya que permite realizar la multiplicación de matrices vectoriales mediante una serie de productos de punto. |
| PRECISIÓN PARCIAL DEL SOMBREADOR D3D10 \_ \_ \_               | Forzar que todos los cálculos se realizan con precisión parcial; esto puede ejecutarse más rápido en algún hardware.                                                                                                                                                |
| SOMBREADOR D3D10 \_ PREFIERE EL CONTROL DE \_ \_ \_ FLUJO            | Diga al compilador que use el control de flujo (cuando sea posible).                                                                                                                                                                                             |
| OPTIMIZACIÓN DE SKIP \_ DEL \_ SOMBREADOR D3D10 \_               | Omitir optimización durante la generación de código; generalmente se recomienda solo para la depuración.                                                                                                                                                                |
| VALIDACIÓN DE SKIP \_ DEL SOMBREADOR D3D10 \_ \_                 | No valide el código generado con las funcionalidades y restricciones conocidas. Use esta opción solo con sombreadores que se hayan compilado correctamente en el pasado. DirectX siempre valida los sombreadores antes de establecerse en el dispositivo.         |
| LAS ADVERTENCIAS DEL SOMBREADOR D3D10 \_ \_ SON \_ \_ ERRORES            | Informe al compilador HLSL de que trate todas las advertencias como errores al compilar el código del sombreador. Para el nuevo código de sombreador, debe usar esta opción para poder resolver todas las advertencias y garantizar el menor número posible de defectos de código difíciles de encontrar.             |



 

Estas constantes se definen como macros en d3d10shader.h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de sombreador](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



