---
description: Introducción a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introducción a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152280"
---
# <a name="introduction-to-directshow"></a>Introducción a DirectShow

Microsoft® DirectShow® es una arquitectura para el streaming de contenido multimedia en la plataforma de® de Microsoft Windows. DirectShow proporciona una captura y reproducción de alta calidad de flujos multimedia. Admite una amplia variedad de formatos, entre los que se incluyen Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio capa 3 (MP3) y archivos de sonido WAV. Admite la captura desde dispositivos digitales y analógicos basados en el Modelo de controlador de Windows (WDM) o vídeo para Windows. Detecta y usa automáticamente hardware de aceleración de vídeo y audio cuando está disponible, pero también admite sistemas sin hardware de aceleración.

DirectShow se basa en el modelo de objetos componentes (COM). Para escribir una aplicación o un componente de DirectShow, debe entender la programación del cliente COM. Para la mayoría de las aplicaciones, no es necesario implementar sus propios objetos COM. DirectShow proporciona los componentes necesarios. Sin embargo, si desea extender DirectShow escribiendo sus propios componentes, debe implementarlos como objetos COM.

DirectShow está diseñado para C++. Microsoft no proporciona una API administrada para DirectShow.

DirectShow simplifica la reproducción multimedia, la conversión de formato y las tareas de captura. Al mismo tiempo, proporciona acceso a la arquitectura de control de flujo subyacente para las aplicaciones que requieren soluciones personalizadas. También puede crear sus propios componentes de DirectShow para admitir nuevos formatos o efectos personalizados.

Algunos ejemplos de los tipos de aplicación que se pueden escribir con DirectShow son reproductores de archivos, reproductores de TV y DVD, aplicaciones de edición de vídeo, convertidores de formato de archivo, aplicaciones de captura de vídeo de audio, codificadores y descodificadores, procesadores de señal digital, etc.

Esta sección contiene los siguientes temas:

-   [Novedades de DirectShow](whats-new-in-directshow.md)
-   [Formatos admitidos en DirectShow](supported-formats-in-directshow.md)
-   [Preguntas más frecuentes sobre DirectShow](directshow-faq.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Usar DirectShow](using-directshow.md)
</dt> </dl>

 

 



