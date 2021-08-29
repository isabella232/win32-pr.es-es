---
title: Reproducir una pista de disco compacto
description: Reproducir una pista de disco compacto
ms.assetid: 05f68361-7fec-4c45-b434-a8b654f2d0c3
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48764ad0a79921ceb65e89d5adeaf22606d74103c853f7257f937c9919c32a10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038024"
---
# <a name="playing-a-compact-disc-track"></a>Reproducir una pista de disco compacto

En el ejemplo siguiente se abre un dispositivo de audio de CD, se reproduce la pista especificada por el *parámetro bTrack* y se cierra el dispositivo una vez completada la reproducción. Usa la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85))


```C++
// Plays a specified audio track using MCI_OPEN, MCI_PLAY. Returns as 
// soon as playback begins. The window procedure function for the 
// specified window will be notified when playback is complete. 
// Returns 0L on success; otherwise, returns an MCI error code.

DWORD playCDTrack(HWND hWndNotify, BYTE bTrack)
{
    UINT wDeviceID;
    DWORD dwReturn;
    MCI_OPEN_PARMS mciOpenParms;
    MCI_SET_PARMS mciSetParms;
    MCI_PLAY_PARMS mciPlayParms;

    // Open the CD audio device by specifying the device name.
    mciOpenParms.lpstrDeviceType = "cdaudio";
    if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
        MCI_OPEN_TYPE, (DWORD)(LPVOID) &mciOpenParms))
    {
        // Failed to open device. Don't close it; just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Set the time format to track/minute/second/frame (TMSF).
    mciSetParms.dwTimeFormat = MCI_FORMAT_TMSF;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_SET, 
        MCI_SET_TIME_FORMAT, (DWORD)(LPVOID) &mciSetParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    } 
    // Begin play from the specified track and play to the beginning 
    // of the next track. The window procedure function for the parent 
    // window will be notified with an MM_MCINOTIFY message when 
    // playback is complete. Unless the play command fails, the window 
    // procedure closes the device.

    mciPlayParms.dwFrom = 0L;
    mciPlayParms.dwTo = 0L;
    mciPlayParms.dwFrom = MCI_MAKE_TMSF(bTrack, 0, 0, 0);
    mciPlayParms.dwTo = MCI_MAKE_TMSF(bTrack + 1, 0, 0, 0);
    mciPlayParms.dwCallback = (DWORD) hWndNotify;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_PLAY,
        MCI_FROM | MCI_TO | MCI_NOTIFY, 
        (DWORD)(LPVOID) &mciPlayParms))
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    return (0L);
}
```



Para especificar una posición relativa a una pista en un disco compacto, debe usar el formato de tiempo pista/minuto/segundo/fotograma (TMSF).

 

 