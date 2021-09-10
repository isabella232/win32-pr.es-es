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
ms.openlocfilehash: c148c075df09cb702caf6b1d192fe8ce41b48ad0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370357"
---
# <a name="finding-a-specific-format"></a>Buscar un formato específico

Una aplicación podría tener solo una especificación parcial para un formato cuando necesita la especificación completa. Por ejemplo, la especificación podría estipular un formato ADPCM mono de 11 kHz, de 4 bits, pero no el promedio de bytes por segundo. La aplicación puede obtener el formato completo sin intervención del usuario mediante la función [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum) y especificando marcas en el *parámetro fdwEnum.*

 

 




