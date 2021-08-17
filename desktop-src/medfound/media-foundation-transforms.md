---
description: Media Foundation transformaciones
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61057831383c808a3e05cbe2e9cd779b46522a7a3d52d379b936f27c549d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268705"
---
# <a name="media-foundation-transforms"></a>Media Foundation transformaciones

Media Foundation transformaciones (MFT) proporcionan un modelo genérico para procesar datos multimedia. Las MFT se usan para descodificadores, codificadores y procesadores de señales digitales (DSP). En resumen, todo lo que se encuentra en la canalización de medios entre el origen de medios y el receptor de medios es un MFT.

En esta sección se describe el modelo de programación de MFT y cómo implementar un MFT, con recomendaciones para tipos específicos de MFT, como descodificadores.



| Tema                                                                    | Descripción                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de las MTA](about-mfts.md)                                             | Proporciona una breve introducción a las MTA.                                                                                                                                                                   |
| [Modelo básico de procesamiento de MFT](basic-mft-processing-model.md)             | Describe con más detalle el modelo básico para procesar datos con un MFT.                                                                                                                           |
| [MFT asincrónicas](asynchronous-mfts.md)                               | Describe un modelo de procesamiento asincrónico que es una alternativa al modelo básico.<br/> El procesamiento asincrónico se introdujo en Windows 7. No todos los MFT admiten este modelo.<br/> |
| [Registro y enumeración de MTA](registering-and-enumerating-mfts.md) | Cómo registrar un MFT y cómo enumerar las MFT en el registro.                                                                                                                                   |
| [Restricciones de campo de uso](field-of-use-restrictions.md)               | Describe el mecanismo para desbloquear un MFT que tiene restricciones de campo de uso.                                                                                                                    |
| [Comparación de MFT y DMO](comparison-of-mfts-and-dmos.md)           | Resume las diferencias entre las MTO y las DMA.                                                                                                                                                   |
| [Escribir un MFT personalizado](writing-a-custom-mft.md)                         | Directrices para escribir un MFT personalizado.                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation canalización](media-foundation-pipeline.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




