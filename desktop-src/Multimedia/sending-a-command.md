---
title: Envío de un comando
description: Envío de un comando
ms.assetid: 28c38f36-b6a7-44da-95e2-25b3dccefc84
keywords:
- Función mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2b5763ae93887da607cfba9e94f55a254d7bcd8b0413e40ab9dff45f922cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801755"
---
# <a name="sending-a-command"></a>Envío de un comando

La siguiente función de ejemplo envía el [**comando play**](play.md) con las marcas "from" y "to" mediante la [**función mciSendString.**](/previous-versions//dd757161(v=vs.85))


```C++
BOOL PlayFromTo(LPTSTR lpstrAlias, DWORD dwFrom, DWORD dwTo) 
{ 
    TCHAR achCommandBuff[128]; 
    int result;
    MCIERROR err;

    // Form the command string.
    result = _stprintf_s(
        achCommandBuff, 
        TEXT("play %s from %u to %u"), 
        lpstrAlias, dwFrom, dwTo); 

    if (result == -1)
    {
        return FALSE;
    }

    // Send the command string.
    err = mciSendString(achCommandBuff, NULL, 0, NULL); 
    if (err != 0)
    {
        return FALSE;
    }

    return TRUE;
} 
```



 

 