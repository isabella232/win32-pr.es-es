---
title: Usar sombreadores en Direct3D 9
description: Usar sombreadores en Direct3D 9
ms.assetid: 8d8f5124-fbf3-4af5-8399-43ba28aa6eb9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6455b47d24c1c83683ce8b85c48990bb32e221ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997048"
---
# <a name="using-shaders-in-direct3d-9"></a>Usar sombreadores en Direct3D 9

-   [Compilar un sombreador para hardware específico](#compiling-a-shader-for-specific-hardware)
-   [Inicializar constantes de sombreador](#initializing-shader-constants)
-   [Enlazar un parámetro de sombreador a un registro determinado](#binding-a-shader-parameter-to-a-particular-register)
-   [Representar un sombreador programable](#rendering-a-programmable-shader)
-   [Depurar sombreadores](#debugging-shaders)
-   [Temas relacionados](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Compilar un sombreador para hardware específico

Los sombreadores se agregaron por primera vez a Microsoft DirectX en DirectX 8,0. En ese momento, se definieron varias máquinas de sombreador virtual, cada una de las cuales corresponde aproximadamente a un procesador de gráficos determinado producido por los principales proveedores de gráficos 3D. Para cada uno de estos equipos de sombreador virtual, se diseñó un lenguaje de ensamblado. Los programas escritos en los modelos de sombreador (nombres frente a \_ 1 \_ 1 y PS 1 \_ \_ 1-PS \_ 1 \_ 4) fueron relativamente cortos y, por lo general, los escribieron los desarrolladores directamente en el lenguaje de ensamblado adecuado. La aplicación pasaría este código de lenguaje de ensamblado legible a la biblioteca de D3DX mediante [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) y obtener una representación binaria del sombreador que, a su vez, se pasaría con [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) o [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader). Para obtener más información, vea el kit de desarrollo de software (SDK) de.

La situación en Direct3D 9 es similar. Una aplicación pasa un sombreador HLSL a D3DX mediante [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) y devuelve una representación binaria del sombreador compilado que, a su vez, se pasa a Microsoft Direct3D mediante [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) o [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader). El runtime no sabe nada sobre HLSL, solo los modelos de sombreador de ensamblados binarios. Esto es muy útil porque significa que el compilador de HLSL se puede actualizar independientemente del tiempo de ejecución de Direct3D. También puede compilar sombreadores sin conexión mediante [FXC](/windows/desktop/direct3dtools/fxc).

Además del desarrollo del compilador de HLSL, Direct3D 9 también incorporó los modelos de sombreador de nivel de ensamblado para exponer la funcionalidad de la última generación de hardware de gráficos. Los desarrolladores de aplicaciones pueden trabajar en ensamblados para estos nuevos modelos (vs \_ 2 \_ 0, vs \_ 3 \_ 0, PS \_ 2 \_ 0, PS \_ 3 \_ 0), pero esperamos que la mayoría de los desarrolladores pasen a HLSL para el desarrollo del sombreador.

Por supuesto, la capacidad de escribir un programa HLSL para expresar un algoritmo de sombreado determinado no permite que se ejecute automáticamente en ningún hardware determinado. Una aplicación llama a D3DX para compilar un sombreador en el código de ensamblado binario con [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader). Una de las limitaciones de este punto de entrada es un parámetro que define cuál de los modelos de nivel de ensamblado (o destinos de compilación) debe usar el compilador de HLSL para expresar el código del sombreador final. Si una aplicación está realizando la compilación del sombreador HLSL en tiempo de ejecución (en lugar del tiempo de compilación o sin conexión), la aplicación podría examinar las capacidades del dispositivo Direct3D y seleccionar el destino de compilación para que coincida. Si el algoritmo expresado en el sombreador HLSL es demasiado complejo para ejecutarse en el destino de compilación seleccionado, se producirá un error en la compilación. Esto significa que, aunque HLSL es una gran ventaja para el desarrollo del sombreador, no libera a los desarrolladores de las realidades de la entrega de juegos a una audiencia de destino con dispositivos gráficos de distintas funcionalidades. Como desarrollador de juegos, todavía tiene que administrar un enfoque en capas para los objetos visuales; Esto significa que se escriben mejores sombreadores para tarjetas gráficas más capaces y se escriben versiones más básicas para tarjetas más antiguas. Sin embargo, con HLSL bien escrito, esta carga se puede simplificar considerablemente.

En lugar de compilar sombreadores HLSL con D3DX en el equipo del cliente en el momento de la carga de la aplicación o al usarse por primera vez, muchos desarrolladores optan por compilar su sombreador de HLSL en código de ensamblado binario antes de que se envíen. Esto mantiene el código fuente de HLSL fuera de los ojos no contratados y también garantiza que todos los sombreadores que su aplicación ejecuten se han pasado por su proceso de control de calidad interno. Una utilidad adecuada para compilar sombreadores sin conexión es [FXC](/windows/desktop/direct3dtools/fxc). Esta herramienta tiene una serie de opciones que puede usar para compilar código para el destino de compilación especificado. Estudiar la salida desensamblada puede ser muy educativo durante el desarrollo si desea optimizar los sombreadores o, por lo general, conocer las funcionalidades de la máquina del sombreador virtual en un nivel más detallado. Estas opciones se resumen a continuación:

## <a name="initializing-shader-constants"></a>Inicializar constantes de sombreador

Las constantes de sombreador están contenidas en la tabla de constantes. Se puede tener acceso a este a través de la interfaz [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) . Las variables de sombreador global se pueden inicializar en el código del sombreador. Se inicializan en tiempo de ejecución mediante una llamada a [**SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Enlazar un parámetro de sombreador a un registro determinado

El compilador asignará automáticamente los registros a las variables globales. El compilador asignaría el entorno al registro de muestra S0, SparkleNoise al registro de muestra S1 y k \_ s al registro constante C0 (suponiendo que ya no se asignaron otros registros de muestra o de constantes) para las tres variables globales siguientes:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



También es posible enlazar variables a un registro específico. Para forzar al compilador a que se asigne a un registro determinado, use la siguiente sintaxis:


```
register(RegisterName)
```



donde RegisterName es el nombre del registro específico. En los siguientes ejemplos se muestra la sintaxis de asignación de registro específica, en la que el entorno de muestra se enlazará al registro de muestra S1, SparkleNoise se enlazará al registro de muestra S0 y k \_ s se enlazará al registro constante C12:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Representar un sombreador programable

Un sombreador se representa estableciendo el sombreador actual en el dispositivo, Inicializando las constantes del sombreador, indicando el dispositivo del que proceden los distintos datos de entrada y, por último, la representación de los primitivos. Cada una de ellas se puede realizar mediante una llamada a los métodos siguientes, respectivamente:

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Depurar sombreadores

La extensión de DirectX para Microsoft Visual Studio .NET proporciona un depurador de HLSL totalmente integrado en el entorno de desarrollo integrado (IDE) de Visual Studio .NET. Para preparar la depuración del sombreador, debe instalar las herramientas adecuadas en el equipo (consulte [depuración de sombreadores en Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 