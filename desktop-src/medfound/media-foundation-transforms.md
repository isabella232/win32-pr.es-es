---
description: Media Foundation transformaciones
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Media Foundation transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707565"
---
# <a name="media-foundation-transforms"></a>Media Foundation transformaciones

Media Foundation transformaciones (MFTs) proporcionan un modelo genérico para procesar los datos multimedia. MFTs se usan para descodificadores, codificadores y procesadores de señal digital (DSP). En Resumen, todo lo que se encuentra en la canalización multimedia entre el origen multimedia y el receptor multimedia es un MFT.

En esta sección se describe el modelo de programación de MFT y cómo implementar una MFT, con recomendaciones para tipos específicos de MFTs, como descodificadores.



| Tema                                                                    | Descripción                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de MFTs](about-mfts.md)                                             | Proporciona una breve introducción a MFTs                                                                                                                                                                   |
| [Modelo básico de procesamiento de MFT](basic-mft-processing-model.md)             | Describe con más detalle el modelo básico de procesamiento de datos con una MFT.                                                                                                                           |
| [MFTs asincrónico](asynchronous-mfts.md)                               | Describe un modelo de procesamiento asincrónico que es una alternativa al modelo básico.<br/> El procesamiento asincrónico se presentó en Windows 7. No todos los MFT admiten este modelo.<br/> |
| [Registro y enumeración de MFTs](registering-and-enumerating-mfts.md) | Cómo registrar una MFT y cómo enumerar MFTs en el registro.                                                                                                                                   |
| [Campo de restricciones de uso](field-of-use-restrictions.md)               | Describe el mecanismo para desbloquear una MFT que tiene restricciones de campo de uso.                                                                                                                    |
| [Comparación de MFT y DMO](comparison-of-mfts-and-dmos.md)           | Resume las diferencias entre MFTs y DMOs.                                                                                                                                                   |
| [Escribir una MFT personalizada](writing-a-custom-mft.md)                         | Instrucciones para escribir un MFT personalizado.                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




