---
description: En este tema se describen las consideraciones y las estrategias de optimización con la biblioteca de DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Optimización del código con la biblioteca de DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11b331077e3d6538952a2f7956641b8b3919e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696712"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Optimización del código con la biblioteca de DirectXMath

En este tema se describen las consideraciones y las estrategias de optimización con la biblioteca de DirectXMath.

-   [Usar descriptores de acceso con moderación](#use-accessors-sparingly)
-   [Usar la configuración de compilación correcta](#use-correct-compilation-settings)
-   [Usar las funciones de est cuando sea necesario](#use-est-functions-when-appropriate)
-   [Usar tipos de datos alineados y operaciones](#use-aligned-data-types-and-operations)
-   [Alinear las asignaciones correctamente](#properly-align-allocations)
-   [Evitar sobrecargas de operador cuando sea posible](#avoid-operator-overloads-when-possible)
-   [Desnormalizados](#denormals)
-   [Sacar provecho de la doble de punto flotante de entero](#take-advantage-of-the-integer-floating-point-duality)
-   [Preferir formularios de plantilla](#prefer-template-forms)
-   [Usar DirectXMath con Direct3D](#using-directxmath-with-direct3d)
-   [Temas relacionados](#related-topics)

## <a name="use-accessors-sparingly"></a>Usar descriptores de acceso con moderación

Las operaciones basadas en vectores usan los conjuntos de instrucciones SIMD y estos hacen uso de registros especiales. El acceso a componentes individuales requiere el traslado de los registros SIMD a los valores escalares y viceversa.

Siempre que sea posible, es más eficaz inicializar todos los componentes de una [**XMVECTOR**](xmvector-data-type.md) al mismo tiempo, en lugar de usar una serie de descriptores de acceso vectoriales individuales.

## <a name="use-correct-compilation-settings"></a>Usar la configuración de compilación correcta

En el caso de los destinos x86 de Windows, habilite/Arch: SSE2. Para todos los destinos de Windows, habilite/FP: Fast.

De forma predeterminada, la compilación en la biblioteca de DirectXMath para los destinos de Windows x86 se realiza con las \_ \_ \_ funciones intrínsecas de XM SSE \_ definidas. Esto significa que todas las funciones de DirectXMath harán uso de instrucciones SSE2. Sin embargo, lo mismo no es cierto para otro código.

El código fuera de DirectXMath se controla mediante los valores predeterminados del compilador. Sin este modificador, el código generado puede usar a menudo el código x87 menos eficaz.

Se recomienda encarecidamente usar siempre la versión más reciente disponible del compilador.

## <a name="use-est-functions-when-appropriate"></a>Usar las funciones de est cuando sea necesario

Muchas funciones tienen una función de estimación equivalente que termina en est. Estas funciones intercambian cierta precisión para mejorar el rendimiento. Las funciones de est son adecuadas para cálculos no críticos en los que se puede sacrificar la precisión de la velocidad. La cantidad exacta de pérdida de precisión y aumento de velocidad es dependiente de la plataforma.

Por ejemplo, la función [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) puede usarse en lugar de la función [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) .

## <a name="use-aligned-data-types-and-operations"></a>Usar tipos de datos alineados y operaciones

Los conjuntos de instrucciones SIMD en las versiones de Windows que admiten SSE2 suelen tener versiones alineadas y no alineadas de las operaciones de memoria. El uso de las operaciones alineadas es más rápido y se debe preferir siempre que sea posible.

La biblioteca de DirectXMath proporciona funcionalidad alineada y sin alinear a través de tipos, estructuras y funciones de vector de variante. Estas variantes se indican mediante una "A" al final del nombre.

Por ejemplo, hay una estructura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) sin alinear y una estructura [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) alineada, que son usadas por las funciones [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) y [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) , respectivamente.

## <a name="properly-align-allocations"></a>Alinear las asignaciones correctamente

Las versiones alineadas de los intrínsecos [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) subyacentes a la biblioteca de DirectXMath son más rápidas que la no alineada.

Por este motivo, las operaciones de DirectXMath que usan objetos [**XMVECTOR**](xmvector-data-type.md) y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) suponen que los objetos tienen una alineación de 16 bytes. Esto es automático para las asignaciones basadas en la pila, si el código se compila con la biblioteca de DirectXMath mediante la configuración recomendada del compilador de Windows (vea [usar la configuración de compilación correcta](#use-correct-compilation-settings)). Sin embargo, es importante asegurarse de que la asignación de montones que contiene objetos **XMVECTOR** y **XMMATRIX** , o conversiones a estos tipos, cumpla estos requisitos de alineación.

Mientras que las asignaciones de memoria de Windows de 64 bits tienen una alineación de 16 bytes, de forma predeterminada, en las versiones de 32 bits de la memoria asignada de Windows, solo se alinea con 8 bytes. Para obtener información sobre cómo controlar la alineación de memoria, consulte [ \_ aligned \_ malloc](https://msdn.microsoft.com/library/8z34s9c6(VS.80).aspx).

Al usar tipos alineados de DirectXMath con la biblioteca de plantillas estándar (STL), deberá proporcionar un asignador personalizado que garantice la alineación de 16 bytes. Consulte el [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) del equipo de Visual C++ para obtener un ejemplo de cómo escribir un asignador personalizado (en lugar de malloc/Free, que querrá usar \_ malloc alineado \_ y \_ alineado \_ de forma gratuita en su implementación).

> [!Note]  
> Algunas plantillas STL modifican la alineación del tipo proporcionado. Por ejemplo, [la \_<>compartidas ](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) agrega información interna de seguimiento que puede respetar o no la alineación del tipo de usuario proporcionado, lo que da lugar a miembros de datos no alineados. En este caso, debe usar tipos no alineados en lugar de tipos alineados. Si deriva de clases existentes, incluidos muchos objetos Windows Runtime, también puede modificar la alineación de una clase o estructura.

 

## <a name="avoid-operator-overloads-when-possible"></a>Evitar sobrecargas de operador cuando sea posible

Como ventaja, una serie de tipos como [**XMVECTOR**](xmvector-data-type.md) y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) tienen sobrecargas de operador para las operaciones aritméticas comunes. Estas sobrecargas de operador tienden a crear numerosos objetos temporales. Se recomienda evitar estas sobrecargas de operador en el código sensible al rendimiento.

## <a name="denormals"></a>Desnormalizados

Para admitir cálculos cercanos a 0, el estándar de punto flotante IEEE 754 incluye compatibilidad con el subdesbordamiento gradual. El subdesbordamiento gradual se implementa mediante el uso de valores desnormalizados y muchas implementaciones de hardware son lentas cuando se administran desnormalizaciones. Una optimización que se debe considerar es deshabilitar el control de las desnormalizaciones para las operaciones de vector usadas por DirectXMath.

El cambio del control de las desnormalizaciones se realiza mediante la rutina [ \_ controlfp \_ s](/cpp/c-runtime-library/reference/controlfp-s) en una base de subprocesos y puede dar lugar a mejoras en el rendimiento. Use este código para cambiar el control de las desnormalizaciones:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> En las versiones de 64 bits de Windows, las instrucciones de [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) se usan para todos los cálculos, no solo las operaciones de vector. Cambiar el control de desnormalización afecta a todos los cálculos de punto flotante en el programa, no solo a las operaciones de vector usadas por DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Sacar provecho de la doble de punto flotante de entero

DirectXMath admite vectores de 4 valores de punto flotante de precisión sencilla o de 4 32 bits (con o sin signo).

Dado que los conjuntos de instrucciones que se usan para implementar la biblioteca de DirectXMath tienen la capacidad de tratar los mismos datos como varios tipos diferentes; por ejemplo, tratar el mismo vector como datos de punto flotante y enteros, se pueden lograr ciertas optimizaciones. Puede obtener estas optimizaciones mediante las rutinas de inicialización de vectores enteros y los operadores de bits para manipular los valores de punto flotante.

El formato binario de los números de punto flotante de precisión sencilla que usa la biblioteca de DirectXMath se ajusta totalmente al estándar IEEE 764:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Cuando se trabaja con el número de punto flotante de precisión sencilla IEEE 764, es importante tener en cuenta que algunas representaciones tienen un significado especial (es decir, no se ajustan a la descripción anterior). Algunos ejemplos son:

-   Cero positivo es 0
-   Cero negativo es 0x80000000
-   Q \_ Nan es 07FC0000
-   + INF es 0x7F800000
-   -INF es 0xFF800000

## <a name="prefer-template-forms"></a>Preferir formularios de plantilla

El formulario de plantilla existe para [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle), [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert), [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft), [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)y [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright). El uso de estos en lugar del formulario de función general permite al compilador crear muchas más implementaciones de efficent. En el caso de [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)), esto suele contraerse hasta uno o dos \_ valores de PS de \_ orden aleatorio \_ . En el caso de ARM-neón, la plantilla **XMVectorSwizzle** puede emplear una serie de casos especiales en lugar del valor de VTBL swizzle/permute más general.

## <a name="using-directxmath-with-direct3d"></a>Usar DirectXMath con Direct3D

Un uso común de DirectXMath es realizar cálculos de gráficos para su uso con Direct3D. Con Direct3D 10. x y Direct3D 11. x, puede usar la biblioteca de DirectXMath de estas formas directas:

-   Utilice las [constantes](ovw-xnamath-reference-constants.md) de espacio de nombres Colors directamente en el parámetro *ColorRGBA* en una llamada al método [**ID3D11DeviceContext:: ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) o [**ID3D10Device:: ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) . Para Direct3D 9, debe convertir al tipo [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) para usarlo como parámetro de *color* en una llamada al método [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) .
-   Use los tipos [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) y [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) para configurar estructuras de búfer de constantes como referencia [](../direct3dhlsl/dx-graphics-hlsl-scalar.md) en los tipos de/float4x4 de [**matriz**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)o de HLSL.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / Los tipos de [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) están en formato de fila principal. Por lo tanto, si usa el modificador de compilador/ZPR (la marca de compilación principal de la columna de la [**matriz de D3DCOMPILE \_ Pack \_ \_ \_**](../direct3dhlsl/d3dcompile-constants.md) ) u omitir la \_ [palabra clave](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) major de la fila al declarar el tipo de matriz en HLSL, debe transponer la matriz al establecerla en el búfer de constantes.

     

-   Con Direct3D 10. x y Direct3D 11. x, puede suponer que el puntero devuelto por el método de asignación (por ejemplo, [**ID3D11DeviceContext:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) en el miembro **pdata** ([**D3D10 \_ asignado \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**D3D10 \_ asignado \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** o [**\_ \_ subrecurso asignado D3D11**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) es una alineación de 16 bytes si se usa el [nivel de característica](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ 0 o superior, o cada vez que se usan los recursos de [**\_ \_ almacenamiento provisional de uso de D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
