---
description: La biblioteca DirectXMath se basa en la versión 2.x de la biblioteca SIMD de C++ matemática de XNA. Aquí se describe cómo se diferencia DirectXMath de XNA Math y cómo difieren las versiones de DirectXMath.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Novedades (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df1e7f25789ca6f58205ce9f45482e0a49540d1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827631"
---
# <a name="whats-new-directxmath"></a>Novedades (DirectXMath)

La biblioteca DirectXMath se basa en la versión [2.04](https://walbourn.github.io/xna-math-version-2-04/)de la biblioteca SIMD de C++ matemática de XNA. Aquí se describe cómo se diferencia DirectXMath de XNA Math y cómo difieren las versiones de DirectXMath.

-   [Historial de versión preliminar](#release-history)
-   [Diferencias de DirectXMath con respecto a XNA Math](#directxmath-differences-from-xna-math)
-   [Temas relacionados](#related-topics)

## <a name="release-history"></a>Historial de versiones

<table>
 <tr>
  <td>Windows 10 SDK (20348), versión 2104</td><td>DirectXMath 3.16</td>
 </td>
 <tr>
  <td>Windows 10 SDK de actualización de mayo de 2020</td><td>DirectXMath 3.14</td>
 </tr>
 <tr>
  <td>ACTUALIZACIÓN DE OCTUBRE DE 2018 DE WINDOWS 10 SDK</td><td>DirectXMath 3.13</td>
 </tr>
 <tr>
  <td>ACTUALIZACIÓN DE ABRIL DE 2018 DE WINDOWS 10 SDK<br />Windows 10 Fall Creators Update SDK</td><td>DirectXMath 3.11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update SDK</td><td>DirectXMath 3.10</td>
 </tr>
 <tr>
  <td>SDK de Windows 10 Anniversary</td><td>DirectXMath 3.09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (noviembre de 2015)</td><td>DirectXMath 3.08</td>
 </tr>
 <tr>
  <td>Windows SDK para Windows 8.1 (spring 2015)</td><td>DirectXMath 3.07</td>
 </tr>
 <tr>
  <td>Windows SDK para Windows 8.1</td><td>DirectXMath 3.06</td>
 </tr>
 <tr>
  <td>Windows SDK para Windows 8</td><td>DirectXMath 3.03</td>
 </tr>
</table>

Consulte [Versiones de DirectXMath](https://github.com/Microsoft/DirectXMath/releases) para obtener más información.

## <a name="directxmath-differences-from-xna-math"></a>Diferencias de DirectXMath con respecto a XNA Math

Este es el modo en que la biblioteca DirectXMath difiere principalmente de la biblioteca matemática de XNA:

-   DirectXMath es solo C++ (espacios de nombres, sobrecargas, nuevas plantillas, entre otros).
-   Requiere compatibilidad con la biblioteca estándar de C++11 (es decir, stdint.h, y así sucesivamente).
-   Compatibilidad intrínseca de ARM-NEON con la plataforma Windows RT sistema.
-   Nueva funcionalidad de color (conversiones de espacio de color, constantes de color de .NET).
-   Límite de tipos de volumen (una versión de la que se encontraba anteriormente en el encabezado XNACollision en el ejemplo de colisión del SDK de DirectX).
-   No hay Xbox 360 versión disponible. El Xbox 360 XDK continúa con el envío de XNAMath v2.x; eliminación de Xbox 360 tipos de datos y variantes de función específicos.
-   [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) se ha reelatrado para mejorar la optimización de los intrínsecos SSE y ARM-NEON.
-   El [**tipo XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) es totalmente opaco. Para acceder a elementos individuales **de XMMATRIX,** use otros tipos como [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versiones de DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
