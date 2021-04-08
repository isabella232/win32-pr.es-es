---
title: Hoja de ruta para aplicaciones DirectX de escritorio
description: Estos son los recursos clave que le ayudarán a empezar a usar DirectX y C++ para desarrollar aplicaciones de escritorio con un uso intensivo de gráficos, como los juegos.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca95e1fe281253705620136afdced3cb705fe02
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104078647"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Hoja de ruta para aplicaciones DirectX de escritorio

Estos son los recursos clave que le ayudarán a empezar a usar DirectX y C++ para desarrollar aplicaciones de escritorio con un uso intensivo de gráficos, como los juegos. Esta no es una lista completa de todas las características o de los recursos disponibles.

## <a name="get-started"></a>Primeros pasos

Estos son algunos temas clave. Configurar el proyecto de DirectX, aclimatando a Windows y aplicaciones de ejemplo.

| Tema | Descripción |
|-|-|
| [Creación de la primera aplicación de Windows con DirectX](building-your-first-directx-app.md) | Use este tutorial básico para empezar a trabajar con el desarrollo de aplicaciones de DirectX y luego use el mapa de ruta para seguir explorando DirectX. |
| [Introducción a DirectX para Windows](getting-started-with-a-directx-game.md) | Revise los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++. |
| [Código completo de un marco de DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Obtiene el código para un marco básico de representación de DirectX. |
| [Cómo usar Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | En esta sección se muestra cómo usar la API de Microsoft Direct3D 11 para realizar varias tareas comunes. |
| [Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](/windows/desktop/direct3d11/dx-graphics-overviews) | La guía de programación contiene información sobre cómo usar la canalización programable de Microsoft Direct3D 11 para crear gráficos 3D en tiempo real para las aplicaciones de escritorio. |
| [Herramientas para gráficos de DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentación para las herramientas que se usan para admitir el desarrollo de DirectX. |
| [Novedades de Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Un desglose de todas las características agregadas en las versiones más recientes de DirectX y Direct3D (actualmente 11,2). |
| [Descarga de Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Debes tener Visual Studio Express 2013 para escritorio de Windows para crear juegos de la tienda Windows. Para ver un paseo por Visual Studio, consulte desarrollo de aplicaciones de la [tienda Windows con visual studio 2012](/previous-versions/windows/apps/br211384(v=win.10)). Para obtener información sobre las nuevas características de Visual Studio, consulte los [aspectos destacados del producto para Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md) | Contiene instrucciones para los desarrolladores que quieren traer sus proyectos de DirectX a Microsoft Visual Studio. |

## <a name="sample-applications"></a>Aplicaciones de ejemplo

| Tema | Descripción |
|-|-|
| [Tutorial de Direct3D ejemplo de Win32](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Ejemplo de tutorial básico de Direct3D de escritorio. |
| [Ejemplo de representación de vídeo en DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Un ejemplo que muestra la representación de vídeo personalizada con Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Revisar los conceptos clave de Direct3D 11

| Tema | Descripción |
|-|-|
| [Canalización de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Trata la canalización de gráficos de Direct3D 11 básica. |
| [Representación](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Trata los modelos de representación, los componentes, los sombreadores y el flujo de llamadas de API de Direct3D. |
| [Recursos](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Abarca "recursos" de Direct3D, como búferes y otros tipos de recursos de GPU. |
| [Efectos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Trata la creación de instancias y los efectos de Direct3D multishader.  |
| [Cómo: crear una cadena de intercambio](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Cómo crear la cadena de intercambio utilizada para dibujar píxeles en una región de la pantalla. |
| [Cómo: crear un dispositivo y un contexto inmediato](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Cómo crear una abstracción de dispositivo Direct3D y un contexto inmediato para el dibujo. |
| [Cómo: crear un búfer de vértices](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Cómo crear una lista simple de vértices de malla para su procesamiento por parte de la GPU. |
| [Cómo: crear un búfer de índice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Cómo crear un búfer de índice que permita al sombreador de vértices recorrer el orden de los vértices de una malla. |
| [Cómo: crear un búfer de constantes](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Cómo pasar datos constantes (uniformes) entre la CPU y la GPU durante la representación. |
| [Cómo: crear una textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Cómo crear una textura u otro recurso de búfer que pueda ser muestreado por la GPU. |
| [Cómo: inicializar una textura desde un archivo](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Cómo cargar una textura desde un archivo y procesarla para su uso por parte de la canalización del sombreador. |
| [Cómo: compilar un sombreador](../direct3d11/how-to--compile-a-shader.md) | Cómo compilar un sombreador para usarlo en la aplicación de gráficos. |

## <a name="graphics-apis"></a>API de gráficos

| Tema | Descripción |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentación de las API principales para la virtualización de la GPU y sus recursos, y para dibujar gráficos con un modelo de sombreador unificado. |
| [HLSL de Direct3D](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentación de referencia sobre el lenguaje de sombreador de High-Level, la sintaxis y las reglas que se usan para definir los programas de sombreador que se ejecutan como parte de la canalización de gráficos en un modelo de sombreador unificado. |
| [Interfaz de gráficos de DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentación de las API de bajo nivel que se usan para adquirir la interfaz de GPU y los recursos del sistema. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentación de las API de Direct2D, que admiten el dibujo de primitivos 2D. Normalmente, Direct2D se usa para las interfaces de usuario personalizadas, el procesamiento por lotes y el procesamiento de imágenes y los juegos sencillos. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentación de las API de DirectWrite, que admiten la representación y el escalado de fuentes personalizadas. |
| [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api) | Documentación para las API de WIC, que se usan para leer y administrar diferentes formatos de imagen de mapa de bits. |
| [Superficies de DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) para texturas | Documentación para las API de DDS, que se usan para la compresión y la descompresión de texturas 2D junto con las API de WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentación para las API de DirectXMath, que admiten Direct3D con un conjunto de tipos y funciones adecuadas para el desarrollo de gráficos en tiempo real 3D. (Anteriormente XNAMath). |
| [DirectCompute](https://walbourn.github.io/) | Documentación para las API de DirectCompute, que se usa para el proceso o la funcionalidad de sombreador de uso general. |

## <a name="audio-media-and-input-apis"></a>API de audio, multimedia y de entrada

| Tema | Descripción |
|-|-|
| [Guía de programación de XAudio2](/windows/desktop/xaudio2/programming-guide) | Nodo de nivel superior para la documentación conceptual de la API de audio de XAudio2. |
| [Referencia de programación de XAudio2](/windows/desktop/xaudio2/programming-reference) | Nodo de nivel superior para la documentación de referencia de la API de audio de XAudio2. |
| [Guía de programación de XInput](/windows/desktop/xinput/programming-guide) | Nodo de nivel superior para la documentación conceptual de la API de controlador de XInput. |
| [Referencia de programación de XInput](/windows/desktop/xinput/programming-reference) | Nodo de nivel superior para la documentación de referencia de la API del controlador de XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nodo de nivel superior para la documentación de la API de reproducción multimedia de Media Foundation (MF) (audio/vídeo). Normalmente, MF se usa en juegos para la reproducción de la banda sonora, mientras que XAudio2 se usa para el audio dinámico. |

## <a name="port-to-directx-11"></a>Puerto a DirectX 11

| Tema | Descripción |
|-|-|
| [Migración a Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Instrucciones básicas para mover el código base de DirectX 9 a DirectX 11. |
| [Técnicas de codificación de doble uso para juegos](https://walbourn.github.io/) | Entrada de blog detallada sobre el desarrollo de niveles de características de DirectX 9 \_ \* y DirectX 11 \_ \* en una sola aplicación. |
| [Implementación de búferes de sombra para el nivel de característica 9 de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10)) | Instrucciones para implementar mapas de instantáneas en el nivel de características 9 de DirectX \_ \* . |

## <a name="work-with-c"></a>Trabajar con C++

Si es una mano anterior con C++ en plataformas Windows, las cosas pueden tener un aspecto ligeramente diferente. Estos son algunos punteros a temas que pueden ayudarle a obtener un identificador de la diferencia.

> [!NOTE]
> Algunos de estos temas existen para ayudarle a mantener su aplicación de C++/CX. Pero se recomienda usar [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) para las nuevas aplicaciones. C++/WinRT es una moderna proyección de lenguaje C++17 totalmente estándar para las API de Windows Runtime (WinRT), implementada como una biblioteca basada en archivos de encabezado y diseñada para darte acceso de primera clase a la API moderna de Windows.

| Tema | Descripción |
|-|-|
| [**Referencia del lenguaje de Visual C++ (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Página de alto nivel que vincula a contenido relacionado con C++. |
| [**Referencia rápida (Windows Runtime y Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabla que proporciona información rápida sobre los operadores y palabras clave de las extensiones de componentes de Visual C++ (C++/CX). |
| [**Sistema de tipos (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Contenido de referencia para los tipos compatibles con C++/CX. |
| [**Espacios de nombres (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Contenido de referencia para los espacios de nombres que contienen tipos específicos de C++ que se pueden usar en aplicaciones de la tienda Windows. |

| | |
|-|-|
| [Programación asincrónica (DirectX y C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Obtenga información sobre la programación asincrónica y multiproceso para aplicaciones y juegos de DirectX. |
| [Programación asincrónica en C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Describe las formas básicas de usar la clase de tarea para consumir Windows Runtime métodos asincrónicos. |
| [**Task (clase) (Runtime de simultaneidad)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentación de referencia de la clase de tarea. |
| [Paralelismo de tareas (Runtime de simultaneidad)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Información detallada sobre la clase de tarea y cómo usarla. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Bibliotecas útiles adicionales para la programación de Windows C++

| | |
|-|-|
| [Biblioteca de plantillas estándar de C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows Runtime tipos juegan bien con los tipos de biblioteca de plantillas estándar. La mayoría de las aplicaciones de la tienda Windows de C++ usan los algoritmos y las colecciones de la biblioteca de plantillas estándar, excepto en el límite de ABI. |
| [Biblioteca de modelos de procesamiento paralelo (PPL)](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL proporciona algoritmos y tipos que simplifican el paralelismo de tareas y el paralelismo de datos en la CPU.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP proporciona acceso a la GPU para el paralelismo de datos de uso general en tarjetas de vídeo compatibles con DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blogs y otros recursos

| Tema | Descripción |
|-|-|
| [Blog de juegos para Windows y DirectX](https://walbourn.github.io/) | Blog actualizado periódicamente de un colaborador de desarrollo de DirectX clave y un excelente recurso todo en torno a los desarrolladores de DirectX. |
| [Blog para desarrolladores de Windows DirectX](https://devblogs.microsoft.com/directx/) | Blog oficial de Windows DirectX. |
| [Blog de DirectX de Shawn Hargreave](https://www.shawnhargreaves.com/blogindex.html) | Blog de desarrollo de otro colaborador de desarrollo de Windows para Windows DirectX. |
| [Kit de herramientas de DirectX](https://directxtk.codeplex.com/) | Sitio de CodePlex para el kit de herramientas de DirectX (DxTK), que contiene una serie de API de compatibilidad útiles para cargar mallas, reproducir sonidos y otros comportamientos comunes. |
| [Biblioteca de procesamiento de texturas de DirectXTex](https://directxtex.codeplex.com/) | Sitio de Plex de código para la biblioteca de procesamiento de texturas de DirectX (DxTEX), que contiene las API de compatibilidad para el procesamiento de texturas y la compresión y descompresión. |