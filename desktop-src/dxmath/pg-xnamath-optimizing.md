---
description: En este tema se describen las consideraciones y estrategias de optimización con la biblioteca DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Optimización de código con la biblioteca DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15369ab36e199eb1a204cc4b761dc637f114f2a1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827259"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Optimización de código con la biblioteca DirectXMath

En este tema se describen las consideraciones y estrategias de optimización con la biblioteca DirectXMath.

-   [Usar los accessors con moderación](#use-accessors-sparingly)
-   [Usar la configuración de compilación correcta](#use-correct-compilation-settings)
-   [Usar funciones Est cuando sea necesario](#use-est-functions-when-appropriate)
-   [Usar operaciones y tipos de datos alineados](#use-aligned-data-types-and-operations)
-   [Alinear correctamente las asignaciones](#properly-align-allocations)
-   [Evitar sobrecargas de operador cuando sea posible](#avoid-operator-overloads-when-possible)
-   [Desnormalizados](#denormals)
-   [Aprovechar la dualidad de punto flotante entero](#take-advantage-of-the-integer-floating-point-duality)
-   [Preferir formularios de plantilla](#prefer-template-forms)
-   [Uso de DirectXMath con Direct3D](#using-directxmath-with-direct3d)
-   [Temas relacionados](#related-topics)

## <a name="use-accessors-sparingly"></a>Usar los accessors con moderación

Las operaciones basadas en vectores usan los conjuntos de instrucciones SIMD y usan registros especiales. El acceso a componentes individuales requiere pasar de los registros SIMD a los escalares y volver atrás.

Siempre que sea posible, es más eficaz inicializar todos los componentes de [**un XMVECTOR**](xmvector-data-type.md) a la vez, en lugar de usar una serie de accessors vectoriales individuales.

## <a name="use-correct-compilation-settings"></a>Usar la configuración de compilación correcta

Para los destinos x86 de Windows, habilite /arch:SSE2. Para todos los destinos de Windows, habilite /fp:fast.

De forma predeterminada, la compilación en los destinos x86 de la biblioteca DirectXMath para windows se realiza con LAS FUNCIONES \_ \_ INTRÍNSECAS de SSE de XM \_ \_ definidas. Esto significa que toda la funcionalidad de DirectXMath usará instrucciones de SSE2. Sin embargo, no ocurre lo mismo para otro código.

El código fuera de DirectXMath se controla mediante los valores predeterminados del compilador. Sin este modificador, el código generado a menudo puede usar el código x87 menos eficaz.

Se recomienda encarecidamente usar siempre la versión más reciente disponible del compilador.

## <a name="use-est-functions-when-appropriate"></a>Usar funciones Est cuando sea necesario

Muchas funciones tienen una función de estimación equivalente que termina en Est. Estas funciones negocian cierta precisión para mejorar el rendimiento. Las funciones Est son adecuadas para cálculos no críticos en los que se puede sacrificar la precisión por velocidad. La cantidad exacta de precisión perdida y el aumento de velocidad dependen de la plataforma.

Por ejemplo, la [**función XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) podría usarse en lugar de la función [**XMVector3AngleBetweenNormals.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals)

## <a name="use-aligned-data-types-and-operations"></a>Usar operaciones y tipos de datos alineados

Los conjuntos de instrucciones SIMD de las versiones de windows que admiten SSE2 suelen tener versiones alineadas y no alineadas de las operaciones de memoria. El uso de las operaciones alineadas es más rápido y debe ser preferible siempre que sea posible.

La biblioteca DirectXMath proporciona funcionalidad de acceso alineada y no alineada a través de tipos de vectores, estructura y funciones variantes. Estas variantes se indican mediante una "A" al final del nombre.

Por ejemplo, hay una estructura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) no alineada y una estructura [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) alineada, que usan las funciones [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) y [**XMStoreFloat4A,**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) respectivamente.

## <a name="properly-align-allocations"></a>Alinear correctamente las asignaciones

Las versiones alineadas de los [intrínsecos de SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) subyacentes a la biblioteca DirectXMath son más rápidas que las no alineadas.

Por esta razón, las operaciones de DirectXMath que usan [**objetos XMVECTOR**](xmvector-data-type.md) y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) suponen que esos objetos están alineados con 16 bytes. Esto es automático para las asignaciones basadas en la pila, si el código se compila en la biblioteca DirectXMath mediante la configuración recomendada del compilador de Windows (vea [Usar](#use-correct-compilation-settings)la configuración de compilación correcta). Sin embargo, es importante asegurarse de que la asignación del montón que contiene objetos **XMVECTOR** y **XMMATRIX,** o que se convierte a estos tipos, cumple estos requisitos de alineación.

Aunque las asignaciones de memoria de Windows de 64 bits están alineadas con 16 bytes, de forma predeterminada en las versiones de 32 bits de memoria de Windows asignadas solo se alinean 8 bytes. Para obtener información sobre cómo controlar la alineación de memoria, vea [ \_ \_ malloc alineado.](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc)

Al usar tipos directXMath alineados con la biblioteca de plantillas estándar (STL), deberá proporcionar un asignador personalizado que garantice la alineación de 16 bytes. Consulte el [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) de Visual C++ Team para obtener un ejemplo de escritura de un asignador personalizado (en lugar de malloc/free, querrá usar malloc alineado y alineado libre en \_ la \_ \_ \_ implementación).

> [!Note]  
> Algunas plantillas STL modifican la alineación del tipo proporcionado. Por ejemplo, [hacer \_ ](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) que la<>agrega información de seguimiento interna que puede o no respetar la alineación del tipo de usuario proporcionado, lo que da lugar a miembros de datos no alineados. En este caso, debe usar tipos no alineados en lugar de tipos alineados. Si deriva de clases existentes, incluidos Windows Runtime objetos, también puede modificar la alineación de una clase o estructura.

 

## <a name="avoid-operator-overloads-when-possible"></a>Evitar sobrecargas de operador cuando sea posible

Por comodidad, una serie de tipos como [**XMVECTOR**](xmvector-data-type.md) y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) tienen sobrecargas de operador para operaciones aritméticas comunes. Estas sobrecargas de operador tienden a crear numerosos objetos temporales. Se recomienda evitar estas sobrecargas de operador en código sensible al rendimiento.

## <a name="denormals"></a>Desnormalizados

Para admitir cálculos cercanos a 0, el estándar de punto flotante IEEE 754 incluye compatibilidad con el subdesbordmiento gradual. El subdesbordmiento gradual se implementa mediante el uso de valores desnormalizados y muchas implementaciones de hardware son lentas al controlar desnormales. Una optimización que se debe tener en cuenta es deshabilitar el control de desnormales para las operaciones vectoriales que usa DirectXMath.

El cambio del control de los desnormales se realiza mediante el uso de la rutina del [ \_ controlfp \_ ](/cpp/c-runtime-library/reference/controlfp-s) de forma previa al subproceso y puede dar lugar a mejoras de rendimiento. Use este código para cambiar el control de los desnormales:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> En las versiones de 64 bits de Windows, las instrucciones [de SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) se usan para todos los cálculos, no solo para las operaciones vectoriales. Cambiar el control desnormal afecta a todos los cálculos de punto flotante del programa, no solo a las operaciones vectoriales que usa DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Aprovechar la dualidad de punto flotante entero

DirectXMath admite vectores de 4 valores de punto flotante de precisión sencilla o cuatro valores de 32 bits (con signo o sin signo).

Dado que los conjuntos de instrucciones usados para implementar la biblioteca DirectXMath tienen la capacidad de tratar los mismos datos que varios tipos diferentes(por ejemplo, tratar el mismo vector que las optimizaciones de punto flotante y de datos enteros) se pueden lograr. Puede obtener estas optimizaciones mediante las rutinas de inicialización de vectores enteros y los operadores de bits para manipular valores de punto flotante.

El formato binario de números de punto flotante de precisión sencilla usados por la biblioteca DirectXMath se ajusta completamente al estándar IEEE 764:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Al trabajar con el número de punto flotante de precisión sencilla IEEE 764, es importante tener en cuenta que algunas representaciones tienen un significado especial (es decir, no se ajustan a la descripción anterior). Los ejemplos incluyen:

-   Cero positivo es 0
-   Cero negativo es 0x80000000
-   Q \_ NAN es 07FC0000
-   +INF es 0x7F800000
-   -INF es 0xFF800000

## <a name="prefer-template-forms"></a>Preferir formularios de plantilla

Existe un formulario de plantilla para [**XMVectorSwechle,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**XMVectorInsert,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) [**XMVectorShiftLeft,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)y [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright). El uso de estos en lugar del formulario de función general permite al compilador crear implementaciones mucho más efficentes. Para [SSE,](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))a menudo se contrae a uno o dos \_ mm de valores ps \_ \_ aleatorios. En el caso de ARM-NEON, la plantilla **XMVectorSw vtle** puede utilizar una serie de casos especiales en lugar de la vtbl swzzle/permute más general.

## <a name="using-directxmath-with-direct3d"></a>Uso de DirectXMath con Direct3D

Un uso común de DirectXMath es realizar cálculos gráficos para su uso con Direct3D. Con Direct3D 10.x y Direct3D 11.x, puede usar la biblioteca DirectXMath de estas maneras directas:

-   Use las [](ovw-xnamath-reference-constants.md) constantes de espacio de nombres Colors directamente en el *parámetro ColorRGBA* en una llamada al método [**ID3D11DeviceContext::ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) o [**ID3D10Device::ClearRenderTargetView.**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) Para Direct3D 9, debe convertir al tipo [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) para usarlo como el *parámetro Color* en una llamada al método [**IDirect3DDevice9::Clear.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
-   Use los tipos [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) y [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)XMMATRIX para configurar estructuras de búfer constante como referencia por los tipos / [](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) HLSL [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) o [**matrix**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**Los tipos XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) están en formato de fila principal. Por lo tanto, si usa el modificador del compilador /Zpr (la marca de compilación [**D3DCOMPILE \_ PACK MATRIX COLUMN \_ \_ \_ MAJOR)**](../direct3dhlsl/d3dcompile-constants.md) u omite la palabra clave principal de fila al declarar el tipo de matriz en \_ HLSL, debe transponer la matriz al establecerla en el búfer constante. [](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md)

     

-   Con Direct3D 10.x y Direct3D 11.x, puede suponer que el puntero devuelto por el método Map (por ejemplo, [**ID3D11DeviceContext::Map)**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)en el miembro **pData** ([**D3D10 \_ MAPPED \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**D3D10 \_ MAPPED \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** o [**D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) tiene una alineación de [](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 16 bytes si usa el nivel de característica 10 0 o superior o siempre que use recursos de ALMACENAMIENTO PROVISIONAL DE USO de \_ [**D3D11. \_ \_**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
