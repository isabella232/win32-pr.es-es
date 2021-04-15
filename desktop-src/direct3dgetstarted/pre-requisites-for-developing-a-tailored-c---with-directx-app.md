---
title: Requisitos previos para el desarrollo con DirectX
description: Cuando empiece a desarrollar una aplicación de Windows con DirectX, tenga en cuenta los requisitos previos de esta página. Esto incluye las tecnologías que debe conocer antes de profundizar.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Aplicación DirectX, requisitos previos
- Aplicación DirectX, aplicación de la tienda Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d5e09484bef67546047214702fab7d2d0a5c48d
ms.sourcegitcommit: 6394972f1e8b01229db602469df6bb137e31d776
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/16/2020
ms.locfileid: "104488609"
---
# <a name="prerequisites-for-developing-with-directx"></a>Requisitos previos para el desarrollo con DirectX

Cuando empiece a desarrollar una aplicación de Windows con DirectX, tenga en cuenta los requisitos previos de esta página. Esto incluye las tecnologías que debe conocer antes de profundizar.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>¿Qué debo saber para desarrollar un juego de Windows con DirectX?

Antes de empezar a desarrollar una aplicación de la tienda Windows con DirectX, debe saber cómo programar en Windows con C++. Las aplicaciones de Windows que usan DirectX se desarrollan en un nivel bajo de programación, lo que significa que se expondrán a muchas características del sistema operativo. Entre ellas se incluyen la administración de memoria y recursos, y la interfaz para el propio dispositivo de gráficos. Si no está familiarizado con el desarrollo de aplicaciones de juegos o gráficos, puede encontrar este desafío. Sin embargo, también encontrará recompensas, ya que el desarrollo de juegos en este nivel crea muchas más posibilidades para el diseño y el desarrollo de aplicaciones de juegos y gráficos.

También necesitará comprender los aspectos básicos de la programación de gráficos 2D y 3D y de las matemáticas, ya que muchas de las API que va a usar se desarrollaron teniendo en cuenta estos principios. Le resultará más fácil comprender sus parámetros y resultados si está familiarizado con las operaciones subyacentes.

Como mínimo, debe tener una idea de lo siguiente:

-   Programación de Windows C/C++. Esto significa que comprende los punteros y referencias, eventos y devoluciones de llamada, y quizás algunas de las bibliotecas comunes, como ATL.
-   Programación de Win32. Comprende cómo se crean las ventanas y cómo se procesan los eventos de la interfaz de usuario. También comprende un poco más acerca de las API de Win32 y las API de Win32 esenciales.
-   Álgebra lineal y trigonometría. Aunque no es esencial, tendrá un tiempo más sencillo si está familiarizado con los conceptos de estas dos disciplinas matemáticas, ya que son la base de gran parte de la programación de gráficos 3D.
-   Terminología y conceptos básicos de los gráficos, como mapas de bits, texturas, vértices, mallas y ventanillas.

## <a name="what-does-directx-provide-me"></a>¿Qué me proporciona DirectX?

DirectX es el conjunto principal de API de gráficos que se usará para desarrollar juegos de Windows. Estas son las categorías de características con las que debe familiarizarse al decidir cómo desarrollar el juego.



| Biblioteca     | Descripción                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Un conjunto de bibliotecas eficaces y con aceleración de rendimiento y orientado al rendimiento para representar gráficos 3D.                                              |
| Direct2D    | Un conjunto de bibliotecas de gráficos 2D para el dibujo acelerado por hardware y el dibujo 2D vectorial.                                                           |
| DirectXMath | Biblioteca de operaciones matemáticas comunes y optimizadas utilizadas en gráficos 2D y 3D, como operaciones de vector y matriz.                                |
| DirectWrite | Biblioteca de API de representación y presentación de texto 2D. Admite la aceleración de hardware y la rasterización de software.                              |
| XAudio2     | Una API de audio de bajo nivel multiplataforma para Microsoft Windows que proporciona una base de procesamiento de señal y combinación de audio para el desarrollo de juegos. |
| XInput      | Una biblioteca que admite varios controles de juego tradicionales, con énfasis en el modelo de controladora Xbox 360.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>¿Qué herramientas necesito para desarrollar un juego de Windows con DirectX?

Para empezar a trabajar con este tutorial, necesitará lo siguiente:

-   Windows 8.1 o superior
-   Microsoft Visual Studio 2013 o superior

 

 




