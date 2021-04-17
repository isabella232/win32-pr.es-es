---
title: Introducción a DirectX para Windows
description: Crear un juego de Microsoft DirectX para Windows es un reto para un nuevo desarrollador. Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.
ms.assetid: fd460c52-9854-4ffe-b89e-5219be2e11f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae09cd127a30401ae0493f5dd770fe1e67607b45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704975"
---
# <a name="get-started-with-directx-for-windows"></a>Introducción a DirectX para Windows

Crear un juego de Microsoft DirectX para Windows es un reto para un nuevo desarrollador. Aquí se revisan rápidamente los conceptos implicados y los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++.

Empecemos.

## <a name="what-skills-do-you-need"></a>¿Qué conocimientos necesita?

Para desarrollar un juego en DirectX para Windows, debe tener unos conocimientos básicos. En concreto, debe ser capaz de:

-   Lea y escriba código moderno de C++ (C++ 11 ayuda a la mayoría) y familiarícese con los principios básicos y patrones de diseño de C++, como las plantillas y el modelo de fábrica. También debe estar familiarizado con las bibliotecas comunes de C++ como la biblioteca de plantillas estándar y, en concreto, con los operadores de conversión, los tipos de puntero y las estructuras de datos de la biblioteca de plantillas estándar (como STD:: Vector).
-   Comprenda la geometría básica, las trigonometría y el álgebra lineal. Gran parte del código que encontrará en los ejemplos supone que comprende estas formas de matemáticas y sus reglas comunes.
-   Familiarícese con COM, especialmente [**Microsoft:: WRL:: ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) (puntero inteligente).
-   Comprenda las bases de la tecnología de gráficos y gráficos, especialmente los gráficos 3D. Aunque DirectX tiene su propia terminología, todavía se basa en una comprensión bien establecida de los principios generales de gráficos 3D.
-   Comprenda el concepto de un bucle de mensajes, ya que va a implementar un bucle que realiza escuchas en el sistema operativo Windows.

## <a name="and-were-off"></a>Y estamos desactivados.

¿Estás listo para empezar? Vamos a revisar antes de empezar. Ha:

-   Instalación actualizada y en funcionamiento de Windows 8.1.
-   Instalación de [Microsoft Visual Studio](https://visualstudio.microsoft.com/downloads/download-visual-studio-vs).
-   Un espíritu Intrepid y el deseo de obtener más información sobre el desarrollo de juegos de DirectX.

## <a name="next-steps"></a>Pasos siguientes



|                                                                                                    |                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Trabajar con recursos de dispositivos DirectX](work-with-dxgi.md)                                           | Obtenga información sobre cómo usar DXGI para crear un dispositivo de gráficos virtualizado y crear y configurar una cadena de intercambio.     |
| [Descripción de la canalización de representación de Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md) | Obtenga información sobre cómo enlazar a la clase de recursos de dispositivo DirectX y cómo dibujar mediante la canalización de gráficos Direct3D. |
| [Trabajar con sombreadores y recursos del sombreador](work-with-shaders-and-shader-resources.md)               | Obtenga información sobre cómo escribir programas de sombreador HLSL para las fases de canalización de gráficos de Direct3D.                            |



 

 

 