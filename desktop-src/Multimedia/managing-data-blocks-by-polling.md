---
title: Administrar bloques de datos mediante sondeo
description: Administrar bloques de datos mediante sondeo
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- audio de onda, bloqueos de datos de sondeo
- bloques de datos de audio, sondeo
- sondear bloques de datos de audio
- Estructura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077613"
---
# <a name="managing-data-blocks-by-polling"></a>Administrar bloques de datos mediante sondeo

Además de usar una función de devolución de llamada, puede sondear el miembro **dwFlags** de una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para determinar cuándo ha finalizado un dispositivo de audio con un bloque de datos. A veces es mejor sondear **dwFlags** que esperar a que otro mecanismo reciba mensajes de los controladores. Por ejemplo, después de llamar a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) para liberar bloques de datos pendientes, puede sondear inmediatamente para asegurarse de que se han liberado los bloques de datos antes de llamar a [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) y liberar memoria para el bloque de datos.

Puede usar la marca WHDR \_ Done para probar el miembro **dwFlags** . \_En cuanto se establece la marca WHDR done en el miembro **dwFlags** de la estructura **WAVEHDR** , el controlador finaliza con el bloque de datos.

 

 