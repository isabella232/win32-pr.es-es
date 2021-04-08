---
title: Control de dispositivo (Windows multimedia)
description: Control de dispositivos
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078749"
---
# <a name="device-control-windows-multimedia"></a><span data-ttu-id="43a4f-103">Control de dispositivo (Windows multimedia)</span><span class="sxs-lookup"><span data-stu-id="43a4f-103">Device Control (Windows Multimedia)</span></span>

<span data-ttu-id="43a4f-104">Para controlar un dispositivo MCI, abra el dispositivo, envíele los comandos necesarios y, a continuación, cierre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="43a4f-104">To control an MCI device, you open the device, send the necessary commands to it, and then close the device.</span></span> <span data-ttu-id="43a4f-105">Los comandos pueden ser muy similares, incluso para dispositivos MCI completamente diferentes.</span><span class="sxs-lookup"><span data-stu-id="43a4f-105">The commands can be very similar, even for completely different MCI devices.</span></span> <span data-ttu-id="43a4f-106">Por ejemplo, la siguiente serie de comandos de MCI reproduce la sexta pista de un CD de audio mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="43a4f-106">For example, the following series of MCI commands plays the sixth track of an audio CD by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="43a4f-107">En el ejemplo siguiente se muestra una serie similar de comandos MCI que desempeñan los primeros 10.000 ejemplos de un archivo de audio de forma de onda:</span><span class="sxs-lookup"><span data-stu-id="43a4f-107">The next example shows a similar series of MCI commands that plays the first 10,000 samples of a waveform-audio file:</span></span>


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="43a4f-108">En estos ejemplos se muestran algunos aspectos interesantes sobre los comandos de MCI:</span><span class="sxs-lookup"><span data-stu-id="43a4f-108">These examples illustrate some interesting facts about MCI commands:</span></span>

-   <span data-ttu-id="43a4f-109">Los mismos comandos básicos ([**abrir**](open.md), [**establecer**](set.md), [**reproducir**](play.md)y [**cerrar**](close.md)) se usan con dispositivos de audio de CD y de onda.</span><span class="sxs-lookup"><span data-stu-id="43a4f-109">The same basic commands ([**open**](open.md), [**set**](set.md), [**play**](play.md), and [**close**](close.md)) are used with CD audio and waveform-audio devices.</span></span> <span data-ttu-id="43a4f-110">Se usan los mismos comandos MCI con todos los dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="43a4f-110">The same MCI commands are used with all MCI devices.</span></span>
-   <span data-ttu-id="43a4f-111">El comando abrir para el dispositivo de audio de onda de onda incluye una especificación de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="43a4f-111">The open command for the waveform-audio device includes a filename specification.</span></span> <span data-ttu-id="43a4f-112">El dispositivo de audio de forma de onda es un *dispositivo compuesto* (uno asociado a un archivo de datos), mientras que el dispositivo de audio de CD es un *dispositivo sencillo* (uno sin un archivo de datos asociado).</span><span class="sxs-lookup"><span data-stu-id="43a4f-112">The waveform-audio device is a *compound device* (one associated with a data file), while the CD audio device is a *simple device* (one without an associated data file).</span></span>
-   <span data-ttu-id="43a4f-113">El comando set especifica los formatos de hora en cada caso, pero la marca de formato de hora para el dispositivo de audio de CD especifica el formato de pista/minutos/segundos/fotogramas (TMSF), mientras que el formato de hora usado con el dispositivo de audio de forma de onda especifica "Samples".</span><span class="sxs-lookup"><span data-stu-id="43a4f-113">The set command specifies time formats in each case, but the time-format flag for the CD audio device specifies tracks/minutes/seconds/frames (TMSF) format, while the time format used with the waveform-audio device specifies "samples".</span></span>
-   <span data-ttu-id="43a4f-114">Las variables que se usan con las marcas "from" y "to" son adecuadas para el formato de hora correspondiente.</span><span class="sxs-lookup"><span data-stu-id="43a4f-114">The variables used with the "from" and "to" flags are appropriate to the respective time format.</span></span> <span data-ttu-id="43a4f-115">Por ejemplo, para el dispositivo de audio de CD, las variables especifican un intervalo de pistas, pero para el dispositivo de audio de onda, las variables especifican un intervalo de muestras.</span><span class="sxs-lookup"><span data-stu-id="43a4f-115">For example, for the CD audio device, the variables specify a range of tracks, but for the waveform-audio device, the variables specify a range of samples.</span></span>

 

 
