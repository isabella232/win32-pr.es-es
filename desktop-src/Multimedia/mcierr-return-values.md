---
title: Valores devueltos de MCIERR
description: Valores devueltos de MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimedia, valores devueltos de MCIERR
- multimedia, valores devueltos de MCIERR
- referencia multimedia, valores devueltos de MCIERR
- referencia para multimedia, valores devueltos de MCIERR
- Valores devueltos de MCIERR, acerca de
- mciSendCommand función)
- mciSendString función)
- Windows multimedia, errores
- multimedia, errores
- referencia multimedia, errores
- referencia de multimedia, errores
- Media control Interface (MCI), valores devueltos de MCIERR
- MCI (media control Interface), valores devueltos de MCIERR
- referencia de MCI, valores devueltos de MCIERR
- Referencia de MCI, valores devueltos de MCIERR
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676365"
---
# <a name="mcierr-return-values"></a>Valores devueltos de MCIERR

Las funciones [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) y [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelven cero si son correctas; de lo contrario, devuelven un valor **DWORD** que contiene uno de los siguientes valores de error en la palabra baja.

-   [Errores generales de MCI](general-mci-errors.md)
-   [Errores de mciSendString](mcisendstring-errors.md)
-   [Errores de vídeo digital](digital-video-errors.md)
-   [Errores del secuenciador](sequencer-errors.md)
-   [Onda-errores de audio](waveform-audio-errors.md)

Puede obtener una descripción de los valores devueltos individuales pasando los valores devueltos a la función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .

 

 