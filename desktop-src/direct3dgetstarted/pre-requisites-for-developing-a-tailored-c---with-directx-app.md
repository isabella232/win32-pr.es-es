---
title: Requisitos previos para desarrollar con DirectX
description: Cuando empiece a desarrollar una aplicación Windows con DirectX, tenga en cuenta los requisitos previos de esta página. Esto incluye las tecnologías que debe conocer antes de profundizar.
ms.assetid: 93f566cf-0c16-4487-9d53-dc59746e4d00
keywords:
- Aplicación DirectX, requisitos previos
- Aplicación DirectX, Windows Store
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c575fc24da5632582e30b9786d8c800161e5ad1a1cfbc765aa5ec33db3f94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950995"
---
# <a name="prerequisites-for-developing-with-directx"></a>Requisitos previos para desarrollar con DirectX

Cuando empiece a desarrollar una aplicación Windows con DirectX, tenga en cuenta los requisitos previos de esta página. Esto incluye las tecnologías que debe conocer antes de profundizar.

## <a name="what-should-i-know-to-develop-a-windows-game-using-directx"></a>¿Qué debo saber para desarrollar un Windows con DirectX?

Antes de empezar a desarrollar una aplicación Windows Store mediante DirectX, debe saber cómo programar en Windows con C++. Windows aplicaciones que usan DirectX se desarrollan en un bajo nivel de programación, lo que significa que estará expuesto a muchas características del sistema operativo. Estos incluyen la administración de recursos y memoria, y la interfaz para el propio dispositivo gráfico. Si no está nuevo en el desarrollo de aplicaciones de juegos o gráficos, puede que le sea difícil. Pero también lo encontrará recompensado, ya que el aprendizaje del desarrollo de juegos en este nivel crea posibilidades mucho más grandes para el diseño y el desarrollo de aplicaciones de juegos y gráficos.

También deberá comprender los conceptos básicos de la programación y matemáticas de gráficos 2D y 3D, ya que muchas de las API que usará se desarrollaron pensando en estos principios. Si está familiarizado con las operaciones subyacentes, le será más fácil comprender sus parámetros y resultados.

Como mínimo, debe comprender lo siguiente:

-   Windows Programación de C/C++. Esto significa que comprende punteros y referencias, eventos y devoluciones de llamada, y quizás algunas de las bibliotecas comunes como ATL.
-   Programación de Win32. Comprende cómo se crean las ventanas y cómo se procesan los eventos de la interfaz de usuario. También comprende un poco sobre LAS API COM y Win32 esenciales.
-   Álgebra lineal y trigonometría. Aunque no es esencial, lo tendrá más fácil si está familiarizado con los conceptos de estas dos materias matemáticas, ya que son la base de gran parte de la programación de gráficos 3D.
-   Terminología y conceptos básicos de gráficos, como mapas de bits, texturas, vértices, mallas y ventanillas.

## <a name="what-does-directx-provide-me"></a>¿Qué me proporciona DirectX?

DirectX es el conjunto principal de API de gráficos que usará para desarrollar Windows juegos. Estas son las categorías de características con las que debe familiarizarse cuando decida cómo desarrollar el juego.



| Biblioteca     | Descripción                                                                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D    | Un conjunto eficaz de bibliotecas aceleradas por hardware y orientadas al rendimiento para representar gráficos 3D.                                              |
| Direct2D    | Conjunto de bibliotecas de gráficos 2D para mapas de bits acelerados por hardware y dibujos 2D vectoriales.                                                           |
| DirectXMath | Una biblioteca de operaciones matemáticas comunes y optimizadas que se usan en gráficos 2D y 3D, como operaciones de vector y matriz.                                |
| DirectWrite | Una biblioteca de API de representación y diseño de texto 2D. Admite la aceleración de hardware y la rasterización de software.                              |
| XAudio2     | Una API de audio multiplataforma de bajo nivel para Microsoft Windows que proporciona una base de procesamiento de señales y combinación de audio para el desarrollo de juegos. |
| XInput      | Una biblioteca que admite varios controles de juegos tradicionales, con énfasis en el modelo Xbox 360 controlador.                                 |



 

## <a name="what-tools-do-i-need-to-develop-a-windows-game-with-directx"></a>¿Qué herramientas necesito para desarrollar un Windows con DirectX?

Para empezar a trabajar con este tutorial, necesita:

-   Windows 8.1 o superior
-   Microsoft Visual Studio 2013 o posterior

 

 




