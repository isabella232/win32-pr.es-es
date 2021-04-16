---
description: En este tema se describe el diseño interno de la biblioteca de DirectXMath.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Elementos internos de la biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccac708934c393a526fdb46d73f819d6557107f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696713"
---
# <a name="library-internals"></a>Elementos internos de la biblioteca

En este tema se describe el diseño interno de la biblioteca de DirectXMath.

-   [Convenciones de llamada](#calling-conventions)
-   [Equivalencia de tipos de la biblioteca de gráficos](#graphics-library-type-equivalence)
-   [Constantes globales en la biblioteca de DirectXMath](#global-constants-in-the-directxmath-library)
-   [Windows SSE frente a SSE2](#windows-sse-versus-sse2)
-   [Variantes de rutina](#routine-variants)
-   [Incoherencias de la plataforma](#platform-inconsistencies)
-   [Extensiones específicas de la plataforma](#platform-specific-extensions)
-   [Temas relacionados](#related-topics)

## <a name="calling-conventions"></a>Convenciones de llamada

Para mejorar la portabilidad y optimizar el diseño de los datos, debe usar las convenciones de llamada adecuadas para cada plataforma admitida por la biblioteca de DirectXMath. En concreto, cuando se pasan objetos [**XMVECTOR**](xmvector-data-type.md) como parámetros, que se definen como alineados en un límite de 16 bytes, hay diferentes conjuntos de requisitos de llamada, en función de la plataforma de destino:

**Para Windows de 32 bits**

En Windows de 32 bits, hay dos convenciones de llamada disponibles para el paso eficaz de los valores de [ \_ \_ M128](/cpp/cpp/m128) (que implementa [**XMVECTOR**](xmvector-data-type.md) en esa plataforma). El estándar es [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), que puede pasar los tres primeros valores de [ \_ \_ M128](/cpp/cpp/m128) (instancias de **XMVECTOR** ) como argumentos a una función en un registro *sse/sse2* . [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx) pasa los argumentos restantes a través de la pila.

Los compiladores de Microsoft Visual Studio más recientes admiten una nueva Convención de llamada, \_ \_ vectorcall, que puede pasar hasta seis valores [ \_ \_ M128](/cpp/cpp/m128) (instancias [**XMVECTOR**](xmvector-data-type.md) ) como argumentos a una función en un registro *sse/sse2* . También puede pasar agregados vectoriales heterogéneos (también conocidos como [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) a través de registros *sse/sse2* si hay espacio suficiente.

**Para las ediciones de 64 bits de Windows**

En Windows de 64 bits, hay dos convenciones de llamada disponibles para el paso eficaz de los valores de [ \_ \_ M128](/cpp/cpp/m128) . El estándar es [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), que pasa todos los valores de [ \_ \_ M128](/cpp/cpp/m128) en la pila.

Los compiladores de Visual Studio más recientes admiten la \_ \_ Convención de llamada vectorcall, que puede pasar hasta seis valores [ \_ \_ M128](/cpp/cpp/m128) (instancias [**XMVECTOR**](xmvector-data-type.md) ) como argumentos a una función en un registro *sse/sse2* . También puede pasar agregados vectoriales heterogéneos (también conocidos como [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) a través de registros *sse/sse2* si hay espacio suficiente.

**Para Windows RT**

El sistema operativo Windows RT admite el paso de los cuatro primeros \_ \_ valores de n128 (instancias de [**XMVECTOR**](xmvector-data-type.md) ) en el registro.

**Solución de DirectXMath**

Los alias **FXMVECTOR**, **GXMVECTOR**, **HXMVECTOR** y **CXMVECTOR** admiten estas convenciones:

-   Use el alias **FXMVECTOR** para pasar hasta las tres primeras instancias de [**XMVECTOR**](xmvector-data-type.md) usadas como argumentos a una función.
-   Use el alias **GXMVECTOR** para pasar la cuarta instancia de un [**XMVECTOR**](xmvector-data-type.md) utilizado como argumento a una función.
-   Use el alias **HXMVECTOR** para pasar las instancias quinta y sexta de un [**XMVECTOR**](xmvector-data-type.md) usado como argumento a una función. Para obtener información sobre consideraciones adicionales, vea la \_ \_ documentación de vectorcall.
-   Use el alias **CXMVECTOR** para pasar cualquier otra instancia de [**XMVECTOR**](xmvector-data-type.md) utilizada como argumento.

> [!Note]  
> En el caso de los parámetros de salida, use siempre XMVECTOR \* o XMVECTOR& y omítalo con respecto a las reglas anteriores para los parámetros de entrada.

 

Debido a las limitaciones de \_ \_ vectorcall, se recomienda no usar **GXMVECTOR** o **HXMVECTOR** para los constructores de C++. Simplemente use **FXMVECTOR** para los tres primeros valores de [**XMVECTOR**](xmvector-data-type.md) y, luego, use **CXMVECTOR** para el resto.

Los alias **FXMMATRIX** y **CXMMATRIX** sirven de ayuda para aprovechar el argumento HVA que se pasa con \_ \_ vectorcall.

-   Use el alias **FXMMATRIX** para pasar el primer [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como argumento a la función. Se supone que no tiene más de dos argumentos **FXMVECTOR** o más de dos argumentos Float, Double o **FXMVECTOR** en el ' derecho ' de la matriz. Para obtener información sobre consideraciones adicionales, vea la \_ \_ documentación de vectorcall.
-   En caso contrario, utilice el alias **CXMMATRIX** .

Debido a las limitaciones de \_ \_ vectorcall, recomendamos que nunca use **FXMMATRIX** para los constructores de C++. Simplemente use **CXMMATRIX**.

Además de los alias de tipo, también debe utilizar la anotación XM CALLCONV para asegurarse de que \_ la función usa la Convención de llamada adecuada ( \_ \_ fastcall frente a \_ \_ vectorcall) según el compilador y la arquitectura. Debido a las limitaciones de \_ \_ vectorcall, se recomienda no usar los \_ constructores XM CALLCONV para C++.

A continuación se muestran las declaraciones de ejemplo que ilustran esta Convención:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Para admitir estas convenciones de llamada, estos alias de tipo se definen como se indica a continuación (los parámetros deben pasarse por valor para que el compilador los tenga en cuenta para el paso en el registro):

**Para aplicaciones Windows de 32 bits**

Al usar \_ \_ fastcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Cuando se usa \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Para aplicaciones Windows nativas de 64 bits**

Al usar \_ \_ fastcall:


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Cuando se usa \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows RT**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Aunque todas las funciones se declaran en línea y, en muchos casos, el compilador no necesitará usar convenciones de llamada para estas funciones, hay casos en los que el compilador puede decidir que es más eficaz no alinear la función y, en estos casos, queremos la mejor Convención de llamada posible para cada plataforma.

 

## <a name="graphics-library-type-equivalence"></a>Equivalencia de tipos de la biblioteca de gráficos

Para admitir el uso de la biblioteca de DirectXMath, muchos tipos y estructuras de la biblioteca de DirectXMath son equivalentes a las implementaciones de Windows de los tipos **D3DDECLTYPE** y **D3DFORMAT** , así como los tipos de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) . 

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | formato de DXGI \_                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | Formato de DXGI \_ \_ R8G8 \_ Sint                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (solo Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | Formato de DXGI \_ \_ x8x8x8x8 \_ Sint                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | Formato de DXGI \_ \_ R8G8 \_ SNORM                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (solo Xbox)                                                       | D3DFMT \_ x8x8x8x8                                              | Formato de DXGI \_ \_ x8x8x8x8 \_ SNORM                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | Formato de DXGI \_ \_ B8G8R8A8 \_ UNORM (dxgi 1.1 +)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (solo Xbox)                                                         | D3DDECLTYPE \_ DEC3 (solo Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (solo Xbox)                                                        | D3DDECLTYPE \_ DEC3N (solo Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | Formato de DXGI \_ \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | Formato de DXGI \_ \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | Formato de DXGI \_ \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | Formato de DXGI \_ \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | Formato de DXGI \_ \_ R11G11B10 \_ float                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | Formato de DXGI \_ \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | Formato de DXGI \_ \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | Formato de DXGI \_ \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | Formato de DXGI \_ \_ R16G16 \_ float                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | Formato de DXGI \_ \_ R16G16B16A16 \_ float                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | Formato de DXGI \_ \_ R32G32 \_ Sint                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | Formato de DXGI \_ \_ R32G32B32 \_ Sint                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | Formato de DXGI \_ \_ R32G32B32A32 \_ Sint                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | Formato de DXGI \_ \_ R16G16 \_ Sint                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | Formato de DXGI \_ \_ R16G16 \_ SNORM                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | Formato de DXGI \_ \_ R16G16B16A16 \_ Sint                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | Formato de DXGI \_ \_ R16G16B16A16 \_ SNORM                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | Formato de DXGI \_ \_ R8G8 \_ uint                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | Formato de DXGI \_ \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | Formato de DXGI \_ \_ R32G32 \_ uint                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | Formato de DXGI \_ \_ R32G32B32 \_ uint                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | Formato de DXGI \_ \_ R32G32B32A32 \_ uint                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | Formato de DXGI \_ \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | Formato de DXGI \_ \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | Formato de DXGI \_ \_ x8x8x8x8 \_ uint                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | Formato de DXGI \_ \_ x8x8x8x8 \_ UNORM<br/> \_Formato DXGI \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM (use [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) y [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)).<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3 (solo Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | Formato de DXGI \_ \_ R10G10B10A2 \_ uint                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3N (solo Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | Formato de DXGI \_ \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | Formato de DXGI \_ \_ B4G4R4A4 \_ UNORM (dxgi 1.2 +)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | Formato de DXGI \_ \_ R16G16 \_ uint                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | Formato de DXGI \_ \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (solo Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | Formato de DXGI \_ \_ R16G16B16A16 \_ uint                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | Formato de DXGI \_ \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Constantes globales en la biblioteca de DirectXMath

Para reducir el tamaño del segmento de datos, la biblioteca de DirectXMath usa la macro [XMGLOBALCONST](xmglobalconst.md) para hacer uso de varias constantes internas globales en su implementación. Por Convención, tales constantes globales internas llevan el prefijo **g \_ XM**. Normalmente, son uno de los tipos siguientes: [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md)o **XMVECTORI32**.

Estas constantes globales internas están sujetas a cambios en futuras revisiones de la biblioteca de DirectXMath. Utilice funciones públicas que encapsulen las constantes cuando sea posible, en lugar de usar directamente los valores globales de **g \_ XM** . También puede declarar sus propias constantes globales mediante [XMGLOBALCONST](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE frente a SSE2

El conjunto de instrucciones SSE solo proporciona compatibilidad con vectores de punto flotante de precisión sencilla. DirectXMath debe hacer uso del conjunto de instrucciones SSE2 para proporcionar compatibilidad con vectores enteros. SSE2 es compatible con todos los procesadores Intel desde la introducción de Pentium 4, todos los procesadores AMD K8 y versiones posteriores, y todos los procesadores compatibles con x64.

> [!Note]  
> Windows 8 para x86 requiere compatibilidad con SSE2. Todas las versiones de Windows x64 requieren compatibilidad con SSE2. Windows RT (también conocido como Windows en ARM) requiere ARM \_ neón.

 

## <a name="routine-variants"></a>Variantes de rutina

Hay varias variantes de las funciones de DirectXMath que facilitan el trabajo:

-   Funciones de comparación para crear una bifurcación condicional complicada basada en un número menor de operaciones de comparación vectoriales. El nombre de estas funciones termina en "R", como XMVector3InBoundsR. Las funciones devuelven un registro de comparación como un valor devuelto de UINT o como un parámetro de salida UINT. Puede usar las macros ** \* XMComparision* _ para probar el valor.
-   Funciones de batch para realizar operaciones de estilo de lote en matrices de vectores más grandes. El nombre de estas funciones termina en "Stream", como [_ *XMVector3TransformStream* *](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream). Las funciones operan en una matriz de entradas y generan una matriz de salidas. Normalmente, toman un intervalo de entrada y salida.
-   Funciones de estimación que implementan una estimación más rápida en lugar de un resultado más lento y más preciso. El nombre de estas funciones termina en "est", como [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest). El impacto en la calidad y el rendimiento del uso de la estimación varía según la plataforma y la plataforma, pero se recomienda usar variantes de estimación para el código sensible al rendimiento.

## <a name="platform-inconsistencies"></a>Incoherencias de la plataforma

La biblioteca de DirectXMath está pensada para su uso en aplicaciones y juegos de gráficos sensibles al rendimiento. Por lo tanto, la implementación está diseñada para ofrecer una velocidad óptima en todas las plataformas admitidas. Los resultados en las condiciones de límite, especialmente los que generan especiales de punto flotante, pueden variar de un destino a un destino. Este comportamiento también dependerá de otras opciones de configuración en tiempo de ejecución, como la palabra de control x87 para el destino no intrínsecos de bits de Windows 32 o la palabra de control de SSE para Windows 32-bit y 64 bits. Además, habrá diferencias en las condiciones de límite entre varios proveedores de CPU.

No use DirectXMath en las aplicaciones científicas o de otro lugar donde la precisión numérica sea primordial. Además, esta limitación se refleja en la falta de compatibilidad con los cálculos de precisión doble u otros.

> [!Note]  
> Las \_ \_ \_ rutas de acceso del \_ código escalar no intrínsecos de XM generalmente están escritas para el cumplimiento, no para el rendimiento. También variarán los resultados de la condición de límite.

 

## <a name="platform-specific-extensions"></a>Extensiones específicas de la plataforma

La biblioteca de DirectXMath está diseñada para simplificar la programación de C++ SIMD, lo que proporciona una excelente compatibilidad con las plataformas x86, x64 y Windows RT mediante instrucciones intrínsecas compatibles ampliamente (SSE2 y ARM-neón).

Sin embargo, hay ocasiones en las que es posible que las instrucciones específicas de la plataforma resulten beneficiosas. Debido a la forma en que se implementa DirectXMath, en muchos casos es trivial usar directamente los tipos de DirectXMath en las instrucciones intrínsecas compatibles con el compilador estándar y usar DirectXMath como ruta de acceso de reserva para las plataformas que no admiten la instrucción extendida.

Por ejemplo, a continuación se muestra un ejemplo simplificado del uso de la instrucción de producto SSE 4,1 dot-product. Tenga en cuenta que debe proteger explícitamente la ruta de acceso del código para evitar que se generen excepciones de instrucción no válidas en tiempo de ejecución. Asegúrese de que las rutas de acceso del código hacen que el trabajo sea lo suficientemente importante para justificar el costo adicional de la bifurcación, la complejidad del mantenimiento de varias rutas de acceso de código, etc.


```
#include <windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
   __cpuid( CPUInfo, 0 );

   if ( CPUInfo[0] >= 1 )
   {
       __cpuid(CPUInfo, 1 );
 
       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ... 

   return 0;
}
```



Para obtener más información acerca de las extensiones específicas de la plataforma, consulte:

<dl>

[DirectXMath: SSE, SSE2 y ARM-neón](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath: SSE3 y SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath: SSE 4.1 y SSE 4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath: AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath: F16C y FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
