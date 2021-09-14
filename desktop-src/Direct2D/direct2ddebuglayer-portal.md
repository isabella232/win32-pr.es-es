---
title: Capa de depuración de Direct2D
description: Una extensión en tiempo de ejecución para Direct2D que ofrece mensajes de error descriptivos, detección de pérdida de objetos, avisos de rendimiento y otras indicaciones para ayudarle a crear aplicaciones de Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163334"
---
# <a name="direct2d-debug-layer"></a>Capa de depuración de Direct2D

## <a name="purpose"></a>Propósito

La capa de depuración de Direct2D, implementada por separado de Direct2D en su propio archivo DLL denominado d2d1debug.dll, proporciona mensajes de depuración en tiempo de diseño para minimizar el error de la aplicación en tiempo de ejecución. Los mensajes de depuración suelen ser el resultado de infracciones de contratos de API, como parámetros no válidos (podrían estar relacionados con Direct3D), recursos no válidos, infracciones de subprocesos y otros problemas de rendimiento, como el uso de una capa cuando bastaría con un clip.

Para ayudarle a decidir cuánta información se sigue por la capa de depuración, la capa de depuración ofrece tres niveles de depuración: información, advertencia y error. Estos tres niveles se interpretan de la manera siguiente:

-   **Error:** Direct2D envía mensajes de error graves a la capa de depuración. Por ejemplo, la separación de una restricción de subprocesos generará un error grave.

    Además, un mensaje de error de nivel desencadena el punto de interrupción para ayudarle a depurar.

-   **Advertencia:** Direct2D envía mensajes de error y advertencias a la capa de depuración para que pueda abordar cualquiera de estos mensajes.

-   **Información:** Direct2D envía mensajes de error, advertencias e información de diagnóstico adicional a la capa de depuración. Por ejemplo, los mensajes de mejora del rendimiento se enviarán en este nivel de depuración.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Instalación de la capa de depuración de Direct2D](installing-the-direct2d-debug-layer.md)<br/> | Describe cómo instalar la capa de depuración de Direct2D.<br/>      |
| [Introducción a la capa de depuración de Direct2D](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [Depurar mensajes](direct2ddebuglayer-debugmessages.md)<br/>                         | Enumera los mensajes de depuración de la capa de depuración de Direct2D.<br/> |



 

 

 





