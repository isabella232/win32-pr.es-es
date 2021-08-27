---
title: Reproducción del archivo AVI
description: Reproducción del archivo AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e0c490a61bbd53dd62a8223a3ded1aa047ce071d1d2544a2b26d1a9152450b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038025"
---
# <a name="playing-the-avi-file"></a>Reproducción del archivo AVI

Antes de usar la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar el comando [**\_ MCI PLAY,**](mci-play.md) la aplicación asigna la memoria para la estructura, inicializa los miembros que usará y establece las marcas correspondientes a los miembros utilizados en la estructura. (Si la aplicación no establece una marca para un miembro de estructura, los controladores de MCI omiten el miembro). Por ejemplo, en el ejemplo siguiente se reproduce una película desde la posición inicial especificada por **dwFrom** hasta la posición final especificada por **dwTo**. (Si cualquiera de las posiciones es cero, el ejemplo se escribe para que no se utilice la posición).


```C++
DWORD PlayMovie(WORD wDevID, DWORD dwFrom, DWORD dwTo) 
{ 
    MCI_DGV_PLAY_PARMS mciPlay;    // play parameters 
    DWORD dwFlags = 0; 
 
    // Check dwFrom. If it is != 0 then set parameters and flags. 
    if (dwFrom){ 
        mciPlay.dwFrom = dwFrom; // set parameter 
        dwFlags |= MCI_FROM;     // set flag to validate member 
    } 
 
    // Check dwTo. If it is != 0 then set parameters and flags. 
    if (dwTo){ 
        mciPlay.dwTo = dwTo;    // set parameter 
        dwFlags |= MCI_TO;      // set flag to validate member 
    } 
 
    // Send the MCI_PLAY command and return the result. 
    return mciSendCommand(wDevID, MCI_PLAY, dwFlags, 
       (DWORD)(LPVOID)&mciPlay); 
} 
```



 

 