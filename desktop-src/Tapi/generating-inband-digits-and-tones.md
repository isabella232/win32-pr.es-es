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
# <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="da11e-103">Generar dígitos y tonos en banda</span><span class="sxs-lookup"><span data-stu-id="da11e-103">Generating Inband Digits and Tones</span></span>

<span data-ttu-id="da11e-104">Una vez que una llamada está en estado *conectado* , se puede transmitir información sobre ella.</span><span class="sxs-lookup"><span data-stu-id="da11e-104">After a call is in the *connected* state, information can be transmitted over it.</span></span> <span data-ttu-id="da11e-105">Se proporcionan dos funciones que permiten la señalización en banda de un extremo a otro entre la aplicación y el equipo de la estación remota, como una máquina de respuesta.</span><span class="sxs-lookup"><span data-stu-id="da11e-105">Two functions are provided that allow end-to-end inband signaling between the application and remote station equipment such as an answering machine.</span></span> <span data-ttu-id="da11e-106">Una función es [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), que genera dígitos en banda en una llamada y los señala a través del canal de voz.</span><span class="sxs-lookup"><span data-stu-id="da11e-106">One function is [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), which generates inband digits on a call, signaling them over the voice channel.</span></span> <span data-ttu-id="da11e-107">Los dígitos se pueden señalizar como secuencias giratorias/pulsos o como tonos DTMF.</span><span class="sxs-lookup"><span data-stu-id="da11e-107">Digits can be signaled as either rotary/pulse sequences or as DTMF tones.</span></span> <span data-ttu-id="da11e-108">La otra función es [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), lo que permite que la aplicación genere una de una variedad de tonalidades de varias frecuencias (en el flujo multimedia).</span><span class="sxs-lookup"><span data-stu-id="da11e-108">The other function is [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), which enables the application to generate one of a variety of multifrequency tones inband (over the media stream).</span></span> <span data-ttu-id="da11e-109">Esto genera tonos de telefonía, como timbre, bip y Busy, así como tonos de frecuencias multifrecuencia arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="da11e-109">This generates telephony tones, such as ringback, beep, and busy, as well as arbitrary multifrequency, multicadenced tones.</span></span>

<span data-ttu-id="da11e-110">Solo puede haber una generación de dígitos o de tono en curso en una llamada en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="da11e-110">Only one digit or tone generation can be in progress on a call at any one time.</span></span> <span data-ttu-id="da11e-111">Cuando se completa la generación de dígitos o tono, se envía un mensaje de generación de [**línea \_**](line-generate.md) a la aplicación que solicitó la generación.</span><span class="sxs-lookup"><span data-stu-id="da11e-111">When digit or tone generation completes, a [**LINE\_GENERATE**](line-generate.md) message is sent to the application that requested the generation.</span></span> <span data-ttu-id="da11e-112">En el caso de que se generen varios dígitos, solo se devolverá un mensaje una vez que se hayan generado todos los dígitos.</span><span class="sxs-lookup"><span data-stu-id="da11e-112">In the case where multiple digits are generated, only a single message is sent back after all digits have been generated.</span></span> <span data-ttu-id="da11e-113">La llamada a [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) o [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) mientras la generación de dígitos o de tono está en curso anulará la generación actualmente en curso y enviará el mensaje de generación de línea \_ a la aplicación cuya generación se anuló con una indicación de cancelación.</span><span class="sxs-lookup"><span data-stu-id="da11e-113">Calling [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) or [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) while digit or tone generation is in progress will abort the generation currently in progress and send the LINE\_GENERATE message to the application whose generation was aborted with a cancel indication.</span></span>

 

 



