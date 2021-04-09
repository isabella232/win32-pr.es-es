---
title: Recuperación de la información de Track-Specific de CD
description: Recuperación de la información de Track-Specific de CD
ms.assetid: 7a26fac2-7cc5-4a65-b045-35baf979c134
keywords:
- MCI_TRACK marca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb71e57ee1b2d7e300f0567359ab5d435cb310e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995114"
---
# <a name="retrieving-compact-disc-track-specific-information"></a>Recuperación de la información de Track-Specific de CD

En el caso de los dispositivos de audio de CD, puede obtener la ubicación de inicio y la longitud de una pista especificando la \_ marca de pista de MCI y estableciendo el miembro **DwTrack** de [**MCI \_ status \_ parms**](mci-status-parms.md) en el número de pista deseado. Para obtener la ubicación inicial de una pista, establezca el miembro **dwItem** en la \_ posición de estado de MCI \_ . Para obtener la longitud de una pista, establezca **dwItem** en la \_ longitud del estado de MCI \_ . Por ejemplo, en el ejemplo siguiente se recupera el número total de pistas del disco compacto y la ubicación inicial de cada pista. A continuación, utiliza la función [MessageBox](/windows/win32/api/winuser/nf-winuser-messagebox) para notificar las ubicaciones de inicio de las pistas.


```C++
// Uses the MCI_STATUS command to get and display the 
// starting times for the tracks on a compact disc. 
// Returns 0L if successful; otherwise, it returns an 
// MCI error code.

DWORD DisplayCDTrackStartTimes(HWND hMainWnd)
{
    UINT wDeviceID;
    int i, iNumTracks;
    DWORD dwReturn;
    DWORD *pMem;
    TCHAR szTempString[64];
    TCHAR szTimeString[512] = TEXT("\0");  // Room for 20 tracks.
    MCI_OPEN_PARMS mciOpenParms;
    MCI_SET_PARMS mciSetParms;
    MCI_STATUS_PARMS mciStatusParms;

    // Open the device by specifying the device name.
    mciOpenParms.lpstrDeviceType = TEXT("cdaudio");
    if (dwReturn = mciSendCommand(NULL, MCI_OPEN,
        MCI_OPEN_TYPE, (DWORD_PTR)(LPVOID) &mciOpenParms))
    {
        // Failed to open device. 
        // Don't close device; just return error.
        return (dwReturn);
    }

    // The device opened successfully; get the device ID.
    wDeviceID = mciOpenParms.wDeviceID;

    // Set the time format to minute/second/frame (MSF) format. 
    mciSetParms.dwTimeFormat = MCI_FORMAT_MSF;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_SET, 
        MCI_SET_TIME_FORMAT, 
        (DWORD_PTR)(LPVOID) &mciSetParms)) 
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }

    // Get the number of tracks; 
    // limit it to the number that can be displayed (20).
    mciStatusParms.dwItem = MCI_STATUS_NUMBER_OF_TRACKS;
    if (dwReturn = mciSendCommand(wDeviceID, MCI_STATUS, 
        MCI_STATUS_ITEM, (DWORD_PTR)(LPVOID) &mciStatusParms)) 
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (dwReturn);
    }
    iNumTracks = (int)mciStatusParms.dwReturn;
    iNumTracks = min(iNumTracks, 20);

    // Allocate memory to hold starting positions.
    pMem = (DWORD *)LocalAlloc(LPTR, 
        iNumTracks * sizeof(DWORD));
    if (pMem == NULL) 
    {
        mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
        return (-1);
    } 
 
    // For each track, get and save the starting location and
    // build a string containing the starting locations.
    for(i=1; i<=iNumTracks; i++) 
    {
        mciStatusParms.dwItem = MCI_STATUS_POSITION;
        mciStatusParms.dwTrack = i;
        if (dwReturn = mciSendCommand(wDeviceID, 
            MCI_STATUS, MCI_STATUS_ITEM | MCI_TRACK, 
            (DWORD_PTR)(LPVOID) &mciStatusParms)) 
        {
            mciSendCommand(wDeviceID, MCI_CLOSE, 0, NULL);
            return (dwReturn);
        }

        pMem[i-1] = (DWORD)mciStatusParms.dwReturn;

        _stprintf_s(szTempString, 
            TEXT("Track %2d - %02d:%02d:%02d\n"), i,
            MCI_MSF_MINUTE(pMem[i-1]), 
            MCI_MSF_SECOND(pMem[i-1]), 
            MCI_MSF_FRAME(pMem[i-1]));

        _tcscat_s(szTimeString, szTempString);
    }

    // Use MessageBox to display starting times.
    MessageBox(
        hMainWnd, 
        szTimeString, 
        TEXT("Track Starting Position"), 
        MB_ICONINFORMATION);

    // Free memory and close the device.
    LocalFree((HANDLE) pMem);
    if (dwReturn = mciSendCommand(wDeviceID, 
        MCI_CLOSE, 0, NULL)) 
    {
        return (dwReturn);
    }

    return (0L);
}
```



 

 