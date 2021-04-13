---
title: Capa de depuración de Direct2D
description: Una extensión en tiempo de ejecución para Direct2D que ofrece mensajes de error descriptivos, detección de fugas de objetos, avisos de rendimiento y otras indicaciones para ayudarle a crear aplicaciones de Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418439"
---
# <a name="direct2d-debug-layer"></a>Capa de depuración de Direct2D

## <a name="purpose"></a>Propósito

La capa de depuración de Direct2D, implementada de forma independiente de Direct2D en su propio archivo DLL denominado d2d1debug.dll, proporciona mensajes de depuración en tiempo de diseño para que pueda minimizar el error de aplicación en tiempo de ejecución. Los mensajes de depuración se suelen producir a causa de infracciones de contratos de API, como parámetros no válidos (pueden estar relacionados con Direct3D), recursos no válidos, infracciones de subprocesos y otros problemas de rendimiento, como el uso de una capa cuando un clip sería suficiente.

Para ayudarle a decidir la cantidad de información de la que se realiza el seguimiento por la capa de depuración, la capa de depuración ofrece tres niveles de depuración: información, ADVERTENCIA y error. Estos tres niveles se interpretan de la siguiente manera:

-   **Error:** Direct2D envía mensajes de error graves a la capa de depuración. Por ejemplo, si se interrumpe una restricción de subproceso, se producirá un error grave.

    Además, un mensaje de error de nivel desencadena el punto de interrupción para ayudarle a depurar.

-   **ADVERTENCIA:** Direct2D envía mensajes de error y advertencias a la capa de depuración para que pueda tratar cualquiera de estos mensajes.

-   **Información:** Direct2D envía mensajes de error, advertencias e información de diagnóstico adicional a la capa de depuración. Por ejemplo, los mensajes de mejora del rendimiento se enviarán en este nivel de depuración.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Instalar la capa de depuración de Direct2D](installing-the-direct2d-debug-layer.md)<br/> | Describe cómo instalar la capa de depuración de Direct2D.<br/>      |
| [Introducción a la capa de depuración de Direct2D](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Depurar mensajes](direct2ddebuglayer-debugmessages.md)<br/>                         | Enumera los mensajes de depuración de la capa de depuración de Direct2D.<br/> |



 

 

 





