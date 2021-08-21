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
ms.openlocfilehash: a1ef04c14682aa6e763222fd0c8db0e2eedf33abf747da97a16b2b1621e1c42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119749"
---
# <a name="using-shaders-in-direct3d-9"></a>Usar sombreadores en Direct3D 9

-   [Compilar un sombreador para hardware específico](#compiling-a-shader-for-specific-hardware)
-   [Inicialización de constantes de sombreador](#initializing-shader-constants)
-   [Enlazar un parámetro de sombreador a un registro determinado](#binding-a-shader-parameter-to-a-particular-register)
-   [Representación de un sombreador programable](#rendering-a-programmable-shader)
-   [Depurar sombreadores](#debugging-shaders)
-   [Temas relacionados](#related-topics)

## <a name="compiling-a-shader-for-specific-hardware"></a>Compilar un sombreador para hardware específico

Los sombreadores se agregaron por primera vez a Microsoft DirectX en DirectX 8.0. En ese momento, se definieron varias máquinas de sombreador virtual, cada una aproximadamente correspondiente a un procesador de gráficos determinado generado por los principales proveedores de gráficos 3D. Para cada una de estas máquinas de sombreador virtual, se diseñó un lenguaje de ensamblado. Los programas escritos en los modelos de sombreador (nombres frente a \_ \_ 1 1 y ps \_ \_ 1 1 - ps \_ 1 \_ 4) eran relativamente cortos y, por lo general, los desarrolladores los escribieron directamente en el lenguaje de ensamblado adecuado. La aplicación pasaría este código de lenguaje de ensamblado legible a la biblioteca D3DX mediante [**D3DXAssembleShader**](/windows/desktop/direct3d9/d3dxassembleshader) y recuperaría una representación binaria del sombreador que, a su vez, se pasaría mediante [**CreateVertexShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) o [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader). Para más información, consulte el kit de desarrollo de software (SDK).

La situación en Direct3D 9 es similar. Una aplicación pasa un sombreador HLSL a D3DX mediante [**D3DXCompileShader**](/windows/desktop/direct3d9/d3dxcompileshader) y obtiene una representación binaria del sombreador compilado que, a su vez, se pasa a Microsoft Direct3D mediante [**CreatePixelShader**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createpixelshader) [**o CreateVertexShader.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createvertexshader) El tiempo de ejecución no sabe nada sobre HLSL, solo los modelos de sombreador de ensamblados binarios. Esto es bueno porque significa que el compilador HLSL se puede actualizar independientemente del tiempo de ejecución de Direct3D. También puede compilar sombreadores sin conexión mediante [fxc](/windows/desktop/direct3dtools/fxc).

Además del desarrollo del compilador HLSL, Direct3D 9 también introdujo los modelos de sombreador de nivel de ensamblado para exponer la funcionalidad de la última generación de hardware gráfico. Los desarrolladores de aplicaciones pueden trabajar en ensamblado para estos nuevos modelos (frente a \_ 2 \_ 0, frente a \_ 3 \_ 0, ps \_ 2 \_ 0, ps \_ 3 0), \_ pero esperamos que la mayoría de los desarrolladores pasen a HLSL para el desarrollo de sombreadores.

Por supuesto, la capacidad de escribir un programa HLSL para expresar un algoritmo de sombreado determinado no le permite ejecutarse automáticamente en ningún hardware determinado. Una aplicación llama a D3DX para compilar un sombreador en código de ensamblado binario [**con D3DXCompileShader.**](/windows/desktop/direct3d9/d3dxcompileshader) Una de las limitaciones de este punto de entrada es un parámetro que define cuál de los modelos de nivel de ensamblado (o destinos de compilación) debe usar el compilador HLSL para expresar el código final del sombreador. Si una aplicación está realizando la compilación del sombreador HLSL en tiempo de ejecución (en lugar del tiempo de compilación o sin conexión), la aplicación podría examinar las funcionalidades del dispositivo Direct3D y seleccionar el destino de compilación para que coincida. Si el algoritmo expresado en el sombreador HLSL es demasiado complejo para ejecutarse en el destino de compilación seleccionado, se producirá un error en la compilación. Esto significa que, aunque HLSL es una gran ventaja para el desarrollo de sombreadores, no libera a los desarrolladores de las realidades de envío de juegos a un público objetivo con dispositivos gráficos de funcionalidades variables. Como desarrollador de juegos, todavía tiene que administrar un enfoque por niveles para los objetos visuales. Esto significa escribir mejores sombreadores para tarjetas gráficas más capaces y escribir versiones más básicas para tarjetas anteriores. Sin embargo, con HLSL bien escrito, esta carga se puede reducir significativamente.

En lugar de compilar sombreadores HLSL mediante D3DX en el equipo del cliente en el momento de la carga de la aplicación o en el primer uso, muchos desarrolladores eligen compilar su sombreador de HLSL en código de ensamblado binario antes de que se envíe. Esto mantiene su código fuente HLSL lejos de los ojos abiertos y también garantiza que todos los sombreadores que su aplicación ejecutará alguna vez han pasado por su proceso interno de control de calidad. Una utilidad práctica para compilar sombreadores sin conexión es [fxc](/windows/desktop/direct3dtools/fxc). Esta herramienta tiene una serie de opciones que puede usar para compilar código para el destino de compilación especificado. Estudiar la salida desensamblada puede ser muy educativo durante el desarrollo si desea optimizar los sombreadores o simplemente conocer las funcionalidades de la máquina virtual de sombreador en un nivel más detallado. Estas opciones se resumen a continuación:

## <a name="initializing-shader-constants"></a>Inicialización de constantes de sombreador

Las constantes del sombreador están contenidas en la tabla constante. Se puede acceder a él con la [**interfaz ID3DXConstantTable.**](/windows/desktop/direct3d9/id3dxconstanttable) Las variables de sombreador global se pueden inicializar en el código del sombreador. Estos se inicializan en tiempo de ejecución mediante una llamada [**a SetDefaults**](/windows/desktop/direct3d9/id3dxconstanttable--setdefaults).

## <a name="binding-a-shader-parameter-to-a-particular-register"></a>Enlazar un parámetro de sombreador a un registro determinado

El compilador asignará automáticamente registros a variables globales. El compilador asignaría Environment a sampler register s0, SparkleNoise a sampler register s1 y k s a constant register c0 (suponiendo que no se haya asignado ningún otro sampler o registro constante) para las tres \_ variables globales siguientes:


```
sampler Environment;
sampler SparkleNoise;
float4 k_s;
```



También es posible enlazar variables a un registro específico. Para forzar que el compilador se asigne a un registro determinado, use la sintaxis siguiente:


```
register(RegisterName)
```



donde RegisterName es el nombre del registro específico. En los ejemplos siguientes se muestra la sintaxis de asignación de registro específica, donde el entorno de sampler se enlazará al registro de sampler s1, SparkleNoise se enlazará al registro de sampler s0 y k s se enlazará al registro \_ constante c12:


```
sampler Environment : register(s1);
sampler SparkleNoise : register(s0);
float4 k_s : register(c12);
```



## <a name="rendering-a-programmable-shader"></a>Representación de un sombreador programable

Un sombreador se representa estableciendo el sombreador actual en el dispositivo, inicializando las constantes del sombreador, contando al dispositivo de dónde vienen los datos de entrada variables y, por último, representando las primitivas. Cada uno de ellos se puede lograr mediante una llamada a los métodos siguientes, respectivamente:

-   [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)
-   [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)
-   [**SetStreamSource**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource)
-   [**DrawPrimitive**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-drawprimitive)

## <a name="debugging-shaders"></a>Depurar sombreadores

La extensión DirectX para Microsoft Visual Studio .NET proporciona un depurador HLSL totalmente integrado dentro Visual Studio entorno de desarrollo integrado (IDE) de .NET. Para prepararse para la depuración del sombreador, debe instalar las herramientas adecuadas en el equipo (consulte Depuración de [sombreadores en Visual Studio (Direct3D 9)](dx-graphics-hlsl-debug-visual-studio.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 