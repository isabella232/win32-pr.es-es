---
title: Uso de la precisión mínima hlsl
description: A partir Windows 8, los controladores gráficos pueden implementar tipos de datos escalares HLSL de precisión mínima mediante cualquier precisión mayor o igual que la precisión de bits especificada.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4981cd80fdd80fbccf1b2610cbfeb210a9894a857fb2d7af1ddd84b9e2772e70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067285"
---
# <a name="using-hlsl-minimum-precision"></a>Uso de la precisión mínima hlsl

A partir Windows 8, los controladores gráficos pueden implementar tipos de datos [escalares HLSL](dx-graphics-hlsl-scalar.md) de precisión mínima mediante cualquier precisión mayor o igual que su precisión de bits especificada. Cuando el código del sombreador de precisión mínima HLSL se usa en hardware que implementa la precisión mínima hlsl, se usa menos ancho de banda de memoria y, como resultado, también se usa menos potencia del sistema.

Puede consultar la compatibilidad de precisión mínima que proporciona el controlador de gráficos llamando a [**ID3D11Device::CheckFeatureSupport con**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) el valor [**D3D11 \_ FEATURE SHADER MIN PRECISION \_ \_ \_ \_ SUPPORT.**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) Para obtener más información, vea [Compatibilidad con la precisión mínima hlsl](/windows/desktop/direct3d11/direct3d-11-1-features).

-   [Declaración de variables con tipos de datos de precisión mínima](#declare-variables-with-minimum-precision-data-types)
-   [Prueba del código de sombreador de precisión mínima](#testing-your-minimum-precision-shader-code)
-   [Temas relacionados](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Declaración de variables con tipos de datos de precisión mínima

Para usar la precisión mínima en el código del sombreador HLSL, declare variables individuales con tipos como **min16float** **(min16float4** para un vector), **min16int,** **min10float,** y así sucesivamente. Con estas variables, el código del sombreador indica que no requiere más precisión de la que indican las variables. Pero el hardware puede omitir los indicadores de precisión mínima y ejecutarse con una precisión completa de 32 bits. Cuando el código del sombreador se usa en hardware que aprovecha la precisión mínima, se usa menos ancho de banda de memoria y, como resultado, también se usa menos potencia del sistema siempre y cuando el código del sombreador no espere más precisión de la especificada.

No es necesario crear varios sombreadores que usen y no usen la precisión mínima. En su lugar, cree sombreadores con precisión mínima y las variables de precisión mínima se comporten con una precisión completa de 32 bits si el controlador de gráficos informa de que no admite ninguna precisión mínima. Los sombreadores de precisión mínima HLSL no funcionan en sistemas operativos anteriores a Windows 8 por lo que si planea dirigirse a sistemas operativos anteriores, deberá crear varios sombreadores, algunos que sí lo hacen y otros que no usan la precisión mínima.

> [!Note]  
> No realice cambios de datos entre distintos niveles de precisión dentro de un sombreador porque estos tipos de conversiones son desaperciba y reducen el rendimiento. La excepción es que las constantes del sombreador siguen siendo siempre de 32 bits, pero los proveedores pueden diseñar hardware gráfico que se pueda convertir libremente a cualquier precisión inferior que pueda usar la lectura de instrucciones HLSL.

 

Con la precisión mínima, puede controlar la precisión de los cálculos en varias partes del código del sombreador.

Las reglas para la precisión mínima hlsl son similares a C/C++, donde los tipos de una expresión determinan la precisión de la operación, no el tipo en el que se escribe finalmente.

## <a name="testing-your-minimum-precision-shader-code"></a>Prueba del código de sombreador de precisión mínima

El rasterizador de referencia ([**D3D \_ DRIVER \_ TYPE \_ REFERENCE**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) proporciona una idea aproximada de cómo se comporta la precisión mínima en el código del sombreador HLSL al cuantificar cada instrucción HLSL en la precisión especificada. Esto le ayuda a detectar código que podría basarse accidentalmente en más de la precisión mínima. El rasterizador de referencia no se ejecuta más rápido cuando el código del sombreador HLSL usa la precisión mínima, pero puede usarlo para comprobar la exactitud del código. [WARP](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) no admite el uso de precisión mínima en el código del sombreador HLSL; WARP solo se ejecuta con una precisión completa de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 