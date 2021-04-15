---
description: Una vez que una llamada está en estado conectado, se puede transmitir información sobre ella.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Generar dígitos y tonos en banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677324"
---
# <a name="generating-inband-digits-and-tones"></a>Generar dígitos y tonos en banda

Una vez que una llamada está en estado *conectado* , se puede transmitir información sobre ella. Se proporcionan dos funciones que permiten la señalización en banda de un extremo a otro entre la aplicación y el equipo de la estación remota, como una máquina de respuesta. Una función es [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), que genera dígitos en banda en una llamada y los señala a través del canal de voz. Los dígitos se pueden señalizar como secuencias giratorias/pulsos o como tonos DTMF. La otra función es [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), lo que permite que la aplicación genere una de una variedad de tonalidades de varias frecuencias (en el flujo multimedia). Esto genera tonos de telefonía, como timbre, bip y Busy, así como tonos de frecuencias multifrecuencia arbitrarios.

Solo puede haber una generación de dígitos o de tono en curso en una llamada en cualquier momento. Cuando se completa la generación de dígitos o tono, se envía un mensaje de generación de [**línea \_**](line-generate.md) a la aplicación que solicitó la generación. En el caso de que se generen varios dígitos, solo se devolverá un mensaje una vez que se hayan generado todos los dígitos. La llamada a [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) o [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) mientras la generación de dígitos o de tono está en curso anulará la generación actualmente en curso y enviará el mensaje de generación de línea \_ a la aplicación cuya generación se anuló con una indicación de cancelación.

 

 



