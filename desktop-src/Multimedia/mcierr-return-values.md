---
title: Valores devueltos de MCIERR
description: Valores devueltos de MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimedia, valores devueltos de MCIERR
- multimedia, valores devueltos de MCIERR
- referencia multimedia, valores devueltos de MCIERR
- referencia de multimedia, valores devueltos de MCIERR
- Valores devueltos de MCIERR, acerca de
- Función mciSendCommand
- Función mciSendString
- Windows multimedia, errores
- multimedia, errores
- referencia multimedia, errores
- referencia de multimedia, errores
- Interfaz de control multimedia (MCI), valores devueltos de MCIERR
- MCI (interfaz de control multimedia), valores devueltos de MCIERR
- referencia de MCI, valores devueltos de MCIERR
- Referencia de MCI, valores devueltos de MCIERR
- Interfaz de control multimedia (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fc8426b264f68d7a6ab793e365d529774c931e72d89536b40b22592728a2ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783415"
---
# <a name="mcierr-return-values"></a>Valores devueltos de MCIERR

Las [**funciones mciSendCommand**](/previous-versions//dd757160(v=vs.85)) y [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelven cero si se han realizado correctamente; De lo contrario, devuelven un **valor DWORD** que contiene uno de los siguientes valores de error en la palabra baja.

-   [Errores generales de MCI](general-mci-errors.md)
-   [Errores de mciSendString](mcisendstring-errors.md)
-   [Errores de vídeo digital](digital-video-errors.md)
-   [Errores del secuenciador](sequencer-errors.md)
-   [Errores de audio de forma de onda](waveform-audio-errors.md)

Puede obtener una descripción de los valores devueltos individuales pasando los valores devueltos a la [**función mciGetErrorString.**](/previous-versions//dd757158(v=vs.85))

 

 