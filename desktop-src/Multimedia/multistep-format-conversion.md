---
title: Conversión de formato de varios pasos
description: Conversión de formato de varios pasos
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Administrador de compresión de audio (ACM), convertir datos
- ACM (administrador de compresión de audio), convertir datos
- Ejemplos de ACM, conversión de datos
- convertir datos
- Función acmFormatSuggest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370340"
---
# <a name="multistep-format-conversion"></a>Conversión de formato de varios pasos

A veces, el ACM no puede convertir datos de un formato a otro en un solo paso. Por ejemplo, una aplicación podría necesitar convertir datos estéreo de 16 bits y 44 kHz en ADPCM mono de 11 kHz. Si el descomprimidor o el descomprimidor no pueden realizar esta conversión directamente, la aplicación podría intentarla en dos pasos. Esto suele significar realizar una conversión entre dos formatos PCM y, a continuación, otra conversión al tipo de formato final.

Para realizar la conversión en dos pasos, use la función [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) para buscar un formato PCM que coincida con el formato ADPCM. A continuación, use dos secuencias de conversión para realizar la conversión. Por ejemplo, realice una conversión de PCM estéreo de 16 bits, 44 kHz a 16 bits, mono de 11 kHz y, a continuación, convierta de ADPCM mono de 16 bits y 11 kHz mono a 11 kHz.

La conversión de varios pasos también se produce cuando el formato de origen o de destino no es PCM. Si el formato de origen no es PCM, debe cambiarse a un formato PCM antes de la conversión. Si el formato de destino no es PCM, el origen debe convertirse a un formato PCM intermedio y, a continuación, convertirse al formato de destino final.

Las conversiones más sencillas se producen cuando los formatos de origen y destino son formatos PCM. Cuando el formato de origen o destino no es PCM, la conversión puede requerir un paso adicional. Si los formatos de origen y destino no son PCM, la conversión normalmente requerirá más de un paso y, en algunos casos, es posible que la conversión no sea posible.

 

 




