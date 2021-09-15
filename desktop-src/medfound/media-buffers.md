---
description: Búferes multimedia
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Búferes multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579937"
---
# <a name="media-buffers"></a>Búferes multimedia

Un búfer multimedia es un objeto COM que administra un bloque de memoria, normalmente para contener datos multimedia. Los búferes multimedia se usan para mover datos de un componente de canalización al siguiente. La mayoría de las aplicaciones no usan búferes multimedia directamente, ya que la sesión multimedia controla todo el flujo de datos entre objetos de canalización. Debe usar búferes multimedia si está escribiendo su propio componente de canalización o si usa un componente de canalización directamente sin la sesión multimedia.

Los búferes multimedia exponen la [**interfaz IMFMediaBuffer.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) Esta interfaz está diseñada para leer o escribir cualquier tipo de datos. Los fotogramas de vídeo sin comprimir requieren un control especial, ya que podrían almacenarse en superficies de Direct3D ubicadas en la memoria de vídeo.

Esta sección contiene los temas siguientes.



| Tema                                                        | Descripción                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [Trabajar con búferes multimedia](working-with-media-buffers.md) | Describe el comportamiento general de los búferes multimedia para todos los tipos de medios. |
| [Búferes de vídeo sin comprimir](uncompressed-video-buffers.md) | Cómo trabajar con búferes multimedia que contienen fotogramas de vídeo sin comprimir.  |
| [Búfer de superficie de DirectX](directx-surface-buffer.md)         | Describe cómo almacenar una superficie de Direct3D en un búfer multimedia.         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation primitivos](media-foundation-primitives.md)
</dt> </dl>

 

 



