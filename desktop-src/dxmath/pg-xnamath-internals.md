---
description: En este tema se describe el diseño interno de la biblioteca DirectXMath.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Biblioteca interna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26d2a6171a14abebbec0665233c66f873ed7ede2c3b8f01fb70ed406ffea33b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118155"
---
# <a name="library-internals"></a>Biblioteca interna

En este tema se describe el diseño interno de la biblioteca DirectXMath.

-   [Convenciones de llamada](#calling-conventions)
-   [Equivalencia de tipos de biblioteca de gráficos](#graphics-library-type-equivalence)
-   [Constantes globales en la biblioteca DirectXMath](#global-constants-in-the-directxmath-library)
-   [Windows SSE frente a SSE2](#windows-sse-versus-sse2)
-   [Variantes rutinarias](#routine-variants)
-   [Incoherencias de la plataforma](#platform-inconsistencies)
-   [Extensiones específicas de la plataforma](#platform-specific-extensions)
-   [Temas relacionados](#related-topics)

## <a name="calling-conventions"></a>Convenciones de llamada

Para mejorar la portabilidad y optimizar el diseño de datos, debe usar las convenciones de llamada adecuadas para cada plataforma compatible con la biblioteca DirectXMath. En concreto, cuando se pasan objetos [**XMVECTOR**](xmvector-data-type.md) como parámetros, que se definen como alineados en un límite de 16 bytes, hay diferentes conjuntos de requisitos de llamada, en función de la plataforma de destino:

**Para archivos de 32 Windows**

En el caso de las Windows de 32 bits, hay dos convenciones de llamada disponibles para el paso eficaz de valores [ \_ \_ m128](/cpp/cpp/m128) (que implementa [**XMVECTOR**](xmvector-data-type.md) en esa plataforma). El estándar es [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall), que puede pasar los tres primeros valores [ \_ \_ m128](/cpp/cpp/m128) (instancias **XMVECTOR)** como argumentos a una función en un registro *de SSE/SSE2.* [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall) pasa los argumentos restantes a través de la pila.

Los compiladores de Microsoft Visual Studio más recientes admiten una nueva convención de llamada, vectorcall, que puede pasar hasta seis valores \_ \_ [ \_ \_ m128](/cpp/cpp/m128) (instancias [**XMVECTOR)**](xmvector-data-type.md) como argumentos a una función en un registro *SSE/SSE2.* También puede pasar agregados vectoriales heterogéneos (también conocidos como [**XMMATRIX)**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)a través de registros *SSE/SSE2* si hay espacio suficiente.

**Para las ediciones de 64 bits de Windows**

En el caso de las Windows de 64 bits, hay dos convenciones de llamada disponibles para el paso eficaz de [ \_ \_ valores m128.](/cpp/cpp/m128) El estándar es [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall), que pasa todos los [ \_ \_ valores m128](/cpp/cpp/m128) de la pila.

Los Visual Studio más recientes admiten la convención de llamada vectorcall, que puede pasar hasta seis valores \_ \_ [ \_ \_ m128](/cpp/cpp/m128) (instancias [**XMVECTOR)**](xmvector-data-type.md) como argumentos a una función en un registro *SSE/SSE2.* También puede pasar agregados vectoriales heterogéneos (también conocidos como [**XMMATRIX)**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)a través de registros *SSE/SSE2* si hay espacio suficiente.

**Para Windows en ARM**

La Windows arm & ARM64 admite pasar los cuatro primeros valores \_ \_ n128 (instancias [**XMVECTOR)**](xmvector-data-type.md) en el registro.

**Solución DirectXMath**

Los alias **FXMVECTOR,** **GXMVECTOR,** **HXMVECTOR** y **CXMVECTOR** admiten estas convenciones:

-   Use el alias **FXMVECTOR** para pasar a las tres primeras instancias de [**XMVECTOR**](xmvector-data-type.md) que se usan como argumentos de una función.
-   Use el alias **GXMVECTOR** para pasar la 4ª instancia de [**un XMVECTOR**](xmvector-data-type.md) usado como argumento a una función.
-   Use el alias **HXMVECTOR** para pasar las instancias 5 y 6 de un [**XMVECTOR**](xmvector-data-type.md) usado como argumento a una función. Para obtener información sobre consideraciones adicionales, consulte la \_ \_ documentación de vectorcall.
-   Use el alias **CXMVECTOR** para pasar cualquier otra instancia de [**XMVECTOR**](xmvector-data-type.md) usada como argumentos.

> [!Note]  
> Para los parámetros de salida, use siempre XMVECTOR o XMVECTOR& y ignórlos con respecto a las reglas anteriores para \* los parámetros de entrada.

 

Debido a las limitaciones de vectorcall, se recomienda no usar \_ \_ **GXMVECTOR** o **HXMVECTOR** para constructores de C++. Solo tiene **que usar FXMVECTOR para** los tres primeros valores [**XMVECTOR**](xmvector-data-type.md) y, a continuación, **usar CXMVECTOR** para el resto.

Los alias **FXMMATRIX** y **CXMMATRIX** ayudan a admitir el uso del argumento HVA pasando con \_ \_ vectorcall.

-   Use el alias **FXMMATRIX** para pasar el primer [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) como argumento a la función. Esto supone que no tiene más de dos argumentos **FXMVECTOR** o más de dos argumentos float, double o **FXMVECTOR** a la "derecha" de la matriz. Para obtener información sobre consideraciones adicionales, consulte la \_ \_ documentación de vectorcall.
-   De lo contrario, use el alias **CXMMATRIX.**

Debido a las limitaciones de vectorcall, se recomienda no usar \_ \_ **nunca FXMMATRIX** para constructores de C++. Solo tiene que **usar CXMMATRIX.**

Además de los alias de tipo, también debe usar la anotación XM CALLCONV para asegurarse de que la función usa la convención de llamada adecuada \_ \_ \_ (fastcall frente \_ \_ a vectorcall) en función del compilador y la arquitectura. Debido a las limitaciones de vectorcall, se recomienda no usar \_ \_ XM \_ CALLCONV para constructores de C++.

A continuación se muestran declaraciones de ejemplo que ilustran esta convención:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Para admitir estas convenciones de llamada, estos alias de tipo se definen de la siguiente manera (los parámetros deben pasarse por valor para que el compilador los tenga en cuenta para pasarlos en el registro):

**Para aplicaciones de 32 Windows bits**

Cuando se usa \_ \_ fastcall:


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



**Para aplicaciones nativas de 64 bits Windows aplicaciones**

Cuando se usa \_ \_ fastcall:


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



**Windows en ARM**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Aunque todas las funciones se declaran insertadas y, en muchos casos, el compilador no necesitará usar convenciones de llamada para estas funciones, hay casos en los que el compilador puede decidir que es más eficaz no incluir la función y, en estos casos, queremos la mejor convención de llamada posible para cada plataforma.

 

## <a name="graphics-library-type-equivalence"></a>Equivalencia de tipos de biblioteca de gráficos

Para admitir el uso de la biblioteca DirectXMath, muchos tipos y estructuras de directXMath Library son equivalentes a las implementaciones de Windows de los tipos **D3DDECLTYPE** y **D3DFORMAT,** así como los tipos [**\_ DXGI FORMAT.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | FORMATO \_ DXGI                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | DXGI \_ FORMAT \_ R8G8 \_ SINT                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (solo Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ SINT                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (solo Xbox)                                                       | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8x8 \_ SNORM                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM (DXGI 1.1+)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (solo Xbox)                                                         | D3DDECLTYPE \_ DEC3 (solo Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (solo Xbox)                                                        | D3DDECLTYPE \_ DEC3N (solo Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | DXGI \_ FORMAT \_ R11G11B10 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | FORMATO DXGI \_ \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32 \_ SINT                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32 \_ SINT                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32A32 \_ SINT                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | DXGI \_ FORMAT \_ R16G16 \_ SINT                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ SINT                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | DXGI \_ FORMAT \_ R8G8 \_ UINT                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | DXGI \_ FORMAT \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32 \_ UINT                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32 \_ UINT                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32A32 \_ UINT                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | DXGI \_ FORMAT \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UINT                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM (use [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) y [**XMStoreUDecN4 \_ XR).**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3 (solo Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | FORMATO DXGI \_ \_ R10G10B10A2 \_ UINT                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3N (solo Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM (DXGI 1.2+)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | DXGI \_ FORMAT \_ R16G16 \_ UINT                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (solo Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ UINT                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Constantes globales en la biblioteca DirectXMath

Para reducir el tamaño del segmento de datos, la biblioteca DirectXMath usa la macro [XMGLOBALCONST](xmglobalconst.md) para hacer uso de una serie de constantes internas globales en su implementación. Por convención, estas constantes globales internas tienen el prefijo **g \_ XM**. Normalmente, son uno de los tipos siguientes: [**XMVECTORU32,**](xmvectoru32-data-type.md) [**XMVECTORF32**](xmvectorf32-data-type.md)o **XMVECVECVEC32**.

Estas constantes globales internas están sujetas a cambios en futuras revisiones de la biblioteca DirectXMath. Use funciones públicas que encapsulan las constantes cuando sea posible en lugar del uso directo de **valores globales \_ g XM.** También puede declarar sus propias constantes globales mediante [XMGLOBALCONST](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE frente a SSE2

El conjunto de instrucciones SSE solo proporciona compatibilidad con vectores de punto flotante de precisión sencilla. DirectXMath debe usar el conjunto de instrucciones SSE2 para proporcionar compatibilidad con vectores enteros. SSE2 es compatible con todos los procesadores Intel desde la introducción de Pentium 4, todos los procesadores AMD K8 y posteriores y todos los procesadores compatibles con x64.

> [!Note]  
> Windows 8 para x86 o posterior requiere compatibilidad con SSE2. Todas las versiones de Windows x64 requieren compatibilidad con SSE2. Windows en ARM/ARM64 requiere ARM \_ NEON.

 

## <a name="routine-variants"></a>Variantes rutinarias

Hay varias variantes de las funciones de DirectXMath que facilitan el trabajo:

-   Funciones de comparación para crear bifurcaciones condicionales complicadas basadas en un número menor de operaciones de comparación de vectores. El nombre de estas funciones termina en "R", como XMVector3InBoundsR. Las funciones devuelven un registro de comparación como un valor devuelto UINT o como un parámetro UINT out. Puede usar las macros **XMComparision \*** para probar el valor.
-   Funciones por lotes para realizar operaciones de estilo por lotes en matrices de vectores más grandes. El nombre de estas funciones termina en "Stream", como [**XMVector3TransformStream.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream) Las funciones funcionan en una matriz de entradas y generan una matriz de salidas. Normalmente, toman un paso de entrada y salida.
-   Funciones de estimación que implementan una estimación más rápida en lugar de un resultado más lento y preciso. El nombre de estas funciones termina en "Est", como [**XMVector3NormalizeEst.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest) El impacto en la calidad y el rendimiento del uso de la estimación varía de una plataforma a otra, pero se recomienda usar variantes de estimación para el código sensible al rendimiento.

## <a name="platform-inconsistencies"></a>Incoherencias de la plataforma

La biblioteca DirectXMath está pensada para usarse en juegos y aplicaciones gráficas sensibles al rendimiento. Por lo tanto, la implementación está diseñada para una velocidad óptima que realiza un procesamiento normal en todas las plataformas admitidas. Es probable que los resultados en condiciones de límite, especialmente los que generan especiales de punto flotante, varíen de destino a destino. Este comportamiento también dependerá de otras configuraciones en tiempo de ejecución, como la palabra de control x87 para el destino no intrínseco de Windows de 32 bits o la palabra de control SSE para Windows 32 bits y 64 bits. Además, habrá diferencias en las condiciones de límite entre varios proveedores de CPU.

No use DirectXMath en aplicaciones científicas u otras en las que la precisión numérica sea primordial. Además, esta limitación se refleja en la falta de compatibilidad con cálculos de precisión doble u otros cálculos de precisión extendida.

> [!Note]  
> Las rutas de acceso de código escalar XM NO INTRINSICS generalmente se escriben para \_ \_ el \_ \_ cumplimiento, no para el rendimiento. Los resultados de la condición de límite también variarán.

 

## <a name="platform-specific-extensions"></a>Extensiones específicas de la plataforma

La biblioteca DirectXMath está diseñada para simplificar la programación SIMD de C++ proporcionando una excelente compatibilidad con plataformas x86, x64 y Windows RT mediante instrucciones intrínsecas ampliamente admitidas (SSE2 y ARM-NEON).

Sin embargo, hay ocasiones en las que las instrucciones específicas de la plataforma pueden resultar beneficiosas. Debido a la forma en que se implementa DirectXMath, en muchos casos es trivial usar tipos DirectXMath directamente en instrucciones intrínsecas estándar admitidas por el compilador y usar DirectXMath como ruta de acceso de reserva para plataformas que no admiten la instrucción extendida.

Por ejemplo, este es un ejemplo simplificado de aprovechamiento de la instrucción dot-product de SSE 4.1. Tenga en cuenta que debe proteger explícitamente la ruta de acceso del código para evitar generar excepciones de instrucciones no válidas en tiempo de ejecución. Asegúrese de que las rutas de acceso de código hacen un trabajo lo suficientemente importante como para justificar el costo adicional de la bifurcación, la complejidad del mantenimiento de varias rutas de acceso de código, entre otras.


```
#include <Windows.h>
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
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

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



Para más información sobre las extensiones específicas de la plataforma, consulte:

<dl>

[DirectXMath: SSE, SSE2 y ARM-NEON](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath: SSE3 y SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath: SSE4.1 y SSE4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath: AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath: F16C y FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
