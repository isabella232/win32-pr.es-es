---
title: Acerca de Direct2D
description: Presenta Direct2D, una API que proporciona a los desarrolladores de Win32 la capacidad de realizar tareas de representación de gráficos en 2D con un rendimiento y una calidad visual superiores.
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D, acerca de
- Direct2D, interoperabilidad
- Direct2D, rendimiento
- Direct2D, disponibilidad
- Direct2D, aplicaciones
- interoperabilidad, Direct2D
- rendimiento de Direct2D
- disponibilidad para Direct2D
- aplicaciones para Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995458"
---
# <a name="about-direct2d"></a>Acerca de Direct2D

En este tema se presenta Direct2D, una API que proporciona a los desarrolladores de Win32 la capacidad de realizar tareas de representación de gráficos en 2D con un rendimiento y una calidad visual superiores.

## <a name="what-is-direct2d"></a>¿Qué es Direct2D?

Direct2D es una API de gráficos 2D de modo inmediato y con aceleración de hardware que proporciona alto rendimiento y representación de alta calidad para geometría 2D, mapas de bits y texto. La API de Direct2D está diseñada para interoperar con el código existente que usa GDI, GDI+ o Direct3D.

Direct2D está diseñado principalmente para su uso por las siguientes clases de desarrolladores:

-   Desarrolladores de aplicaciones nativas grandes y de escala empresarial.
-   Desarrolladores que crean bibliotecas y kits de biblioteca de controles para su uso por parte de desarrolladores de nivel inferior.
-   Desarrolladores que requieren la representación del lado servidor de gráficos 2D.
-   Los desarrolladores que usan gráficos de Direct3D y necesitan una representación de texto, de alto rendimiento y sencilla para menús, elementos de interfaz de usuario (IU) y pantallas de visualización (HUDs).

## <a name="why-direct2d"></a>¿Por qué está Direct2D?

Entre las motivaciones principales para crear una nueva API de gráficos 2D en Microsoft Windows se incluyen las siguientes:

-   Para mantener el ritmo del aumento de la riqueza visual a la que están acostumbrados los usuarios de Windows.
-   Para permitir que los desarrolladores escriban código de representación 2D que se escala directamente con el hardware de procesamiento de gráficos del equipo en el que se está ejecutando.
-   Permite a los desarrolladores escribir código para representar gráficos 2D que se pueden ejecutar en el contexto de un servicio.

En los últimos años, los usuarios finales han empezado a esperar una mayor fidelidad visual en las experiencias digitales. Esta tendencia se refleja en la electrónica del consumidor. Los dispositivos GPS, los dispositivos de reproducción multimedia, los teléfonos móviles y las cámaras digitales ofrecen experiencias continuamente más enriquecidas año tras año. Esta tendencia también puede verse en la diversidad de contenido gráfico en películas, televisores, juegos de vídeo y en la Web. Para seguir el ritmo de estos cambios, se pide a los desarrolladores de forma coherente que realicen sus aplicaciones Windows existentes en el siguiente nivel de riqueza visual.

Los procesadores de gráficos de los equipos modernos de Windows también han evolucionado de forma constante, por avances en gráficos de juegos de vídeo y en partes de la experiencia de Windows, como Windows Media Center y Aero. Algunas aplicaciones de Windows pueden aprovechar las GPU modernas mediante Microsoft Direct3D y Windows Presentation Foundation (WPF). Mientras que Direct3D sirve aplicaciones de gráficos 3D de gama alta y WPF aborda las necesidades de los desarrolladores de .NET, existen huecos para los desarrolladores que tienen grandes códigos base de representación de código basados en GDI e GDI+, o que desean incorporar gráficos 2D de alta calidad en sus aplicaciones basadas en Direct3D.

Por último, la necesidad de una API de gráficos que se puede usar en un servicio se ha convertido en un requisito emergente para los desarrolladores que trabajan en escenarios empresariales y de desarrollo web. Las API de representación existentes se centran en la representación del lado cliente en una sesión de un solo usuario. Como tal, pueden ser breves en áreas de robustez y escalabilidad cuando se usan en un contexto de servicio. Se necesita una nueva API para solucionar este requisito.

## <a name="high-performance-with-maximum-availability"></a>Alto rendimiento con disponibilidad máxima

