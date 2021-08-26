---
description: Obtenga información sobre los ejemplos de medios en Microsoft Media Foundation. Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Ejemplos de medios (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83bad0186d54d99b6c7f7666a5971f6c35e8e2a561109e7bfd6afd45fd5f5e6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061075"
---
# <a name="media-samples-microsoft-media-foundation"></a>Ejemplos de medios (Microsoft Media Foundation)

Un ejemplo multimedia es un objeto que contiene una lista ordenada de cero o más búferes. Los ejemplos de medios exponen la [**interfaz DESAMPLESample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) La cantidad de datos contenidos en una muestra depende del componente que crea la muestra y del tipo de datos de los búferes. En el caso del vídeo sin comprimir, un ejemplo suele contener un único fotograma de vídeo. En el caso del audio sin comprimir, la cantidad de datos puede variar, pero normalmente un fotograma de audio no abarca dos muestras. En el caso de los datos comprimidos, es posible que estas directrices no se apliquen.

Una sola muestra puede contener varios búferes por motivos de eficiencia. Por ejemplo, en un archivo ASF, un fotograma de vídeo a menudo se distribuye entre varios paquetes ASF. El origen de medios podría leer los paquetes en varios búferes. En lugar de copiar cada fragmento en un búfer, el origen simplemente coloca todos los búferes en una muestra. Los componentes de nivel inferior pueden decidir si se copian los búferes más pequeños en un búfer contiguo. Por lo general, si está escribiendo un componente de canalización, debe suponer que cualquier ejemplo puede contener más de un búfer.

Esta sección contiene los temas siguientes.



| Tema                                                        | Descripción                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Trabajar con ejemplos multimedia](working-with-media-samples.md) | Describe el comportamiento general de los ejemplos multimedia.                                                                         |
| [Ejemplos de vídeo](video-samples.md)                           | Describe una implementación especializada [**deSAMPLESample diseñada**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para contener fotogramas de vídeo sin comprimir. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes multimedia](media-buffers.md)
</dt> <dt>

[Media Foundation primitivos](media-foundation-primitives.md)
</dt> </dl>

 

 



