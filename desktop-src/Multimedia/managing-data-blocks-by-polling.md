---
title: Administración de bloques de datos mediante sondeo
description: Administración de bloques de datos mediante sondeo
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- audio de forma de onda, bloques de datos de sondeo
- bloques de datos de audio, sondeo
- sondear bloques de datos de audio
- Estructura WAVEHDR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173653"
---
# <a name="managing-data-blocks-by-polling"></a>Administración de bloques de datos mediante sondeo

Además de usar una función de devolución de llamada, puede sondear el miembro **dwFlags** de una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) para determinar cuándo finaliza un dispositivo de audio con un bloque de datos. A veces es mejor sondear **dwFlags** que esperar a que otro mecanismo reciba mensajes de los controladores. Por ejemplo, después de llamar a la función [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) para liberar bloques de datos pendientes, puede sondear inmediatamente para asegurarse de que los bloques de datos se han liberado antes de llamar a [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) y liberar la memoria del bloque de datos.

Puede usar la marca WHDR \_ DONE para probar el miembro **dwFlags.** En cuanto se establece la marca WHDR DONE en el miembro dwFlags de la estructura \_ **WAVEHDR,** el controlador  finaliza con el bloque de datos.

 

 