Direct2D es una biblioteca de modo usuario que se compila mediante la API Direct3D 10,1. Esto significa que las aplicaciones de Direct2D se benefician de la representación con aceleración de hardware en las GPU estándar modernas. La aceleración de hardware también se consigue en el hardware de Direct3D 9 anterior mediante la representación de Direct3D 10-nivel 9. Esta combinación proporciona un rendimiento excelente en el hardware de gráficos de equipos con Windows existentes.

> [!Note]  
> A partir de Windows 8, Direct2D se compila con la API Direct3D 11,1.

 

En el diagrama siguiente se muestra la arquitectura en capas de Direct2D.

![diagrama de la arquitectura en capas de direct2d](images/direct2d-architectual-layering.png)

En los escenarios en los que no es factible el uso de la aceleración de hardware, Direct2D incluye un rasterizador de software de alto rendimiento. Al representarse en el software, las aplicaciones que usan Direct2D experimentan un rendimiento sustancialmente mejor que con GDI+ y con calidad visual similar. El rasterizador de software también está diseñado para su uso en un contexto de servicio.

El contenido que se representa mediante Direct2D también puede mostrarse de forma remota mediante la infraestructura de Protocolo de escritorio remoto (RDP) en el sistema operativo Windows 7. Los desarrolladores pueden seleccionar si la representación se controla mediante la GPU en el equipo de la pantalla o se representa de forma local y se transmite como mapas de bits. Esta opción se puede realizar en función de la velocidad de relleno necesaria y la cantidad de primitivas de gráficos que se representan. Cuando el equipo de pantalla ejecuta un sistema operativo anterior a Windows 7, la representación de pantalla remota se realiza mediante la transmisión de mapas de bits a través de la red.

Al proporcionar una única API que combina el rendimiento de Direct3D y la alta disponibilidad proporcionando la reserva de software, el escritorio remoto y la representación del servicio, Direct2D permite a los desarrolladores tener una única implementación para la representación de alto rendimiento en muchos escenarios diferentes.

## <a name="visual-quality"></a>Calidad visual

Las aplicaciones que usan Direct2D para gráficos pueden ofrecer una calidad visual superior a la que se puede lograr con GDI. Direct2D usa el suavizado de contorno primitivo para ofrecer curvas y líneas de aspecto más suaves en el contenido representado. También hay compatibilidad total para la transparencia y la combinación alfa al representar primitivas 2D. Las siguientes imágenes comparan el contenido con alias representado mediante GDI (a la izquierda) con el contenido con suavizado de contorno representado por Direct2D (a la derecha).

![Ilustración de curvas y líneas que se representan en GDI y en direct2d](images/rendering-curves-and-lines.png)

Los desarrolladores pueden especificar la representación con alias de gráficos vectoriales. Se usa en escenarios en los que es necesario ajustarse a los límites de píxeles rígidos, como los elementos de la interfaz de usuario como los punteros o las reglas, si se debe coincidir con el estilo GDI de la salida, o si el suavizado de contorno se realizará en el proceso de representación mediante el suavizado de contorno de muestreo o algún otro mecanismo.

## <a name="interoperability"></a>Interoperabilidad

La integración de la representación basada en Direct2D es más fácil para los desarrolladores a través de la interoperabilidad de nivel de superficie con GDI y Direct3D. Las aplicaciones que representan contenido principalmente con GDI, GDI+ o Direct3D pueden empezar a usar Direct2D para representar áreas específicas de su aplicación y, con el tiempo, se mueven a un modelo donde la representación se realiza principalmente a través de Direct2D, usando GDI principalmente para complementos o extensibilidad heredada.

Direct2D también facilita el uso de [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) para texto de alta calidad y las características avanzadas de creación de imágenes de [Microsoft Windows Imaging Component (WIC)](https://msdn.microsoft.com/library/ms737408.aspx).

Para obtener más información sobre la interoperabilidad de Direct2D, consulte la [sección interoperabilidad del SDK de direct2d.](interoperability.md)

## <a name="summary"></a>Resumen

Microsoft Direct2D permite a los desarrolladores crear características de gráficos 2D en sus aplicaciones que proporcionan una calidad visual mejorada a través de GDI y características de rendimiento que se escalan con las GPU modernas. El modelo de interoperabilidad de Direct2D permite a los desarrolladores migrar de manera selectiva partes de la aplicación a la vez junto con GDI, GDI+ o la representación basada en Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicio rápido de Direct2D para Windows 8](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[Introducción a la API de Direct2D](the-direct2d-api.md)
</dt> </dl>

 

 