---
title: Introducción (DirectXMath)
description: La biblioteca de DirectXMath implementa una interfaz óptima y portable para operaciones de álgebra aritmética y lineal en vectores de punto flotante de precisión sencilla (2D, 3D y 4D) o matrices (3 × 3 y 4 × 4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e599acfc498e28b33acfc5bbbba2bea5669d2a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361803"
---
# <a name="getting-started-directxmath"></a>Introducción (DirectXMath)

La biblioteca de DirectXMath implementa una interfaz óptima y portable para operaciones de álgebra aritmética y lineal en vectores de punto flotante de precisión sencilla (2D, 3D y 4D) o matrices (3 × 3 y 4 × 4). La biblioteca tiene una compatibilidad limitada para las operaciones de vector de entero. Estas operaciones se usan en gran medida en la representación y la animación de programas de gráficos. No se admiten vectores de precisión doble (incluidos Long, Short o bytes) y solo operaciones de vector de entero limitado.

La biblioteca está disponible en una gran variedad de plataformas de Windows. Dado que la biblioteca proporciona funcionalidad que no está disponible anteriormente, esta versión sustituye a las siguientes bibliotecas:

-   Biblioteca matemática de Xbox proporcionada por el encabezado Xboxmath. h
-   Biblioteca D3DX 9 proporcionada por los archivos dll de D3DX 9
-   Biblioteca matemática de D3DX 10 proporcionada a través de los archivos dll de D3DX 10
-   Biblioteca matemática de XNA proporcionada por el encabezado xnamath. h en el SDK de DirectX y Xbox 360 XDK

En estas secciones se describen los conceptos básicos de introducción.

-   [Descargar](#download)
-   [Requisitos del sistema en tiempo de ejecución](#run-time-system-requirements)
-   [Información general sobre el diseño](#design-overview)
-   [Convención de matriz](#matrix-convention)
-   [Uso básico](#basic-usage)
-   [Instrucciones de uso de tipos](#type-usage-guidelines)
-   [Crear vectores](#creating-vectors)
    -   [VECTORES CONSTANTES](#constant-vectors)
    -   [VECTORES DE VARIABLES](#vectors-from-variables)
    -   [VECTORES DE VECTORES](#vectors-from-vectors)
    -   [VECTORES DE LA MEMORIA](#vectors-from-memory)
-   [Extraer componentes de vectores](#extracting-components-from-vectors)
-   [Temas relacionados](#related-topics)

## <a name="download"></a>Descargar

La biblioteca de DirectXMath se incluye en el Windows SDK. También puede descargarlo desde [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath). Este sitio también contiene proyectos de ejemplo relacionados.

## <a name="run-time-system-requirements"></a>Requisitos del sistema de Run-Time

La biblioteca de DirectXMath usa instrucciones de procesador especializadas para las operaciones de vectores cuando están disponibles. Para evitar que un programa genere errores de "excepción de instrucción desconocida", Compruebe la compatibilidad del procesador llamando a [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) antes de usar la biblioteca de DirectXMath.

Estos son los requisitos básicos de compatibilidad en tiempo de ejecución de la biblioteca de DirectXMath:

-   La compilación predeterminada en una plataforma Windows (x86/x64) requiere la compatibilidad con instrucciones SSE/SSE2.
-   La conformidad predeterminada en una plataforma Windows RT requiere compatibilidad con instrucciones ARM-neón.
-   La compilación con [**\_ XM \_ no \_ intrínsecos \_**](ovw-xnamath-reference-directives.md) definido solo requiere compatibilidad con la operación de punto flotante estándar.

> [!Note]  
> Cuando llame a [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport), incluya <Windows. h> antes de incluir <la> DirectXMath. h. Esta es la única función de la biblioteca que requiere cualquier contenido de <Windows. h> por lo que no es necesario incluir <Windows. h> en cada módulo que use <DirectXMath. h>.

 

## <a name="design-overview"></a>Introducción al diseño

La biblioteca de DirectXMath es compatible principalmente con el lenguaje de programación de C++. La biblioteca se implementa mediante rutinas insertadas en los archivos de encabezado, DirectXMath \* . INL, DirectXPackedVector. INL y DirectXCollision. INL. Esta implementación hace uso de las funciones intrínsecas del compilador de alto rendimiento.

La biblioteca de DirectXMath proporciona:

-   Implementación de con los intrínsecos SSE/SSE2.
-   Implementación sin intrínsecos.
-   Una implementación de que usa intrínsecos ARM-neón.

Dado que la biblioteca se entrega mediante archivos de encabezado, use el código fuente para personalizar y optimizar para su propia aplicación.

## <a name="matrix-convention"></a>Convención de matriz

DirectXMath usa matrices de filas principales, vectores de filas y premultiplicación. La versión de la función se usa (RH frente a LH) y, en caso contrario, la función funciona con las coordenadas de la vista de la izquierda o de la mano derecha.

Como referencia, Direct3D ha utilizado históricamente el sistema de coordenadas de la mano izquierda, las matrices de filas principales, los vectores de fila y la multiplicación previa. La versión moderna de Direct3D no tiene un requisito sólido para las coordenadas izquierda frente a la mano derecha, y normalmente los sombreadores de HLSL usan matrices de columnas principales de forma predeterminada. Consulte [ordenación de matrices de HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) para obtener más información.

## <a name="basic-usage"></a>Uso básico

Para usar las funciones de la biblioteca de DirectXMath, incluya los encabezados DirectXMath. h, DirectXPackedVector. h, DirectXColors. h y/o DirectXCollision. h. Los encabezados se encuentran en el kit de desarrollo de software de Windows para aplicaciones de la tienda Windows.

## <a name="type-usage-guidelines"></a>Instrucciones de uso de tipos

Los tipos [**XMVECTOR**](xmvector-data-type.md) y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) son los caballos de trabajo de la biblioteca de DirectXMath. Cada operación consume o produce datos de estos tipos. Trabajar con ellos es fundamental para usar la biblioteca. Sin embargo, dado que DirectXMath usa los conjuntos de instrucciones SIMD, estos tipos de datos están sujetos a una serie de restricciones. Es fundamental que comprenda estas restricciones si desea hacer un buen uso de las funciones de DirectXMath.

Debe pensar en [**XMVECTOR**](xmvector-data-type.md) como un proxy para un registro de hardware SIMD y [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como proxy para una agrupación lógica de cuatro registros de hardware SIMD. Estos tipos se anotan para indicar que requieren una alineación de 16 bytes para funcionar correctamente. El compilador los colocará automáticamente en la pila cuando se usen como una variable local, o se colocará en el segmento de datos cuando se usen como una variable global. Con las convenciones adecuadas, también se pueden pasar de forma segura como parámetros a una función (consulte [convenciones de llamada](pg-xnamath-internals.md) para obtener más información).

Sin embargo, las asignaciones del montón son más complicadas. Por lo tanto, debe tener cuidado siempre que use [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como miembro de una clase o estructura que se va a asignar desde el montón. En Windows x64, todas las asignaciones del montón tienen una alineación de 16 bytes, pero para windows x86, solo tienen una alineación de 8 bytes. Hay opciones para asignar estructuras del montón con una alineación de 16 bytes (vea [alinear asignaciones correctamente](pg-xnamath-optimizing.md)). En el caso de los programas de C++, puede usar sobrecargas de operador new/delete/New \[ \] /Delete \[ \] (tanto globales como específicas de la clase) para aplicar la alineación óptima si lo desea.

> [!Note]  
> Como alternativa a la aplicación de la alineación en la clase de C++ directamente mediante la sobrecarga de New/Delete, puede usar la [expresión pImpl](https://en.wikipedia.org/wiki/Opaque_pointer). Si se asegura de que la clase **impl** se alinee a través de [**\_ \_ malloc alineada**](/cpp/c-runtime-library/reference/aligned-malloc) internamente, puede utilizar libremente tipos alineados dentro de la implementación interna. Esta es una buena opción cuando la clase ' Public ' es una Windows Runtime clase Ref o está pensada para su uso con [**STD:: Shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class), que de otro modo podría interrumpir la alineación minuciosa.

 

Sin embargo, a menudo es más fácil y más compacto evitar el uso de [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) directamente en una clase o estructura. En su lugar, use [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3), [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4), [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3), [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4), etc., como miembros de la estructura. Además, puede usar las funciones de [carga vectorial](ovw-xnamath-reference-functions-load.md) y [almacenamiento vectorial](ovw-xnamath-reference-functions-storage.md) para trasladar los datos de forma eficaz a las variables locales de **XMVECTOR** o **XMMATRIX** , realizar cálculos y almacenar los resultados. También hay funciones de transmisión por secuencias ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream), [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream), etc.) que operan de forma eficaz directamente en matrices de estos tipos de datos.

## <a name="creating-vectors"></a>Crear vectores

### <a name="constant-vectors"></a>VECTORES CONSTANTES

Muchas operaciones requieren el uso de constantes en los cálculos de vectores y hay varias formas de cargar un [**XMVECTOR**](xmvector-data-type.md) con los valores deseados.

-   Si se carga una constante escalar en todos los elementos de un [**XMVECTOR**](xmvector-data-type.md), use [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) o [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Si usa una constante de vector con valores fijos diferentes como [**XMVECTOR**](xmvector-data-type.md), use las estructuras [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** o [**XMVECTORU8**](xmvectoru8-data-type.md) . A estos se les puede hacer referencia directamente en cualquier lugar en el que se pase un valor de **XMVECTOR** .
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > No utilice las listas de inicializadores directamente con [**XMVECTOR**](xmvector-data-type.md) (es decir, XMVECTOR v = {1.0 f, 2.0 f, 3.0 f, 4.0 f}). Este código es ineficaz y no es portable en todas las plataformas compatibles con DirectXMath.

     

-   DirectXMath incluye una serie de constantes globales predefinidas que puede usar en el código (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g \_ XMHalfPi, g \_ XMPi, etc.). Busque en el encabezado DirectXMath. h los valores de **XMGLOBALCONSTANT** .
-   Hay un conjunto de constantes vectoriales para los colores RGB comunes (rojo, verde, azul, amarillo, etc.). Para obtener más información sobre estas constantes de Vector, vea DirectXColors. h y el espacio de nombres DirectX:: colors.

### <a name="vectors-from-variables"></a>VECTORES DE VARIABLES

-   Si va a crear un vector a partir de una única variable escalar, consulte [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) y [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Si va a crear un vector a partir de cuatro variables escalares, consulte [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) y [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint).
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>VECTORES DE VECTORES

-   Si crea un vector a partir de otro vector con un componente específico establecido en una variable, puede considerar el uso de [funciones de descriptor de acceso de vector](ovw-xnamath-reference-functions-accessors.md).
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Si crea un vector a partir de otro vector con un único componente replicado, use [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx), [**XMVectorSplatY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty), [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)y [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Si crea un vector a partir de otro vector o par de vectores con componentes reordenados, consulte [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) y [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>VECTORES DE LA MEMORIA

-   Para cargar un único valor Float de la memoria, consulte [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)y [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   Las formas comunes de cargar matrices Float son: [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3), [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)y [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   DirectXMath incluye un amplio conjunto de tipos y cargas y almacenes relacionados para administrar diversas estructuras de datos y formatos de GPU comunes. Consulte la [carga de vectores](ovw-xnamath-reference-functions-load.md) y el [almacén de vectores](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Extraer componentes de vectores

El procesamiento de SIMD es más eficaz cuando los datos se cargan en los registros SIMD y se procesan por completo antes de extraer los resultados. La conversión entre las formas escalares y vectoriales es ineficaz, por lo que se recomienda hacerlo solo cuando sea necesario. Por esta razón, las funciones de la biblioteca de DirectXMath que producen un valor escalar se devuelven en forma de vector en la que el resultado escalar se replica en el vector resultante (es decir, [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot), [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length), etc.). Sin embargo, si necesita valores escalares, aquí se muestran algunas opciones sobre cómo hacerlo:

-   Si se calcula una única respuesta escalar, el uso de las [funciones de descriptor de acceso de vector](ovw-xnamath-reference-functions-accessors.md) es adecuado:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Si es necesario extraer varios componentes del vector, considere la posibilidad de almacenar el vector en una estructura de memoria y leerlo de nuevo. Por ejemplo:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   La forma más eficaz de procesamiento vectorial es usar el streaming de memoria a memoria, donde los datos de entrada se cargan desde la memoria (mediante [funciones de carga vectorial](ovw-xnamath-reference-functions-load.md)), se procesan completamente en formato SIMD y, a continuación, se escriben en la memoria (mediante [las funciones de almacenamiento vectorial](ovw-xnamath-reference-functions-storage.md)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 