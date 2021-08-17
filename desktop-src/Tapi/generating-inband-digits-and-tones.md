---
description: Una vez que una llamada está en estado conectado, se puede transmitir información a través de ella.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Generación de dígitos y tonos de banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f144d4bc6b6273f71da37f6b9864146465c5ca29b91018a2e2ff097f6f19b44f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424885"
---
# <a name="generating-inband-digits-and-tones"></a>Generación de dígitos y tonos de banda

Una vez que una llamada está *en estado conectado,* se puede transmitir información a través de ella. Se proporcionan dos funciones que permiten la señalización de inband de un extremo a otro entre la aplicación y el equipo de la estación remota, como un equipo de respuesta. Una función es [**lineGenerateDigits,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)que genera dígitos inband en una llamada, señalándolos a través del canal de voz. Los dígitos se pueden señalar como secuencias de pulsación/pulsación o como tonos DTMF. La otra función es [**lineGenerateTone,**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)que permite a la aplicación generar uno de los diversos tonos de multifrecuencia inband (a través de la secuencia multimedia). Esto genera tonos de telefonía, como ringback, beep y busy, así como tonalidades arbitrarias multifrecuencia y multicadencia.

Solo un dígito o generación de tono puede estar en curso en una llamada en cualquier momento. Cuando se completa la generación de dígitos o tono, se envía un mensaje [**\_ LINE GENERATE**](line-generate.md) a la aplicación que solicitó la generación. En el caso de que se generen varios dígitos, solo se enviará un único mensaje una vez generados todos los dígitos. La llamada a [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) o [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) mientras la generación de dígitos o tono está en curso anulará la generación actualmente en curso y enviará el mensaje LINE GENERATE a la aplicación cuya generación se anuló con una indicación de cancelación. \_

 

 



