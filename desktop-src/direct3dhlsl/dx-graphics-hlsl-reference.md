---
title: Referencia de HLSL
description: La documentación de referencia de HLSL especifica las características del lenguaje. Se divide en varias secciones.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076109"
---
# <a name="reference-for-hlsl"></a>Referencia de HLSL

La documentación de referencia de HLSL especifica las características del lenguaje. Se divide en varias secciones.

-   [Sintaxis del lenguaje (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) : los sombreadores de programación en HLSL requieren que comprenda la sintaxis del lenguaje, es decir, cómo se escribe el código HLSL. Esto incluye el código para declarar e inicializar variables, escribir funciones de sombreador definidas por el usuario y agregar instrucciones de control de flujo para que las funciones sean más eficaces.
-   [Modelos de sombreador frente a perfiles de sombreador](dx-graphics-hlsl-models.md) : el compilador de HLSL implementa reglas y restricciones basadas en modelos de sombreador. El código de cada sombreador de vértices, sombreador de geometría (si se usa Direct3D 10) y sombreador de píxeles se validan con respecto a un modelo de sombreador, que se proporciona en tiempo de compilación.
-   [**Funciones intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) : HLSL tiene muchas funciones intrínsecas. Estas se implementan y prueban para que pueda usarlas sabiendo que ya están depuradas y funcionan bien. Si decide escribir sus propias funciones, consulte la sección sintaxis del lenguaje para escribir funciones definidas por el usuario.
-   [Referencia del sombreador de ASM](dx9-graphics-reference-asm.md) : instrucciones de ensamblado que puede usar para programar y depurar sombreadores.
-   [Referencia de D3DCompiler](dx-graphics-d3dcompiler-reference.md) : compila el origen HLSL sin formato.
-   [Referencia de conversión de formato en línea](inline-format-conversion-reference.md) : el \_ archivo D3DX DXGIFormatConvert. INL contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o en el sombreador de píxeles en el hardware de Direct3D 11. Puede usar estas funciones en la aplicación para leer y escribir simultáneamente en una textura. Es decir, puede realizar la edición en contexto de la imagen. Para usar estas funciones de conversión de formato en línea, incluya el \_ archivo D3DX DXGIFormatConvert. INL en la aplicación.
-   [Apéndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md) : el apéndice está incluido para la integridad. Incluye una lista de las palabras clave y las palabras reservadas; estas palabras no se pueden usar como identificadores en los programas. También incluye una lista de gramática de idioma para referencia.
-   [**Advertencias y errores de HLSL**](hlsl-errors-and-warnings.md) : proporciona códigos de error y de advertencia que un sombreador puede devolver.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




