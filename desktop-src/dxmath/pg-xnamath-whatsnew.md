---
description: La biblioteca de DirectXMath se basa en la biblioteca SIMD de C++ matemática de XNA versión 2. x. Aquí se describe el modo en que DirectXMath difiere de la matemáticas de XNA y cómo difieren las versiones de DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novedades (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696711"
---
# <a name="whats-new-directxmath"></a>Novedades (DirectXMath)

La biblioteca de DirectXMath se basa en la [versión 2,04 de la biblioteca SIMD de C++ matemática de XNA](https://walbourn.github.io/). Aquí se describe el modo en que DirectXMath difiere de la matemáticas de XNA y cómo difieren las versiones de DirectXMath.

-   [Historial de Rlease](#release-history)
-   [Diferencias de DirectXMath con las matemáticas de XNA](#directxmath-differences-from-xna-math)
-   [Temas relacionados](#related-topics)

## <a name="release-history"></a>Historial de versiones

<table>
 <tr>
  <td>SDK de Windows 10 May 2020 Update</td><td>DirectXMath 3,14</td>
 </tr>
 <tr>
  <td>SDK de la actualización 2018 de octubre de Windows 10</td><td>DirectXMath 3,13</td>
 </tr>
 <tr>
  <td>SDK de la actualización de abril de 2018 de Windows 10<br />SDK de Windows 10 Fall Creators Update</td><td>DirectXMath 3,11</td>
 </tr>
 <tr>
  <td>SDK de Windows 10 Creators Update</td><td>DirectXMath 3,10</td>
 </tr>
 <tr>
  <td>SDK de Windows 10 Anniversary</td><td>DirectXMath 3,09</td>
 </tr>
 <tr>
  <td>SDK de Windows 10 (2015 de noviembre)</td><td>DirectXMath 3,08</td>
 </tr>
 <tr>
  <td>Windows SDK para Windows 8.1 (Spring 2015)</td><td>DirectXMath 3,07</td>
 </tr>
 <tr>
  <td>Windows SDK para Windows 8.1</td><td>DirectXMath 3,06</td>
 </tr>
 <tr>
  <td>Windows SDK para Windows 8</td><td>DirectXMath 3,03</td>
 </tr>
</table>

Consulte [versiones de DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obtener más información.

## <a name="directxmath-differences-from-xna-math"></a>Diferencias de DirectXMath con las matemáticas de XNA

Aquí se muestra cómo la biblioteca de DirectXMath difiere principalmente de la biblioteca matemática de XNA:

-   DirectXMath es solo C++ (espacios de nombres, sobrecargas, nuevas plantillas, etc.).
-   Requiere compatibilidad con la biblioteca estándar de C++ 11 (es decir, stdint. h, etc.).
-   Compatibilidad con las funciones intrínsecas ARM-neón para la plataforma de Windows RT.
-   Nueva funcionalidad de color (conversiones de espacio de colores, constantes de color de .NET).
-   Tipos de volumen de límite (una versión de que se encontraba anteriormente en el encabezado XNACollision en el ejemplo de colisión del SDK de DirectX).
-   No hay disponible ninguna versión de Xbox 360. La consola Xbox 360 XDK continúa distribuyendo XNAMath V2. x; eliminación de tipos de datos específicos de Xbox 360 y variantes de función.
-   [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) trabajada para optimizar la optimización de los intrínsecos SSE y ARM-neón.
-   El tipo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) es totalmente opaco. Para tener acceso a elementos individuales de **XMMATRIX**, use otros tipos como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versiones de DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
