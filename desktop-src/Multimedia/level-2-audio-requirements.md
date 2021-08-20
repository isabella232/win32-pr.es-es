---
title: Requisitos de audio de nivel 2
description: Requisitos de audio de nivel 2
ms.assetid: 203648f2-9d20-438d-975b-b80e50b0fb9b
keywords:
- Equipo multimedia (MPC), nivel 2
- MPC (EQUIPO multimedia), nivel 2
- Consejo de marketing de PC multimedia, nivel 2
- Nivel 2 de MPC, requisitos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a2bc9398a25ac916352f41ad2ddc2325820354d1c7beb511b03b27004fadd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139836"
---
# <a name="level-2-audio-requirements"></a>Requisitos de audio de nivel 2

El subsistema de audio de un equipo que cumple la especificación de nivel 2 incluye los siguientes elementos:

-   Un controlador de CD-ROM con salidas de CD-DA (audio de libro rojo) y control de volumen
-   Una DAC de 16 bits con las siguientes características:
    -   Muestreo de PCM lineal (pulsación de código)
    -   Funcionalidad de transferencia en búfer DMA o FIFO con interrupción en el búfer vacío
    -   Frecuencias de muestreo obligatorias de 44,1, 22,05 y 11,025 kHz
    -   Canales estéreo
    -   Uso de ancho de banda de CPU del 10 por ciento o menos al generar audio de frecuencia de muestreo de 22,05 o 11,025 kHz, o un ancho de banda de CPU del 15 por ciento o menos al generar audio de frecuencia de muestreo de 44,1 kHz

<!-- -->

-   Un ADC de 16 bits con las siguientes características:
    -   Muestreo de PCM lineal
    -   Funcionalidad de transferencia en búfer DMA o FIFO con interrupción en el búfer vacío
    -   Frecuencias de muestreo obligatorias de 44,1, 22,05 y 11,025 kHz
    -   Entrada de micrófono

<!-- -->

-   Funcionalidades internas de síntesis con múltiplesvoices, multitimbral, seis notas simultáneas de la música simultánea más dos notas de percusiones simultáneas
-   Combinación interna con las siguientes funcionalidades:
    -   Puede combinar tres orígenes de audio y presentar la salida como una señal de audio estéreo de nivel de línea en el panel posterior.
    -   Los orígenes de mezcla son el audio del libro rojo de CD, el sintetizador y la DAC
    -   Cada origen de mezcla tiene un control de volumen de 3 bits con un taper logarítmico

 

 




