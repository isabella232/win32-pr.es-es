---
description: Introducción a DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introducción a DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cd4dc2a75233c519c4ca3d5db213451b097c0528ab782109da611b6e35aca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952584"
---
# <a name="introduction-to-directshow"></a>Introducción a DirectShow

Microsoft® DirectShow® es una arquitectura para los medios de streaming en la plataforma Windows® Microsoft. DirectShow proporciona captura y reproducción de alta calidad de secuencias multimedia. Admite una amplia variedad de formatos, incluidos Advanced Systems Format (ASF), Motion Picture Experts Group (MPEG), Audio-Video Interleaved (AVI), MPEG Audio Layer-3 (MP3) y archivos de sonido WAV. Admite la captura desde dispositivos digitales y análogos basados en Windows Driver Model (WDM) o Video para Windows. Detecta y usa automáticamente hardware de aceleración de vídeo y audio cuando está disponible, pero también admite sistemas sin hardware de aceleración.

DirectShow se basa en el modelo de objetos componentes (COM). Para escribir una DirectShow o componente, debe comprender la programación del cliente COM. Para la mayoría de las aplicaciones, no es necesario implementar sus propios objetos COM. DirectShow proporciona los componentes que necesita. Sin embargo, si desea ampliar DirectShow escribir sus propios componentes, debe implementarlos como objetos COM.

DirectShow está diseñado para C++. Microsoft no proporciona una API administrada para DirectShow.

DirectShow simplifica la reproducción multimedia, la conversión de formato y las tareas de captura. Al mismo tiempo, proporciona acceso a la arquitectura de control de flujo subyacente para las aplicaciones que requieren soluciones personalizadas. También puede crear sus propios componentes de DirectShow para admitir nuevos formatos o efectos personalizados.

Entre los ejemplos de los tipos de aplicación que puede escribir con DirectShow se incluyen reproductores de archivos, reproductores de TV y DVD, aplicaciones de edición de vídeo, convertidores de formato de archivo, aplicaciones de captura de audio y vídeo, codificadores y descodificadores, procesadores de señales digitales, etc.

Esta sección contiene los siguientes temas:

-   [Novedades de DirectShow](whats-new-in-directshow.md)
-   [Formatos admitidos en DirectShow](supported-formats-in-directshow.md)
-   [DirectShow Preguntas más frecuentes](directshow-faq.yml)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> <dt>

[Uso de DirectShow](using-directshow.md)
</dt> </dl>

 

 



