---
title: Abrir un dispositivo compuesto mediante el nombre de archivo
description: Abrir un dispositivo compuesto mediante el nombre de archivo
ms.assetid: 5199bb68-44be-4fad-af5b-8fe89f27caee
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20eb271658f77c5af4d35db96dd7bdbe6753af08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476796"
---
# <a name="opening-a-compound-device-by-using-the-filename"></a>Abrir un dispositivo compuesto mediante el nombre de archivo

En el ejemplo siguiente se abre el dispositivo de audio de forma de onda especificando un archivo de audio de forma de onda denominado "TIMPANI. WAV" mediante la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
UINT wDeviceID;
DWORD dwReturn;
MCI_OPEN_PARMS mciOpenParms;
 
// Opens a waveform-audio device by specifying the device and 
// file name.

mciOpenParms.lpstrDeviceType = "waveaudio";
mciOpenParms.lpstrElementName = "timpani.wav";

if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
    MCI_OPEN_TYPE | MCI_OPEN_ELEMENT, (DWORD)(LPVOID) &mciOpenParms))
{
    
    // Error, unable to open device.
    
}

// The device opened successfully; get the device ID.
wDeviceID = mciOpenParms.wDeviceID;
```



 

 