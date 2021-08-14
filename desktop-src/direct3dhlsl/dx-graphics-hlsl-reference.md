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
ms.openlocfilehash: 425dc1d56801bbbd6b73429d8d17024a78dffe47a045ec6b34d5cd45b752bcca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513860"
---
# <a name="reference-for-hlsl"></a>Referencia de HLSL

La documentación de referencia de HLSL especifica las características del lenguaje. Se divide en varias secciones.

-   [Sintaxis de lenguaje (DirectX HLSL):](dx-graphics-hlsl-language-syntax.md) la programación de sombreadores en HLSL requiere que comprenda la sintaxis del lenguaje, es decir, cómo escribir código HLSL. Esto incluye código para declarar e inicializar variables, escribir funciones de sombreador definidas por el usuario y agregar instrucciones de control de flujo para que las funciones sea más eficaces.
-   [Modelos de sombreador frente a perfiles de sombreador:](dx-graphics-hlsl-models.md) el compilador HLSL implementa reglas y restricciones basadas en modelos de sombreador. El código de cada sombreador de vértices, sombreador de geometría (si usa Direct3D 10) y sombreador de píxeles se validan con un modelo de sombreador, que se proporciona en tiempo de compilación.
-   [**Funciones intrínsecas (DirectX HLSL):**](dx-graphics-hlsl-intrinsic-functions.md) HLSL tiene muchas funciones intrínsecas. Estos se implementan y prueban para que pueda usarlos sabiendo que ya están depurados y que tienen un buen rendimiento. Si decide escribir sus propias funciones, consulte la sección sintaxis del lenguaje para escribir funciones definidas por el usuario.
-   [Referencia de sombreador de Asm:](dx9-graphics-reference-asm.md) instrucciones de ensamblado que puede usar para programar y depurar sombreadores.
-   [Referencia de D3DCompiler:](dx-graphics-d3dcompiler-reference.md) compila el origen HLSL sin formato.
-   [Referencia](inline-format-conversion-reference.md) de conversión de formato en línea: el archivo D3DX DXGIFormatConvert.inl contiene funciones de conversión de formato en línea que puede usar en el sombreador de cálculo o el sombreador de píxeles en el hardware de \_ Direct3D 11. Puede usar estas funciones en la aplicación para leer y escribir simultáneamente en una textura. Es decir, puede realizar la edición de imágenes en contexto. Para usar estas funciones de conversión de formato insertadas, incluya el archivo D3DX \_ DXGIFormatConvert.inl en la aplicación.
-   [Apéndice (DirectX HLSL):](dx-graphics-hlsl-appendix.md) el apéndice se incluye para su integridad. Incluye una lista de las palabras clave y las palabras reservadas. estas palabras no se pueden usar como identificadores en los programas. También incluye una lista de la gramática del lenguaje como referencia.
-   [**Errores y advertencias hlsl:**](hlsl-errors-and-warnings.md) proporciona códigos de error y advertencia que un sombreador puede devolver.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HLSL](dx-graphics-hlsl.md)
</dt> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




