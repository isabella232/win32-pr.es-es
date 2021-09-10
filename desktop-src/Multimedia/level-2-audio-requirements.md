---
title: Requisitos de audio de nivel 2
description: Requisitos de audio de nivel 2
ms.assetid: 203648f2-9d20-438d-975b-b80e50b0fb9b
keywords:
- Equipo multimedia (MPC), nivel 2
- MPC (Equipo multimedia), nivel 2
- Consejo de marketing de PC multimedia, nivel 2
- MPC nivel 2, requisitos de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20458f8dcb26149c9fa697587faf93cf10c0f27
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372320"
---
# <a name="level-2-audio-requirements"></a>Requisitos de audio de nivel 2

El subsistema de audio de un equipo que cumple la especificación de nivel 2 incluye los siguientes elementos:

-   Un controlador de CD-ROM con salidas de CD-DA (audio de libro rojo) y control de volumen
-   Una DAC de 16 bits con las siguientes características:
    -   Muestreo de PCM lineal (pulsación de código)
    -   Funcionalidad de transferencia en búfer de DMA o FIFO con interrupción en el búfer vacío
    -   Velocidades de muestreo obligatorias de 44,1, 22,05 y 11,025 kHz
    -   Canales estéreo
    -   Uso de ancho de banda de CPU del 10 % o menos al generar audio de una frecuencia de muestreo de 22,05 o 11,025 kHz, o un ancho de banda de CPU del 15 % o menos al generar audio de 44,1 kHz de frecuencia de muestreo

<!-- -->

-   Un ADC de 16 bits con las siguientes características:
    -   Muestreo de PCM lineal
    -   Funcionalidad de transferencia en búfer de DMA o FIFO con interrupción en el búfer vacío
    -   Velocidades de muestreo obligatorias de 44,1, 22,05 y 11,025 kHz
    -   Entrada de micrófono

<!-- -->

-   Funcionalidades de síntesis interna con múltiplesvoices, multitimbrales, seis notas simultáneas de la música simultánea, además de dos notas de percusión simultáneas
-   Combinación interna con las siguientes funcionalidades:
    -   Puede combinar tres orígenes de audio y presentar la salida como una señal de audio estéreo de nivel de línea en el panel posterior.
    -   Los orígenes de mezcla son audio, síntesis y DAC de CD Red Book
    -   Cada origen de mezcla tiene un control de volumen de 3 bits con un taper logarítmico.

 

 




