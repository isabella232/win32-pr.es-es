---
title: Reproducción del archivo AVI
description: Reproducción del archivo AVI
ms.assetid: 6b3845c4-40ec-4824-88c8-6e4ac458f720
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31754bd5f66b455abc76d363c5ff3e5e286e8040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169589"
---
# <a name="playing-the-avi-file"></a>Reproducción del archivo AVI

Antes de usar la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para enviar el comando [**\_ MCI PLAY,**](mci-play.md) la aplicación asigna la memoria de la estructura, inicializa los miembros que usará y establece las marcas correspondientes a los miembros utilizados en la estructura. (Si la aplicación no establece una marca para un miembro de estructura, los controladores de MCI omiten el miembro). Por ejemplo, en el ejemplo siguiente se reproduce una película desde la posición inicial especificada por **dwFrom** hasta la posición final especificada por **dwTo**. (Si cualquiera de las posiciones es cero, el ejemplo se escribe para que no se utilice la posición).


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



 

 