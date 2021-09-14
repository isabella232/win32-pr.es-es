---
description: Describe los tipos y estructuras de la biblioteca DirectXMath.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Estructuras de la biblioteca DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ac040ee932e9da84c186124514d9f763e20e67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126963432"
---
# <a name="directxmath-library-structures"></a>Estructuras de la biblioteca DirectXMath

Describe los tipos y estructuras de la biblioteca DirectXMath.

La biblioteca DirectXMath proporciona una serie de estructuras y tipos definidos para encapsular datos para admitir la facilidad de uso, optimización y portabilidad. En la lista siguiente se incluyen las estructuras que forman parte actualmente de la biblioteca DirectXMath. Están disponibles a través de DirectXMath.h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Vector 2D donde cada componente es un entero con signo de 8 bits (1 byte) de longitud. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Vector 4D donde cada componente es un entero con signo de 8 bits (1 byte) de longitud.  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Vector 2D para almacenar valores con signo y normalizados como enteros de 8 bits (1 byte) con signo. |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Vector 3D para almacenar valores con signo y normalizados como enteros de 8 bits (1 byte) con signo.  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Vector de color azul verde rojo alfa (ARGB) de 32 bits, donde cada canal de color se especifica como un entero de 8 bits sin signo. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Vector 4D con componentes x,y y z- representados como valores enteros de 10 bits con signo y w-component como un valor entero de 2 bits con signo.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Vector 4D para almacenar valores con firma y normalizados como componentes x-, y-y- con firma de 10 bits y un w-component de 2 bits con firma.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Vector 2D que consta de dos valores de punto flotante de precisión sencilla. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Describe una estructura [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) alineada en un límite de 16 bytes. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Describe un vector 3D que consta de tres valores de punto flotante de precisión sencilla. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Describe una estructura [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) alineada en un límite de 16 bytes. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Describe un vector 3D con componentes X e Y almacenados como un número de punto flotante de 11 bits y un componente Z almacenado como un valor de punto flotante de 10 bits.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Describe un vector 3D de tres componentes de punto flotante con mantisas de 9 bits, cada uno de los que comparten el mismo exponente de 5 bits.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Matriz de punto flotante de 3x3. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Matriz principal de columnas de 3x4 que contiene componentes de punto flotante de 32 bits. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Matriz principal de columna de 3x4 que contiene componentes de punto flotante de 32 bits alineados en un límite de 16 bytes. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Describe un vector 4D que consta de cuatro valores de punto flotante de precisión sencilla.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Describe una estructura [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) alineada en un límite de 16 bytes. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Matriz de punto flotante de 4x3. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Describe una estructura [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) alineada en un límite de 16 bytes. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Matriz de punto flotante de 4x4. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Describe una estructura [**XMFLOAT4X4 alineada**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) en un límite de 16 bytes. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Vector 2D que consta de dos valores de punto flotante de precisión media (16 bits).  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Describe un vector 4D que consta de cuatro valores de punto flotante de precisión media (16 bits).  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Vector 2D donde cada componente es un entero con signo. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Vector 3D donde cada componente es un entero con signo. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Vector 4D donde cada componente es un entero con signo. |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Describe una matriz de 4x4 alineada en un límite de 16 bytes que se asigna a cuatro registros de vectores de hardware. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Describe un vector 2D que consta de componentes enteros de 16 bits con signo y normalizados.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Vector 4D que consta de componentes enteros de 16 bits con signo.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Vector 2D para almacenar valores con signo y normalizados como enteros de 16 bits con signo (tipo `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Vector 4D para almacenar valores con signo normalizados como enteros de 16 bits con signo (tipo `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Vector 4D con componentes x-, y y z- representados como valores enteros de 5 bits sin signo y w-component como un valor entero de 1 bit.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Vector 3D con componentes x y z- representados como valores enteros sin signo de 5 bits y el componente y- como un valor entero de 6 bits sin signo. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Describe un vector 2D donde cada componente es un entero sin signo de 8 bits (1 byte) de longitud. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Describe un vector 4D donde cada componente es un entero sin signo de 8 bits (1 byte) de longitud.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Vector 2D para almacenar valores normalizados sin signo como enteros de 8 bits (1 byte) con signo. |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Vector 3D para almacenar valores normalizados sin signo como enteros de 8 bits (1 byte) con signo.  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Vector 4D con componentes x-, y y z- representados como valores enteros de 10 bits sin signo y w-component como un valor entero de 2 bits sin signo.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Vector 4D para almacenar valores enteros normalizados sin signo como componentes x, y y z sin signo de 10 bits y w-component de 2 bits sin signo.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Vector 2D donde cada componente es un entero sin signo. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Vector 3D donde cada componente es un entero sin signo. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Vector 4D donde cada componente es un entero sin signo. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Vector 4D con cuatro componentes enteros de 4 bits sin signo.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Describe un vector 2D que consta de componentes enteros de 16 bits sin signo.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Vector 4D que consta de componentes enteros de 16 bits sin signo.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Vector 2D para almacenar valores sin signo y normalizados como enteros de 16 bits sin signo, (tipo `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Vector 4D para almacenar valores normalizados sin signo como enteros de 16 bits con signo (tipo `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Vector 4D con componentes x-, y- y z- representados como valores enteros con signo de 10 bits y w-component como un valor entero sin signo de 2 bits.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Vector 4D para almacenar valores con signo y normalizados como componentes x-, y-y z- con signo de 10 bits y un valor normalizado sin signo como w-component de 2 bits sin signo.  |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>
