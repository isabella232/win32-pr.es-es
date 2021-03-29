---
title: Comportamiento predeterminado de los controladores
description: Comportamiento predeterminado de los controladores
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791073"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="fdd8b-103">Comportamiento predeterminado de los controladores</span><span class="sxs-lookup"><span data-stu-id="fdd8b-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="fdd8b-104">En muchas situaciones, las especificaciones del comando MCI definen los valores predeterminados y el comportamiento de los controladores de un tipo de dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="fdd8b-105">Dado que los dispositivos multimedia pueden tener una amplia gama de características (y limitaciones), puede haber áreas de comportamiento sin definir.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="fdd8b-106">Además, los controladores pueden controlar las excepciones de manera diferente, en función de las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="fdd8b-107">Por ejemplo, considere los siguientes comandos que se envían a un controlador de audio de una onda mediante la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :</span><span class="sxs-lookup"><span data-stu-id="fdd8b-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="fdd8b-108">El comando [**Record**](record.md) devuelve un valor "parámetro fuera del intervalo" y detiene la reproducción iniciada por el comando [**Play**](play.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="fdd8b-109">Podría esperar que el controlador validara el comando de registro antes de detener la reproducción, pero el controlador detiene primero la reproducción.</span><span class="sxs-lookup"><span data-stu-id="fdd8b-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 