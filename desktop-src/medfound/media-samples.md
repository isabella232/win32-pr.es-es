---
description: Ejemplos de medios
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Ejemplos de medios (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003383"
---
# <a name="media-samples-microsoft-media-foundation"></a>Ejemplos de medios (Microsoft Media Foundation)

Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes. Los ejemplos de medios exponen la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) . La cantidad de datos contenida en una muestra depende del componente que crea el ejemplo y del tipo de datos de los búferes. En el caso de los vídeos sin comprimir, un ejemplo suele contener un único fotograma de vídeo. En el caso de audio sin comprimir, la cantidad de datos puede variar, pero normalmente una trama de audio no abarca dos ejemplos. En el caso de los datos comprimidos, es posible que estas instrucciones no se apliquen.

Un único ejemplo puede contener varios búferes por motivos de eficacia. Por ejemplo, en un archivo ASF, a menudo se distribuye un fotograma de vídeo entre varios paquetes ASF. El origen multimedia podría leer los paquetes en varios búferes. En lugar de copiar cada fragmento en un búfer, el origen simplemente coloca todos los búferes en un ejemplo. Los componentes de nivel inferior pueden decidir después si se copian los búferes más pequeños en un búfer contiguo. Por lo general, si está escribiendo un componente de canalización, debe suponer que cualquier ejemplo puede contener más de un búfer.

Esta sección contiene los temas siguientes.



| Tema                                                        | Descripción                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Trabajar con ejemplos de medios](working-with-media-samples.md) | Describe el comportamiento general de los ejemplos de medios.                                                                         |
| [Ejemplos de vídeo](video-samples.md)                           | Describe una implementación especializada de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) diseñada para contener fotogramas de vídeo sin comprimir. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes multimedia](media-buffers.md)
</dt> <dt>

[Media Foundation primitivas](media-foundation-primitives.md)
</dt> </dl>

 

 



