---
title: Trabajar con recursos de streaming
description: Trabajar con recursos de streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Reproductor de Windows Media complementos, recursos de streaming de ejemplo de eco
- complementos, recursos de streaming de ejemplo de eco
- complementos de procesamiento de señales digitales, recursos de streaming de ejemplo de eco
- Complementos de DSP, recursos de streaming de ejemplo de eco
- Ejemplo de complemento DSP de eco, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1df8cc221f3d75c8333b3ffd41a144d28bed7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467336"
---
# <a name="working-with-streaming-resources"></a>Trabajar con recursos de streaming

El proyecto de complemento DSP de audio de ejemplo generado por el Asistente para complemento de Reproductor de Windows Media no requiere que el complemento asigne ningún recurso de streaming. Sin embargo, el ejemplo de eco requiere un búfer independiente para contener los datos de audio durante un período de tiempo para crear el efecto de retraso. El búfer se administra mediante dos métodos: **IMediaObject::AllocateStreamingResources**, que crea el búfer, e **IMediaObject::FreeStreamingResources**, que libera el búfer. Los **métodos IMediaObject** se implementan en Echo.cpp.

En las secciones siguientes se proporciona más información sobre cómo administrar los búferes:

-   [Variables para administrar el búfer de retraso](variables-to-manage-the-delay-buffer.md)
-   [Implementación de IMediaObject::AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementación de IMediaObject::FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo de eco**](the-echo-sample.md)
</dt> </dl>

 

 




