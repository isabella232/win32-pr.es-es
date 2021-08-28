---
title: Introducción (DirectXMath)
description: La biblioteca DirectXMath implementa una interfaz óptima y portátil para operaciones de álgebra aritméticas y lineales en vectores de punto flotante de precisión sencilla (2D, 3D y 4D) o matrices (3×3 y 4×4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ad7de99a462dc533d8010c45dfadcb1bcfa1b6f33317a941e91c16f30c3d2c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117505"
---
# <a name="getting-started-directxmath"></a>Introducción (DirectXMath)

La biblioteca DirectXMath implementa una interfaz óptima y portátil para operaciones de álgebra aritméticas y lineales en vectores de punto flotante de precisión sencilla (2D, 3D y 4D) o matrices (3×3 y 4×4). La biblioteca tiene compatibilidad limitada con las operaciones de vector entero. Estas operaciones se usan ampliamente en la representación y animación de los programas gráficos. No se admiten vectores de precisión doble (incluidos longs, shorts o bytes) y solo operaciones de vector entero limitadas.

La biblioteca está disponible en una variedad de Windows plataformas. Dado que la biblioteca proporciona funcionalidad no disponible anteriormente, esta versión reemplaza a las bibliotecas siguientes:

-   Biblioteca matemática de Xbox proporcionada por el encabezado Xboxmath.h
-   Biblioteca D3DX 9 proporcionada por los archivos DLL D3DX 9
-   Biblioteca matemática D3DX 10 proporcionada a través de los archivos DLL D3DX 10
-   Biblioteca matemática de XNA proporcionada por el encabezado xnamath.h en el SDK de DirectX y Xbox 360 XDK

En estas secciones se describen los conceptos básicos de la introducción.

-   [Descargar](#download)
-   [Requisitos del sistema en tiempo de ejecución](#run-time-system-requirements)
-   [Información general sobre el diseño](#design-overview)
-   [Convención de matriz](#matrix-convention)
-   [Uso básico](#basic-usage)
-   [Directrices de uso de tipos](#type-usage-guidelines)
-   [Crear vectores](#creating-vectors)
    -   [VECTORES CONSTANTES](#constant-vectors)
    -   [VECTORES DE VARIABLES](#vectors-from-variables)
    -   [VECTORES DE VECTORES](#vectors-from-vectors)
    -   [VECTORES DE MEMORIA](#vectors-from-memory)
-   [Extracción de componentes de vectores](#extracting-components-from-vectors)
-   [Temas relacionados](#related-topics)

## <a name="download"></a>Descargar

La biblioteca DirectXMath se incluye en el SDK Windows. También puede descargarlo desde [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath). Este sitio también contiene proyectos de ejemplo relacionados.

## <a name="run-time-system-requirements"></a>Run-Time del sistema

La biblioteca DirectXMath usa instrucciones de procesador especializadas para las operaciones vectoriales cuando están disponibles. Para evitar que un programa genere errores de "excepción de instrucción desconocida", compruebe la compatibilidad con el procesador llamando a [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) antes de usar la biblioteca DirectXMath.

Estos son los requisitos básicos de compatibilidad en tiempo de ejecución de la biblioteca DirectXMath:

-   La compilación predeterminada en Windows (x86/x64) requiere compatibilidad con instrucciones SSE/SSE2.
-   La compatibilidad predeterminada en una plataforma Windows RT requiere compatibilidad con instrucciones ARM-NEON.
-   La [**\_ compilación con XM \_ NO \_ INTRINSICS \_**](ovw-xnamath-reference-directives.md) definido solo requiere compatibilidad con operaciones de punto flotante estándar.

> [!Note]  
> Al llamar a [**XMVerifyCPUSupport,**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport)incluya <windows.h> antes de incluir <directXMath.h>. Esta es la única función de la biblioteca que requiere cualquier contenido de <windows.h>, por lo que no es necesario incluir <windows.h> en todos los módulos que usan <DirectXMath.h>.

 

## <a name="design-overview"></a>Introducción al diseño

La biblioteca DirectXMath admite principalmente el lenguaje de programación C++. La biblioteca se implementa mediante rutinas insertadas en los archivos de encabezado, DirectXMath \* .inl, DirectXPackedVector.inl y DirectXCollision.inl. Esta implementación usa intrínsecos del compilador de alto rendimiento.

La biblioteca DirectXMath proporciona:

-   Una implementación que usa intrínsecos SSE/SSE2.
-   Implementación sin intrínsecos.
-   Una implementación que usa intrínsecos ARM-NEON.

Dado que la biblioteca se entrega mediante archivos de encabezado, use el código fuente para personalizar y optimizar para su propia aplicación.

## <a name="matrix-convention"></a>Convención de matriz

DirectXMath usa matrices principales de fila, vectores de fila y multiplicación previa. La entrega viene determinada por qué versión de función se usa (RH frente a LH), de lo contrario, la función funciona con coordenadas de vista con la mano izquierda o con la derecha.

Como referencia, Direct3D ha usado históricamente el sistema de coordenadas izquierdo, las matrices principales de fila, los vectores de fila y la multiplicación previa. Direct3D moderno no tiene un requisito fuerte para las coordenadas izquierdas frente a las coordenadas a la derecha y, normalmente, los sombreadores HLSL suelen consumir matrices principales de columna. Consulte [Ordenación de matrices HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) para obtener más información.

## <a name="basic-usage"></a>Uso básico

Para usar las funciones de la biblioteca de DirectXMath, incluya los encabezados DirectXMath.h, DirectXPackedVector.h, DirectXColors.h o DirectXCollision.h. Los encabezados se encuentran en el kit de desarrollo Windows software para aplicaciones Windows Store.

## <a name="type-usage-guidelines"></a>Directrices de uso de tipos

Los [**tipos XMVECTOR**](xmvector-data-type.md) y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) son el trabajo de la biblioteca DirectXMath. Cada operación consume o genera datos de estos tipos. Trabajar con ellos es clave para usar la biblioteca. Sin embargo, dado que DirectXMath usa los conjuntos de instrucciones SIMD, estos tipos de datos están sujetos a una serie de restricciones. Es fundamental que comprenda estas restricciones si desea hacer un buen uso de las funciones de DirectXMath.

Debe considerar [**XMVECTOR**](xmvector-data-type.md) como un proxy para un registro de hardware SIMD y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como un proxy para una agrupación lógica de cuatro registros de hardware SIMD. Estos tipos se anotan para indicar que requieren una alineación de 16 bytes para funcionar correctamente. El compilador los colocará automáticamente correctamente en la pila cuando se utilicen como una variable local o los colocará en el segmento de datos cuando se utilicen como una variable global. Con las convenciones adecuadas, también se pueden pasar de forma segura como parámetros a una función (vea [Convenciones de llamada](pg-xnamath-internals.md) para obtener más información).

Sin embargo, las asignaciones del montón son más complicadas. Por lo tanto, debe tener cuidado cada vez que use [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como miembro de una clase o estructura que se va a asignar desde el montón. En Windows x64, todas las asignaciones de montón están alineadas con 16 bytes, pero para Windows x86, solo están alineadas con 8 bytes. Hay opciones para asignar estructuras del montón con una alineación de 16 bytes (vea [Alinear correctamente asignaciones).](pg-xnamath-optimizing.md) Para los programas de C++, puede usar el operador new/delete/new \[ \] /delete \[ overloads (globalmente o específico de clase) para aplicar una alineación óptima si \] lo desea.

> [!Note]  
> Como alternativa a aplicar la alineación en la clase de C++ directamente mediante la sobrecarga de new/delete, puede usar la expresión [pImpl](https://en.wikipedia.org/wiki/Opaque_pointer). Si se asegura de que **la clase Impl** se alinea internamente a través de [**\_ \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc) alineado, puede usar libremente tipos alineados dentro de la implementación interna. Se trata de una buena opción cuando la clase 'public' es una clase ref del runtime de Windows o está pensada para su uso con [**std::shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class), que de lo contrario puede interrumpir la alineación cuidadosa.

 

Sin embargo, a menudo es más fácil y compacto evitar el uso de [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) directamente en una clase o estructura. En su lugar, use [**XMFLOAT3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) [**XMFLOAT4,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) [**XMFLOAT4X3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) [**XMFLOAT4X4,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)y así sucesivamente, como miembros de la estructura. Además, puede usar las funciones [Vector Loading](ovw-xnamath-reference-functions-load.md) y Vector Storage para mover los datos de forma eficaz [a](ovw-xnamath-reference-functions-storage.md) variables locales **XMVECTOR** o **XMMATRIX,** realizar cálculos y almacenar los resultados. También hay funciones de streaming [**(XMVector3TransformStream,**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream) [**XMVector4TransformStream,**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)y así sucesivamente) que funcionan de forma eficaz directamente en matrices de estos tipos de datos.

## <a name="creating-vectors"></a>Crear vectores

### <a name="constant-vectors"></a>VECTORES CONSTANTES

Muchas operaciones requieren el uso de constantes en cálculos vectoriales y hay varias maneras de cargar [**un XMVECTOR**](xmvector-data-type.md) con los valores deseados.

-   Si carga una constante escalar en todos los elementos de [**un XMVECTOR,**](xmvector-data-type.md)use [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) o [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Si usa una constante vectorial con valores fijos diferentes como [**XMVECTOR,**](xmvector-data-type.md)use las estructuras [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32,**](xmvectoru32-data-type.md) **XMVECVEC32** o [**XMVECTORU8.**](xmvectoru8-data-type.md) A continuación, se puede hacer referencia a ellos directamente en cualquier lugar en el que se pase un **valor XMVECTOR.**
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > No use listas de inicializadores directamente con [**XMVECTOR**](xmvector-data-type.md) (es decir, XMVECTOR v = { 1.0f, 2.0f, 3.0f, 4.0f }). Este código es ineficaz y no es portátil en todas las plataformas compatibles con DirectXMath.

     

-   DirectXMath incluye una serie de constantes globales predefinidas que puede usar en el código (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g \_ XMHalfPi, g \_ XMPi, y así sucesivamente). Busque los valores **XMGLOBALCONSTANT** en el encabezado DirectXMath.h.
-   Hay un conjunto de constantes vectoriales para colores RGB comunes (rojo, verde, azul, amarillo, y así sucesivamente). Para obtener más información sobre estas constantes vectoriales, vea DirectXColors.h y el espacio de nombres DirectX::Colors.

### <a name="vectors-from-variables"></a>VECTORES DE VARIABLES

-   Si crea un vector a partir de una única variable escalar, vea [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) y [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Si crea un vector a partir de cuatro variables escalares, vea [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) y [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint).
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>VECTORES DE VECTORES

-   Si crea un vector a partir de otro vector con un componente específico establecido en una variable, puede considerar el uso de [funciones de accessor de vectores](ovw-xnamath-reference-functions-accessors.md).
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Si crea un vector a partir de otro vector con un único componente replicado, use [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx), [**XMVectorSplatY,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty) [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)y [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Si crea un vector a partir de otro vector o par de vectores con componentes reordenados, vea [**XMVectorSwzolle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) y [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>VECTORES DE MEMORIA

-   Para cargar un único valor float desde la memoria, vea [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr) [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)y [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   Las maneras comunes de cargar matrices float son: [**XMLoadFloat2,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2) [**XMLoadFloat3,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3) [**XMLoadFloat4,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4) [**XMLoadFloat3x3,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3) [**XMLoadFloat4x3 y**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3) [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   DirectXMath incluye un amplio conjunto de tipos y cargas y almacenes relacionados para controlar diversas estructuras de datos y formatos comunes de GPU. Vea [Vector Load (Carga](ovw-xnamath-reference-functions-load.md) de [vectores) y Vector Store (Almacén de vectores).](ovw-xnamath-reference-functions-storage.md)

## <a name="extracting-components-from-vectors"></a>Extraer componentes de vectores

El procesamiento SIMD es más eficaz cuando los datos se cargan en los registros SIMD y se procesan por completo antes de extraer los resultados. La conversión entre formularios escalares y vectoriales es ineficaz, por lo que se recomienda hacerlo solo cuando sea necesario. Por esta razón, las funciones de la biblioteca DirectXMath que generan un valor escalar se devuelven en forma de vector donde el resultado escalar se replica en el vector resultante (es decir, [**XMVector2Dot,**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot) [**XMVector3Length,**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)y así sucesivamente). Sin embargo, cuando necesite valores escalares, estas son algunas opciones sobre cómo hacerlo:

-   Si se calcula una única respuesta escalar, es adecuado usar las funciones [del accessor](ovw-xnamath-reference-functions-accessors.md) vectorial:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Si es necesario extraer varios componentes del vector, considere la posibilidad de almacenar el vector en una estructura de memoria y leerlo de nuevo. Por ejemplo:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   La forma más eficaz de procesamiento vectorial es usar el streaming de memoria a memoria donde los datos de entrada se cargan desde la memoria (mediante funciones de carga [vectorial),](ovw-xnamath-reference-functions-load.md)se procesan completamente en formato SIMD y, a continuación, se escriben en la memoria (mediante [funciones](ovw-xnamath-reference-functions-storage.md)de almacén de vectores).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 