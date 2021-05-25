---
title: Introducción a DirectX para Windows
description: Crear un juego de Microsoft DirectX para Windows es un desafío para un nuevo desarrollador. Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bac8ca2805fed9ec42faf9deda9ddd51da39685
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343590"
---
# <a name="get-started-with-directx-for-windows"></a>Introducción a DirectX para Windows

Crear un juego de Microsoft DirectX para Windows es un desafío para un nuevo desarrollador. Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.

Comencemos.

## <a name="what-skills-do-you-need"></a>¿Qué aptitudes necesita?

Para desarrollar un juego en DirectX para Windows, debe tener algunas aptitudes básicas. En concreto, debe poder:

-   Lea y escriba código C++ moderno (C++11 ayuda al máximo) y familiarícese con los principios y patrones básicos de diseño de C++, como las plantillas y el modelo de fábrica. También debe estar familiarizado con las bibliotecas comunes de C++, como la biblioteca de plantillas estándar, y específicamente con los operadores de conversión, los tipos de puntero y las estructuras de datos de la biblioteca de plantillas estándar (como std::vector).
-   Comprenda la geometría básica, la trigonometría y el álgebra lineal. Gran parte del código que encontrará en los ejemplos supone que comprende estas formas de matemáticas y sus reglas comunes.
-   Familiarícese con COM, especialmente [**Microsoft::WRL::ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntero inteligente).
-   Comprenda los fundamentos de la tecnología de gráficos y gráficos, especialmente los gráficos 3D. Aunque DirectX tiene su propia terminología, todavía se basa en una comprensión bien establecida de los principios generales de gráficos 3D.
-   Comprenda el concepto de bucle de mensajes, ya que implementará un bucle que escucha el sistema operativo Windows.

## <a name="and-were-off"></a>Y estamos apagados.

¿Estás listo para empezar? Vamos a revisar antes de empezar. Ha:

-   Una instalación actualizada y en funcionamiento de Windows 8.1.
-   Una instalación de [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Un miedo intrépido y un deseo de obtener más información sobre el desarrollo de juegos de DirectX.

## <a name="next-steps"></a>Pasos siguientes



| Tema                                                                                                   | Descripción                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Trabajar con recursos de dispositivo DirectX](work-with-dxgi.md)                                           | Obtenga información sobre cómo usar DXGI para crear un dispositivo gráfico virtualizado y crear y configurar una cadena de intercambio.     |
| [Información sobre la canalización de representación de Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Obtenga información sobre cómo enlazar a la clase de recursos de dispositivo DirectX y dibujar mediante la canalización de gráficos de Direct3D. |
| [Trabajar con sombreadores y recursos de sombreador](work-with-shaders-and-shader-resources.md)               | Aprenda a escribir programas de sombreador HLSL para las fases de canalización de gráficos de Direct3D.                            |



 

 

 