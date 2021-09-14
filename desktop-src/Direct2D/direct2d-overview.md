---
title: Acerca de Direct2D
description: Presenta Direct2D, una API que proporciona a los desarrolladores de Win32 la capacidad de realizar tareas de representación de gráficos 2D con un rendimiento y una calidad visual superiores.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D,about
- Direct2D, interoperabilidad
- Direct2D, rendimiento
- Direct2D, disponibilidad
- Direct2D,applications
- interoperabilidad, Direct2D
- rendimiento de Direct2D
- disponibilidad para Direct2D
- aplicaciones para Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163357"
---
# <a name="about-direct2d"></a>Acerca de Direct2D

En este tema se presenta Direct2D, una API que proporciona a los desarrolladores de Win32 la capacidad de realizar tareas de representación de gráficos 2D con un rendimiento y una calidad visual superiores.

## <a name="what-is-direct2d"></a>¿Qué es Direct2D?

Direct2D es una API de gráficos 2D acelerada por hardware e inmediata que proporciona un alto rendimiento y una representación de alta calidad para geometría 2D, mapas de bits y texto. La API de Direct2D está diseñada para interoperar con código existente que usa GDI, GDI+ o Direct3D.

Direct2D está diseñado principalmente para su uso por las siguientes clases de desarrolladores:

-   Desarrolladores de aplicaciones nativas de gran escala empresarial.
-   Desarrolladores que crean kits de herramientas de control y bibliotecas para su consumo por parte de desarrolladores de nivel inferior.
-   Desarrolladores que requieren la representación del lado servidor de gráficos 2D.
-   Desarrolladores que usan gráficos Direct3D y necesitan una representación 2D y de texto sencilla y de alto rendimiento para menús, elementos de la interfaz de usuario (UI) y pantallas de visualización directa (HUD).

## <a name="why-direct2d"></a>¿Por qué Direct2D?

Las motivaciones principales para crear una nueva API de gráficos 2D en Microsoft Windows incluyen las siguientes:

-   Para mantener el ritmo del creciente nivel de enriquecimiento visual al que están acostumbrados Windows los usuarios.
-   Para permitir que los desarrolladores escriban código de representación 2D que se escala directamente con el hardware de procesamiento de gráficos del equipo en el que se ejecuta.
-   Para permitir que los desarrolladores escriban código para representar gráficos 2D que se puedan ejecutar en el contexto de un servicio.

En los últimos años, los usuarios finales han empezado a esperar una mayor fidelidad visual en las experiencias digitales. Esta tendencia se refleja en la electrónica de consumidor. Los dispositivos GPS, los dispositivos de reproducción multimedia, los teléfonos móviles y las cámaras digitales ofrecen experiencias continuamente más enriquecciones año tras año. Esta tendencia también se puede observar en la diversidad de contenido gráfico en películas, televisión, juegos de vídeo y en la Web. Para mantenerse al día con estos cambios, se pide a los desarrolladores que lleve sus aplicaciones de Windows existentes al siguiente nivel de enriquecimiento visual.

Los procesadores gráficos de los equipos Windows modernos también han evolucionado constantemente, controlados por los avances en los gráficos de los juegos de vídeo y en partes de la experiencia de Windows como Windows Media Center y Aero. Algunas Windows aplicaciones pueden aprovechar las GPU modernas mediante Microsoft Direct3D y Windows Presentation Foundation (WPF). Aunque Direct3D sirve aplicaciones de gráficos 3D de gama alta y WPF aborda las necesidades de los desarrolladores de .NET, existen lagunas para los desarrolladores que tienen grandes bases de código existentes para representar código basado en GDI y GDI+ o que desean incorporar gráficos 2D de alta calidad en sus aplicaciones basadas en Direct3D.

Por último, la necesidad de una API de gráficos que se pueda usar en un servicio se ha convertido en un requisito emergente para los desarrolladores que trabajan en escenarios empresariales y de desarrollo web. Las API de representación existentes se centran en la representación del lado cliente en una sola sesión de usuario. Por lo tanto, pueden quedarse cortos en áreas de solidez y escalabilidad cuando se usan en un contexto de servicio. Se requiere una nueva API para solucionar este problema.

## <a name="high-performance-with-maximum-availability"></a>Alto rendimiento con disponibilidad máxima

