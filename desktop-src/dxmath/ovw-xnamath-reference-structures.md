---
description: Describe los tipos y las estructuras de la biblioteca de DirectXMath.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Estructuras de biblioteca de DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ac040ee932e9da84c186124514d9f763e20e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360498"
---
# <a name="directxmath-library-structures"></a>Estructuras de biblioteca de DirectXMath

Describe los tipos y las estructuras de la biblioteca de DirectXMath.

La biblioteca de DirectXMath proporciona una serie de estructuras y tipos definidos para encapsular los datos para admitir la facilidad de uso, la optimización y la portabilidad. La lista siguiente incluye las estructuras que actualmente forman parte de la biblioteca de DirectXMath. Están disponibles a través de DirectXMath. h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Vector 2D donde cada componente es un entero con signo, de 8 bits (1 byte) de longitud. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Un vector 4D donde cada componente es un entero con signo, de 8 bits (1 byte) de longitud.  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Vector 2D para almacenar valores normalizados y firmados como enteros de 8 bits con signo (1 byte). |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Vector 3D para almacenar valores normalizados y firmados como enteros de 8 bits con signo (1 byte).  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Un vector de color verde rojo verde alfa (ARGB) de 32 bits, donde cada canal de color se especifica como un entero de 8 bits sin signo. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Un vector 4D con x-, y-y los componentes z representados como valores enteros con signo de 10 bits, y el componente w como valor entero con signo de 2 bits.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Un vector 4D para almacenar valores normalizados y firmados como componentes x, y y z con signo de 10 bits, y un componente w-signed con signo de 2 bits.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Vector 2D compuesto por dos valores de punto flotante de precisión sencilla. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Describe una estructura [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) alineada en un límite de 16 bytes. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Describe un vector 3D que consta de tres valores de punto flotante de precisión sencilla. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Describe una estructura [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) alineada en un límite de 16 bytes. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Describe un vector 3D con componentes X e y almacenados como número de punto flotante de 11 bits y componente Z almacenado como un valor de punto flotante de 10 bits.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Describe un vector 3D de tres componentes de punto flotante con mantisa de 9 bits, cada uno de los cuales comparte el mismo exponente de 5 bits.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Matriz de punto flotante de 3x3. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Una matriz de columnas principales de 3x4 que contiene componentes de punto flotante de 32 bits. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Una matriz de columnas principales de 3x4 que contiene componentes de punto flotante de 32 bits alineados en un límite de 16 bytes. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Describe un vector 4D que consta de cuatro valores de punto flotante de precisión sencilla.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Describe una estructura [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) alineada en un límite de 16 bytes. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Matriz de punto flotante 4x3. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Describe una estructura [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) alineada en un límite de 16 bytes. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Matriz de punto flotante 4x4. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Describe una estructura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) alineada en un límite de 16 bytes. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Vector 2D compuesto por dos valores de punto flotante de media precisión (16 bits).  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Describe un vector 4D que consta de cuatro valores de punto flotante de media precisión (16 bits).  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Vector 2D en el que cada componente es un entero con signo. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Vector 3D donde cada componente es un entero con signo. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Un vector 4D donde cada componente es un entero con signo. |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Describe una matriz 4x4 alineada en un límite de 16 bytes que se asigna a cuatro registros de vector de hardware. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Describe un vector 2D compuesto por componentes de enteros con signo y normalizados de 16 bits.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Vector 4D compuesto de componentes de tipo entero con signo de 16 bits.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Vector 2D para almacenar valores normalizados y firmados como enteros de 16 bits con signo (tipo `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Un vector 4D para almacenar valores normalizados y firmados como enteros de 16 bits con signo, (tipo `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Un vector 4D con x-, y-y los componentes z representados como valores enteros sin signo de 5 bits, y el componente w como un valor entero de 1 bit.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Un vector 3D con componentes x y z representados como valores enteros sin signo de 5 bits y el componente y como un valor entero de 6 bits sin signo. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Describe un vector 2D donde cada componente es un entero sin signo, de 8 bits (1 byte) de longitud. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Describe un vector 4D donde cada componente es un entero sin signo, de 8 bits (1 byte) de longitud.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Vector 2D para almacenar valores normalizados sin signo como enteros de 8 bits con signo (1 byte). |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Un vector 3D para almacenar valores normalizados sin signo como enteros de 8 bits con signo (1 byte).  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Un vector 4D con x-, y-y los componentes z representados como valores enteros sin signo de 10 bits y el componente w-como valor entero sin signo de 2 bits.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Un vector 4D para almacenar valores enteros sin signo y normalizados como componentes x-, y-y z-de 10 bits sin signo y un componente w-de 2 bits sin signo.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Vector 2D en el que cada componente es un entero sin signo. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Vector 3D en el que cada componente es un entero sin signo. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Un vector 4D en el que cada componente es un entero sin signo. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Un vector 4D con cuatro componentes enteros de 4 bits sin signo.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Describe un vector 2D compuesto por componentes enteros sin signo de 16 bits.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Vector 4D que consta de componentes de entero sin signo de 16 bits.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Vector 2D para almacenar valores normalizados sin signo como enteros de 16 bits sin signo, (tipo `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Un vector 4D para almacenar valores normalizados sin signo como enteros de 16 bits con signo (tipo `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Un vector 4D con x-, y-y los componentes z que se representan como valores enteros con signo de 10 bits y el componente w-como valor entero sin signo de 2 bits.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Un vector 4D para almacenar valores normalizados y firmados como componentes x-, y y z con signo de 10 bits, y un valor normalizado sin signo como componente w-de 2 bits sin signo.  |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>
