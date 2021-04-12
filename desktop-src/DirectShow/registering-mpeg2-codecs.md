---
description: Registro de códecs MPEG2
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: Registro de códecs MPEG2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152207"
---
# <a name="registering-mpeg2-codecs"></a><span data-ttu-id="b542f-103">Registro de códecs MPEG2</span><span class="sxs-lookup"><span data-stu-id="b542f-103">Registering MPEG2 Codecs</span></span>

<span data-ttu-id="b542f-104">Este tema se aplica únicamente a Windows XP Media Center Edition.</span><span class="sxs-lookup"><span data-stu-id="b542f-104">This topic applies to Windows XP Media Center Edition only.</span></span>

<span data-ttu-id="b542f-105">Windows XP Media Center Edition mantiene dos claves del registro que utiliza para determinar qué códec utilizar para reproducir archivos de audio y vídeo MPEG2.</span><span class="sxs-lookup"><span data-stu-id="b542f-105">Windows XP Media Center Edition maintains two registry keys that it uses to determine which codec to use to play back MPEG2 video and audio files.</span></span> <span data-ttu-id="b542f-106">La primera clave del registro especifica el códec MPEG2 del fabricante del equipo y la segunda muestra todos los códecs compatibles con Media Center instalados actualmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b542f-106">The first registry key specifies the computer manufacturer's preferred MPEG2 codec, and the second lists all of the Media Center compatible codecs that are currently installed on the computer.</span></span> <span data-ttu-id="b542f-107">Cuando Media Center necesita reproducir un archivo MPEG2, usa el códec preferido del fabricante, si se especifica uno.</span><span class="sxs-lookup"><span data-stu-id="b542f-107">When Media Center needs to play back an MPEG2 file, it uses the manufacturer's preferred codec, if one is specified.</span></span> <span data-ttu-id="b542f-108">Si no es así, usa el primer códec compatible con Media Center que aparece en el registro.</span><span class="sxs-lookup"><span data-stu-id="b542f-108">If not, it uses the first Media Center compatible codec listed in the registry.</span></span> <span data-ttu-id="b542f-109">Si el registro no especifica códecs preferidos o compatibles, Media Center usa el mérito del filtro DirectShow estándar para elegir un códec.</span><span class="sxs-lookup"><span data-stu-id="b542f-109">If the registry specifies no preferred or compatible codecs, Media Center uses the standard DirectShow filter merit to choose a codec.</span></span>

<span data-ttu-id="b542f-110">Para asegurarse de que Media Center siempre usa un códec MPEG2 compatible, los fabricantes de equipos con Media Center deben especificar el códec MPEG2 preferido en la siguiente ubicación del registro:</span><span class="sxs-lookup"><span data-stu-id="b542f-110">To ensure that Media Center always uses a compatible MPEG2 codec, manufacturers of Media Center computers should specify the preferred MPEG2 codec at the following registry location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



<span data-ttu-id="b542f-111">Los datos clave deben ser los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b542f-111">The key data should be as follows:</span></span>


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



<span data-ttu-id="b542f-112">El programa de instalación de un códec MPEG2 compatible con Media Center debe registrar el códec mediante la creación de dos instancias de la siguiente clave del registro: una para el códec de vídeo y otra para el códec de audio:</span><span class="sxs-lookup"><span data-stu-id="b542f-112">The setup program for a Media Center compatible MPEG2 codec should register the codec by creating two instances of the following registry key—one for the video codec and one for the audio codec:</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



<span data-ttu-id="b542f-113">Los datos clave deben ser los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b542f-113">The key data should be as follows:</span></span>


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