Direct2D es una biblioteca en modo de usuario que se ha creado mediante la API de Direct3D 10.1. Esto significa que las aplicaciones de Direct2D se benefician de la representación acelerada por hardware en GPU estándar modernas. La aceleración de hardware también se logra en hardware direct3D 9 anterior mediante la representación de Direct3D 10 nivel 9. Esta combinación proporciona un rendimiento excelente en el hardware gráfico en equipos Windows existentes.

> [!Note]  
> A partir Windows 8, Direct2D se ha creado mediante la API de Direct3D 11.1.

 

En el diagrama siguiente se muestra la arquitectura en capas de Direct2D.

![diagrama de la arquitectura en capas de Direct2d](images/direct2d-architectual-layering.png)

En escenarios en los que el uso de la aceleración de hardware no es factible, Direct2D incluye un rasterizador de software de alto rendimiento. Al representar en software, las aplicaciones que usan Direct2D experimentan un rendimiento de representación considerablemente mejor que con GDI+ y con una calidad visual similar. El rasterizador de software también está diseñado para su uso en un contexto de servicio.

El contenido representado mediante Direct2D también se puede mostrar de forma remota mediante la infraestructura de Protocolo de escritorio remoto (RDP) en el sistema operativo Windows 7. Los desarrolladores pueden seleccionar si la representación se controla mediante la GPU en el equipo para mostrar o se representa localmente y se transmite como mapas de bits. Esta opción se puede realizar en función de la tasa de relleno necesaria y la cantidad de primitivas de gráficos que se representan. Cuando el equipo para mostrar ejecuta un sistema operativo anterior a Windows 7, la representación de pantalla remota se realiza mediante la transmisión de mapas de bits a través de la red.

Al proporcionar una única API que combina el rendimiento de Direct3D y la alta disponibilidad al proporcionar reserva de software, escritorio remoto y representación de servicios, Direct2D permite a los desarrolladores tener una única implementación para la representación de alto rendimiento en muchos escenarios diferentes.

## <a name="visual-quality"></a>Calidad visual

Las aplicaciones que usan Direct2D para gráficos pueden ofrecer una mayor calidad visual de la que se puede lograr con GDI. Direct2D usa suavizado de contorno por primitivo para ofrecer curvas y líneas de aspecto más suave en el contenido representado. También hay compatibilidad total con la transparencia y la combinación alfa al representar primitivas 2D. Las imágenes siguientes comparan el contenido con alias representado mediante GDI (a la izquierda) con el contenido suavizado de contorno representado por Direct2D (a la derecha).

![ilustración de curvas y líneas que se representan en gdi y en direct2d](images/rendering-curves-and-lines.png)

Los desarrolladores pueden especificar la representación con alias de gráficos vectoriales. Esto se usa en escenarios en los que se requiere ajustar a límites de píxeles duros, como elementos de la interfaz de usuario como punteros o reglas, si se debe coincidir el estilo GDI de salida, o si el suavizado de contorno se realizará de bajada en el proceso de representación a través del suavizado de contorno multimuestreo o algún otro mecanismo.

## <a name="interoperability"></a>Interoperabilidad

La integración de la representación basada en Direct2D es más fácil para los desarrolladores a través de la interoperabilidad de nivel de superficie con GDI y Direct3D. Las aplicaciones que representan contenido principalmente con GDI, GDI+ o Direct3D, pueden empezar por usar Direct2D para representar áreas específicas de su aplicación y, con el tiempo, pasar a un modelo en el que la representación se realiza principalmente a través de Direct2D, usando GDI principalmente para complementos o extensibilidad heredada.

Direct2D también facilita el [](/windows/desktop/DirectWrite/direct-write-portal) uso de DirectWrite texto de alta calidad y las características avanzadas de creación de imágenes de [Microsoft Windows Imaging Component (WIC).](https://msdn.microsoft.com/library/ms737408.aspx)

Para más información sobre la interoperabilidad de Direct2D, consulte la [sección Interoperabilidad del SDK de Direct2D.](interoperability.md)

## <a name="summary"></a>Resumen

Microsoft Direct2D permite a los desarrolladores crear características de gráficos 2D en sus aplicaciones que ofrecen una calidad visual mejorada a través de GDI y características de rendimiento que se escalan con GPU modernas. El modelo de interoperabilidad de Direct2D permite a los desarrolladores migrar selectivamente partes de su aplicación a la vez junto con la representación basada en GDI, GDI+ o Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicio rápido de Direct2D para Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Introducción a la API de Direct2D](the-direct2d-api.md)
</dt> </dl>

 

 