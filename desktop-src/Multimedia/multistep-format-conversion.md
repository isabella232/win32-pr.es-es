---
title: Conversión de formato multipaso
description: Conversión de formato multipaso
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Administrador de compresión de audio (ACM), convertir datos
- ACM (Administrador de compresión de audio), convertir datos
- Ejemplos de ACM, convertir datos
- convertir datos
- acmFormatSuggest función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994284"
---
# <a name="multistep-format-conversion"></a>Conversión de formato multipaso

A veces, el ACM no puede convertir datos de un formato a otro en un solo paso. Por ejemplo, es posible que una aplicación necesite convertir datos estéreo de 16 bits de 44 kHz a un ADPCM mono de 11 kHz. Si el compresor o el descompresor no pueden realizar esta conversión directamente, es posible que la aplicación la intente en dos pasos. Normalmente, esto significa hacer una conversión entre dos formatos PCM y, a continuación, otra conversión al tipo de formato final.

Para realizar la conversión en dos pasos, utilice la función [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) para buscar un formato PCM que coincida con el formato ADPCM. A continuación, use dos flujos de conversión para realizar la conversión. Por ejemplo, realice una conversión del PCM estéreo de 16 bits 44-kHz a mono de 16 bits, de 11 kHz, y, a continuación, convierta de 16 bits a un ADPCM mono a 11 kHz.

La conversión en un solo paso también se produce cuando el formato de origen o de destino no es PCM. Si el formato de origen no es PCM, debe cambiarse a un formato PCM antes de la conversión. Si el formato de destino no es PCM, el origen debe convertirse a un formato PCM intermedio y, a continuación, convertirse al formato de destino final.

Las conversiones más directas se producen cuando los formatos de origen y destino son ambos formatos PCM. Cuando el formato de origen o destino no es PCM, la conversión podría requerir un paso adicional. Si los formatos de origen y destino no son PCM, la conversión normalmente requerirá más de un paso y, en algunos casos, la conversión podría no ser posible.

 

 




