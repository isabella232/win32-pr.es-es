---
description: Opciones de compilación de HLSL.
ms.assetid: vs|directx_sdk|~\d3d10_shader.htm
title: Constantes de D3D10_SHADER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16480e2aceada7f5ed05912eca59cc88886ac9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496439"
---
# <a name="d3d10_shader-constants"></a>D3D10 \_ constantes de sombreador

Opciones de compilación de HLSL.



| \#define                                        | Descripción                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Sombreador de D3D10 \_ evitar el control de \_ flujo \_             | Indique al compilador que no permita el control de flujo (cuando sea posible).                                                                                                                                                                                       |
| \_Depuración de sombreador D3D10 \_                            | Inserte la información de archivo de depuración/línea/tipo/símbolo.                                                                                                                                                                                                |
| El \_ sombreador D3D10 \_ habilita la \_ rigurosidad               | De forma predeterminada, el compilador de HLSL deshabilita la limitación en la sintaxis desusada. Si se especifica esta marca, se habilita la limitación, lo que podría no permitir la sintaxis heredada.                                                                                         |
| \_Sombreador D3D10 \_ habilitar \_ compatibilidad con versiones anteriores \_ | Esto permite a los sombreadores más antiguos compilar en 4 \_ destinos.                                                                                                                                                                                         |
| D3D10 \_ Shader \_ Force \_ vs \_ software \_ no \_ OPT     | Compilar un sombreador de vértices para el siguiente perfil de sombreador más alto. Esta opción activa la depuración (y optimiza la desactivación).                                                                                                                           |
| \_Sombreador D3D10 \_ Force \_ \_ Software PS \_ no \_ OPT     | Compilar un sombreador de píxeles para el siguiente perfil del sombreador más alto. Esta opción activa la depuración (y optimiza la desactivación).                                                                                                                            |
| D3D10 del \_ sombreador \_ IEEE \_                 | Habilita la limitación IEEE.                                                                                                                                                                                                                       |
| \_Sombreador de D3D10 \_ sin \_ sombreador                    | Deshabilita los sombreadores. El uso de esta marca hará que el compilador no extraiga la expresión estática para su evaluación.                                                                                                                                 |
| D3D10 \_ optimización del sombreador \_ \_ LEVEL0             | Nivel de optimización más bajo. Puede generar código más lento, pero lo hará más rápidamente. Esto puede resultar útil en un ciclo de desarrollo de sombreador muy iterativo.                                                                                             |
| D3D10 \_ optimización del sombreador \_ \_ Level1             | Segundo nivel de optimización inferior.                                                                                                                                                                                                              |
| D3D10 \_ optimización del sombreador \_ \_ LEVEL2             | Segundo nivel de optimización más alto.                                                                                                                                                                                                             |
| D3D10 \_ optimización del sombreador \_ \_ level3             | Nivel de optimización más alto. Producirá el mejor código posible, pero puede tardar mucho más tiempo en hacerlo. Esto será útil para las compilaciones finales de una aplicación donde el rendimiento es el factor más importante.                                 |
| D3D10 \_ fila de matriz del módulo de sombreador \_ \_ \_ \_ principal         | A menos que se especifique explícitamente, las matrices se empaquetarán en orden principal de fila en la entrada y la salida del sombreador.                                                                                                                                   |
| D3D10 \_ columna de matriz del módulo de sombreador \_ \_ \_ \_ principal      | A menos que se especifique explícitamente, las matrices se empaquetarán en el orden principal de la columna en la entrada y la salida del sombreador. Esto suele ser más eficaz, ya que permite que se realice la multiplicación de matrices vectoriales mediante una serie de productos de punto. |
| \_Precisión parcial del sombreador D3D10 \_ \_               | Forzar que todos los cálculos se realicen con precisión parcial; Esto puede ejecutarse más rápido en el hardware.                                                                                                                                                |
| El \_ sombreador D3D10 \_ prefiere el \_ control de flujo \_            | Indique al compilador que use Flow-Control (cuando sea posible).                                                                                                                                                                                             |
| \_ \_ Omitir optimización de sombreador de D3D10 \_               | Omitir optimización durante la generación de código; se suele recomendar solo para la depuración.                                                                                                                                                                |
| \_ \_ Omitir validación de sombreador de D3D10 \_                 | No valide el código generado con respecto a las capacidades y restricciones conocidas. Úselo solo con los sombreadores que se hayan compilado correctamente en el pasado. Los sombreadores siempre se validan mediante DirectX antes de que se establezcan en el dispositivo.         |
| Las \_ advertencias del sombreador D3D10 \_ \_ son \_ errores            | Informe al compilador de HLSL para que trate todas las advertencias como errores al compilar el código del sombreador. En el caso del nuevo código del sombreador, debe usar esta opción para resolver todas las advertencias y garantizar el menor número posible de defectos de código difíciles de encontrar.             |



 

Estas constantes se definen como macros en d3d10shader. h.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Constantes de sombreador](d3d10-graphics-reference-d3d10-shader-constants.md)
</dt> </dl>

 

 



