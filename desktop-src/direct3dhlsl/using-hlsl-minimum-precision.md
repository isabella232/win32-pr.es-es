---
title: Usar precisión mínima de HLSL
description: A partir de Windows 8, los controladores de gráficos pueden implementar tipos de datos escalares HLSL de precisión mínima con cualquier precisión mayor o igual que la precisión de bits especificada.
ms.assetid: 422B0C45-5CEB-4235-AD05-62D36C36CFC6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7f66f35aef3e870edb4e8564a280be89ce34be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792274"
---
# <a name="using-hlsl-minimum-precision"></a>Usar precisión mínima de HLSL

A partir de Windows 8, los controladores de gráficos pueden implementar [tipos de datos escalares HLSL](dx-graphics-hlsl-scalar.md) de precisión mínima con cualquier precisión mayor o igual que la precisión de bits especificada. Cuando el código del sombreador de precisión mínima de HLSL se usa en hardware que implementa la precisión mínima de HLSL, se usa menos ancho de banda de memoria y, como resultado, también se usa menos energía del sistema.

Puede consultar la compatibilidad de precisión mínima que proporciona el controlador de gráficos llamando a [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) con el valor de [**\_ \_ \_ \_ \_ compatibilidad de precisión mínima del sombreador de características de D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) . Para obtener más información, consulte [compatibilidad con precisión mínima de HLSL](/windows/desktop/direct3d11/direct3d-11-1-features).

-   [Declarar variables con tipos de datos de precisión mínimos](#declare-variables-with-minimum-precision-data-types)
-   [Probar el código del sombreador de precisión mínima](#testing-your-minimum-precision-shader-code)
-   [Temas relacionados](#related-topics)

## <a name="declare-variables-with-minimum-precision-data-types"></a>Declarar variables con tipos de datos de precisión mínimos

Para usar la precisión mínima en el código del sombreador HLSL, declare las variables individuales con tipos como **min16float** (**min16float4** para un vector), **min16int**, **min10float**, etc. Con estas variables, el código del sombreador indica que no requiere más precisión de lo que indican las variables. Pero el hardware puede pasar por alto los indicadores de precisión mínima y ejecutarse en una precisión completa de 32 bits. Cuando el código del sombreador se usa en hardware que aprovecha la precisión mínima, se usa menos ancho de banda de memoria y, como resultado, también se usa menos energía del sistema siempre que el código del sombreador no espere más precisión de lo especificado.

No es necesario crear varios sombreadores que no utilicen la precisión mínima. En su lugar, cree sombreadores con precisión mínima y las variables de precisión mínima se comportan en una precisión completa de 32 bits si el controlador de gráficos informa de que no admite ninguna precisión mínima. Los sombreadores de precisión mínima de HLSL no funcionan en sistemas operativos anteriores a Windows 8, por lo que si planea dirigirse a sistemas operativos anteriores, tendrá que crear varios sombreadores, otros que sí lo hacen y otros que no usan la precisión mínima.

> [!Note]  
> No haga que los datos cambien entre distintos niveles de precisión dentro de un sombreador porque estos tipos de conversiones son excesivos y reducen el rendimiento. La excepción es que las constantes de sombreador siguen siendo siempre de 32 bits, pero los proveedores pueden diseñar hardware de gráficos que se puede reducir libremente a cualquier precisión inferior que la lectura de instrucciones de HLSL pueda usar.

 

Al usar la precisión mínima, puede controlar la precisión de los cálculos en varias partes del código del sombreador.

Las reglas de precisión mínima de HLSL son similares a C/C++, donde los tipos de una expresión determinan la precisión de la operación, no el tipo en el que finalmente se escribe.

## <a name="testing-your-minimum-precision-shader-code"></a>Probar el código del sombreador de precisión mínima

El rasterizador de referencia [**( \_ \_ \_ referencia de tipo de controlador D3D**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) le ofrece una idea aproximada de cómo se comporta la precisión mínima en el código del sombreador HLSL al cuantificar cada instrucción de HLSL a la precisión especificada. Esto le ayuda a detectar código que podría confiar accidentalmente en más de la precisión mínima. El rasterizador de referencia no se ejecuta más rápido cuando el código del sombreador HLSL usa la precisión mínima, pero se puede usar para comprobar la exactitud del código. [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) ([**\_ tipo de controlador D3D \_ \_ Warp**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type)) no admite el uso de precisión mínima en el código del sombreador HLSL; WARP solo se ejecuta en una precisión completa de 32 bits.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 