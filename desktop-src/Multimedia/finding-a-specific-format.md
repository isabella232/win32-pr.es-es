---
title: Buscar un formato específico
description: Buscar un formato específico
ms.assetid: 0c892758-d409-4ed7-8f38-a24eee646b65
keywords:
- Administrador de compresión de audio (ACM), buscar formatos
- ACM (administrador de compresión de audio), buscar formatos
- Ejemplos de ACM, buscar formatos
- buscar formatos
- Función acmFormatEnum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc291a6dff0c6b2befec6afd001a32735a54e95fd65a464378adb690a95019c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691535"
---
# <a name="finding-a-specific-format"></a>Buscar un formato específico

Una aplicación podría tener solo una especificación parcial para un formato cuando necesita la especificación completa. Por ejemplo, la especificación podría estipular un formato ADPCM mono de 11 kHz de 4 bits, pero no el promedio de bytes por segundo. La aplicación puede obtener el formato completo sin intervención del usuario mediante la función [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) y especificando marcas en el *parámetro fdwEnum.*

 

 




