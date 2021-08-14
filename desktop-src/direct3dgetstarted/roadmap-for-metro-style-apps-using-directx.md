---
title: Hoja de ruta para aplicaciones DirectX de escritorio
description: Estos son los recursos clave que le ayudarán a empezar a usar DirectX y C++ para desarrollar aplicaciones de escritorio con un uso intensivo de gráficos, como juegos.
ms.assetid: d7921f38-e384-4a83-b458-ee71f7044468
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5940e775de65d6d22a9b244d1bd0b881240cf296b740c9a0be9c38f3ab0725a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983895"
---
# <a name="roadmap-for-desktop-directx-apps"></a>Hoja de ruta para aplicaciones DirectX de escritorio

Estos son los recursos clave que le ayudarán a empezar a usar DirectX y C++ para desarrollar aplicaciones de escritorio con un uso intensivo de gráficos, como juegos. Esta no es una lista completa de todas las características o recursos disponibles.

## <a name="get-started"></a>Introducción

Estos son algunos temas clave. Configuración del proyecto de DirectX, aclimatándose a Windows aplicaciones de ejemplo.

| Tema | Descripción |
|-|-|
| [Creación de la primera Windows aplicación mediante DirectX](building-your-first-directx-app.md) | Use este tutorial básico para empezar a trabajar con el desarrollo de aplicaciones de DirectX y, a continuación, use la hoja de ruta para seguir explorando DirectX. |
| [Introducción a DirectX para Windows](getting-started-with-a-directx-game.md) | Revise los pasos que debe seguir para empezar a desarrollar un juego con DirectX y C++. |
| [Código completo para un marco de trabajo de DirectX](complete-code-sample-for-using-a-corewindow-with-directx.md) | Obtenga el código para un marco de representación básico de DirectX. |
| [Uso de Direct3D 11](/windows/desktop/direct3d11/how-to-use-direct3d-11) | En esta sección se muestra cómo usar la API de Microsoft Direct3D 11 para realizar varias tareas comunes. |
| [Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](/windows/desktop/direct3d11/dx-graphics-overviews) | La guía de programación contiene información sobre cómo usar la canalización programable de Microsoft Direct3D 11 para crear gráficos 3D en tiempo real para aplicaciones de escritorio. |
| [Herramientas para gráficos DirectX](/windows/desktop/direct3dtools/dx-graphics-tools) | Documentación de las herramientas que se usan para admitir el desarrollo de DirectX. |
| [Novedades de Direct3D 11](/windows/desktop/direct3d11/dx-graphics-overviews-introduction) | Un desglose de todas las características agregadas en las versiones más recientes de DirectX y Direct3D (actualmente 11.2). |
| [Descarga de Visual Studio 2013](https://msdn.microsoft.com/windows/apps/br229516.aspx) | Debe tener la Visual Studio Express 2013 para escritorio de Windows crear juegos Windows Store. Para ver un paseo por Visual Studio, consulte [Desarrollo de Windows Store con Visual Studio 2012.](/previous-versions/windows/apps/br211384(v=win.10)) Para obtener información sobre las nuevas características Visual Studio, vea [Product Highlights for Visual Studio 2013](/previous-versions/visualstudio/visual-studio-2013/bb386063(v=vs.120)). |
| [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md) | Contiene instrucciones para desarrolladores que desean llevar sus proyectos de DirectX a Microsoft Visual Studio. |

## <a name="sample-applications"></a>Aplicaciones de ejemplo

| Tema | Descripción |
|-|-|
| [Ejemplo de Win32 del tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) | Ejemplo de tutorial básico de Direct3D de escritorio. |
| [Ejemplo de representación de vídeo de DirectX](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20video%20rendering%20sample) | Ejemplo que muestra la representación de vídeo personalizada con Direct3D. |

## <a name="review-key-direct3d-11-concepts"></a>Revisión de los conceptos clave de Direct3D 11

| Tema | Descripción |
|-|-|
| [Canalización de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) | Trata la canalización de gráficos básica de Direct3D 11. |
| [Representación](/windows/desktop/direct3d11/overviews-direct3d-11-render) | Trata los modelos de representación de Direct3D, los componentes, los sombreadores y el flujo de llamadas de API. |
| [Recursos](/windows/desktop/direct3d11/overviews-direct3d-11-resources) | Trata los "recursos" de Direct3D, como los búferes y otros tipos de recursos de GPU. |
| [Efectos](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects) | Trata los efectos y la creación de instancias de varios sombreadores de Direct3D.  |
| [Cómo: Crear una cadena de intercambio](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-swap-chain) | Cómo crear la cadena de intercambio usada para dibujar píxeles en una región de la pantalla. |
| [Cómo: Crear un dispositivo y un contexto inmediato](/windows/desktop/direct3d11/overviews-direct3d-11-devices-initialize) | Cómo crear una abstracción de dispositivos Direct3D y un contexto inmediato para dibujar. |
| [Cómo: Crear un búfer de vértices](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-vertex-how-to) | Cómo crear una lista simple de vértices de malla para su procesamiento por la GPU. |
| [Cómo: Crear un búfer de índice](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-index-how-to) | Cómo crear un búfer de índice que permita al sombreador de vértices recorrer el orden de los vértices en una malla. |
| [Cómo: Crear un búfer constante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to) | Cómo pasar datos constantes (uniformes) entre la CPU y la GPU durante la representación. |
| [Cómo: Crear una textura](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create) | Cómo crear una textura u otro recurso de búfer que la GPU pueda muestrear. |
| [Cómo: Inicializar una textura a partir de un archivo](/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-how-to) | Cómo cargar una textura de un archivo y procesarla para que la use la canalización del sombreador. |
| [Cómo: Compilar un sombreador](../direct3d11/how-to--compile-a-shader.md) | Cómo compilar un sombreador para su uso en la aplicación de gráficos. |

## <a name="graphics-apis"></a>API de gráficos

| Tema | Descripción |
|-|-|
| [Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference) | Documentación de las API principales para la virtualización de la GPU y sus recursos, y para dibujar gráficos mediante un modelo de sombreador unificado. |
| [Direct3D HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) | Documentación de referencia High-Level lenguaje de sombreador, la sintaxis y las reglas que se usan para definir programas de sombreador ejecutados como parte de la canalización de gráficos en un modelo de sombreador unificado. |
| [Interfaz de gráficos DirectX (DXGI)](/windows/desktop/direct3ddxgi/dx-graphics-dxgi) | Documentación de las API de bajo nivel que se usan para adquirir la interfaz de GPU y los recursos del sistema. |
| [Direct2D](/windows/desktop/Direct2D/direct2d-portal) | Documentación de las API de Direct2D, que admiten el dibujo de primitivas 2D. Normalmente, Direct2D se usa para interfaces de usuario personalizadas, procesamiento y procesamiento por lotes de imágenes y juegos sencillos. |
| [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) | Documentación de las API DirectWrite, que admiten la representación y el escalado de fuentes personalizadas. |
| [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api) | Documentación de las API de WIC, que se usan para leer y administrar diferentes formatos de imagen de mapa de bits. |
| [Superficies DirectDraw (DDS)](/windows/desktop/direct3ddds/dx-graphics-dds) para texturas | Documentación de las API de DDS, que se usan para la compresión de textura 2D y la descompresión junto con las API de WIC. |
| [DirectXMath](/windows/desktop/dxmath/directxmath-portal) | Documentación de las API de DirectXMath, que admiten Direct3D con un conjunto de tipos y funciones adecuados para el desarrollo de gráficos en tiempo real en 3D. (Anteriormente XNAMath). |
| [DirectCompute](https://walbourn.github.io/) | Documentación de las API de DirectCompute, que se usa para la funcionalidad de sombreador de uso general o de proceso. |

## <a name="audio-media-and-input-apis"></a>API de audio, multimedia y entrada

| Tema | Descripción |
|-|-|
| [Guía de programación de XAudio2](/windows/desktop/xaudio2/programming-guide) | Nodo de nivel superior para la documentación conceptual de la API de audio XAudio2. |
| [Referencia de programación de XAudio2](/windows/desktop/xaudio2/programming-reference) | Nodo de nivel superior para la documentación de referencia de la API de audio XAudio2. |
| [Guía de programación de XInput](/windows/desktop/xinput/programming-guide) | Nodo de nivel superior para la documentación conceptual de la API del controlador XInput. |
| [Referencia de programación de XInput](/windows/desktop/xinput/programming-reference) | Nodo de nivel superior para la documentación de referencia de la API del controlador XInput. |
| [Media Foundation](/windows/desktop/medfound/about-the-media-foundation-sdk) | Nodo de nivel superior para la documentación Media Foundation API de reproducción de multimedia (MF) (audio/vídeo). Normalmente, MF se usa en juegos para la reproducción de música, mientras que XAudio2 se usa para el audio dinámico. |

## <a name="port-to-directx-11"></a>Puerto a DirectX 11

| Tema | Descripción |
|-|-|
| [Migración a Direct3D 11](/windows/desktop/direct3d11/d3d11-programming-guide-migrating) | Guía básica para mover el código base de DirectX 9 a DirectX 11. |
| [Técnicas de codificación de doble uso para juegos](https://walbourn.github.io/) | Entrada de blog detallada sobre el desarrollo de niveles de características de DirectX 9 y \_ \* DirectX 11 \_ \* en una sola aplicación. |
| [Implementación de búferes de sombra para el nivel 9 de característica de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10)) | Guía para implementar mapas de sombra en el nivel de característica 9 de \_ \* DirectX. |

## <a name="work-with-c"></a>Trabajar con C++

Si es una mano antigua con C++ en Windows plataformas, las cosas pueden parecer un poco diferentes. Estos son algunos punteros a temas que pueden ayudarle a controlar la diferencia.

> [!NOTE]
> Algunos de estos temas existen para ayudarle a mantener la aplicación de C++/CX. Pero se recomienda usar [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/intro-to-using-cpp-with-winrt) para nuevas aplicaciones. C++/WinRT es una moderna proyección de lenguaje C++17 totalmente estándar para las API de Windows Runtime (WinRT), implementada como una biblioteca basada en archivos de encabezado y diseñada para darte acceso de primera clase a la API moderna de Windows.

| Tema | Descripción |
|-|-|
| [**Visual C++ referencia del lenguaje (C++/CX)**](/cpp/cppcx/visual-c-language-reference-c-cx?view=vs-2019) | Página de alto nivel que vincula a contenido relacionado con C++. |
| [**Referencia rápida (Windows Runtime y Visual C++)**](/cpp/cppcx/quick-reference-c-cx?view=vs-2019) | Tabla que proporciona información rápida sobre las Visual C++ y palabras clave de extensiones de componentes (C++/CX). |
| [**Sistema de tipos (C++/CX)**](/cpp/cppcx/type-system-c-cx?view=vs-2019) | Contenido de referencia para los tipos admitidos por C++/CX. |
| [**Espacios de nombres (C++/CX)**](/cpp/cppcx/namespaces-reference-c-cx?view=vs-2019) | Contenido de referencia para los espacios de nombres que contienen tipos específicos de C++ que se pueden usar en Windows Store. |

| Tema | Descripción |
|-|-|
| [Programación asincrónica (DirectX y C++)](/previous-versions/windows/apps/hh994919(v=win.10)) | Obtenga información sobre la programación asincrónica y multiproceso para aplicaciones y juegos de DirectX. |
| [Programación asincrónica en C++](/previous-versions/windows/apps/hh780559(v=win.10)) | Describe las formas básicas de usar la clase de tarea para consumir Windows en tiempo de ejecución. |
| [**task (Clase) (Runtime de simultaneidad)**](/previous-versions/visualstudio/visual-studio-2012/hh750113(v=vs.110)) | Documentación de referencia de la clase de tarea. |
| [Paralelismo de tareas (Runtime de simultaneidad)](/previous-versions/visualstudio/visual-studio-2010/dd492427(v=vs.100)) | Explicación detallada sobre la clase de tarea y cómo usarla. |

## <a name="additional-useful-libraries-for-windows-c-programming"></a>Bibliotecas útiles adicionales para Windows programación de C++

| Tema | Descripción |
|-|-|
| [Biblioteca de plantillas estándar de C++](https://msdn.microsoft.com/library/c191tb28(v=VS.71).aspx) | Windows Los tipos en tiempo de ejecución se reproducen bien con los tipos de biblioteca de plantillas estándar. La mayoría de las aplicaciones Windows Store de C++ usan algoritmos y colecciones de biblioteca de plantillas estándar, excepto en el límite de ABI. |
| [Biblioteca de modelos de procesamiento paralelo (PPL)](/previous-versions/visualstudio/visual-studio-2010/dd492418(v=vs.100)) | PPL proporciona algoritmos y tipos que simplifican el paralelismo de tareas y el paralelismo de datos en la CPU.  |
| [C++ Accelerated Massive Parallelism (C++ AMP)](/previous-versions/visualstudio/visual-studio-2012/hh265137(v=vs.110)) | C++ AMP proporciona acceso a la GPU para el paralelismo de datos de uso general en tarjetas de vídeo que admiten DirectX 11. |

## <a name="blogs-and-other-resources"></a>Blogs y otros recursos

| Tema | Descripción |
|-|-|
| [Blog de Games for Windows y DirectX](https://walbourn.github.io/) | Blog actualizado periódicamente de un colaborador clave de desarrollo de DirectX y un excelente recurso para desarrolladores de DirectX. |
| [Windows Blog para desarrolladores de DirectX](https://devblogs.microsoft.com/directx/) | Blog oficial Windows DirectX. |
| [Blog de DirectX de Hargreave](https://www.shawnhargreaves.com/blogindex.html): | Blog de desarrollo de otro colaborador Windows colaborador de desarrollo de DirectX. |
| [Kit de herramientas de DirectX](https://directxtk.codeplex.com/) | Sitio de CodePlex para el Kit de herramientas de DirectX (DxTK), que contiene una serie de API de soporte útiles para cargar mallas, reproducir sonidos y otros comportamientos comunes. |
| [Biblioteca de procesamiento de texturas de DirectXTex](https://directxtex.codeplex.com/) | Sitio de plex de código para directX Texture Processing Library (DxTEX), que contiene API de compatibilidad para el procesamiento de texturas y la compresión/descompresión. |