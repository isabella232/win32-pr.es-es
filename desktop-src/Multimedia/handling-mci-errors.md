---
title: Control de errores de MCI
description: Control de errores de MCI
ms.assetid: 01a2ff95-34a2-434f-9c7e-d0cdac826c02
keywords:
- Función mciSendCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab8412c74153d5ddfb03a3aff895f9f2e0e73798
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062909"
---
# <a name="handling-mci-errors"></a>Control de errores de MCI

Siempre debe comprobar el valor devuelto de la [**función mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Si indica un error, puede usar [**mciGetErrorString para**](/previous-versions//dd757158(v=vs.85)) obtener una descripción textual del error.

En el ejemplo siguiente se pasa el código de error de MCI especificado por *dwError* a **mciGetErrorString** y, a continuación, se muestra la descripción del error textual resultante mediante la [función MessageBox.](/windows/win32/api/winuser/nf-winuser-messagebox)


```C++
// Use mciGetErrorString to get a textual description of an MCI error.
// Display the error description using MessageBox.

void showError(DWORD dwError)
{
    char szErrorBuf[MAXERRORLENGTH];
    MessageBeep(MB_ICONEXCLAMATION);
    if(mciGetErrorString(dwError, (LPSTR) szErrorBuf, MAXERRORLENGTH))
    {
        MessageBox(hMainWnd, szErrorBuf, "MCI Error",
        MB_ICONEXCLAMATION);
    }
    else
    {
        MessageBox(hMainWnd, "Unknown Error", "MCI Error",
            MB_ICONEXCLAMATION);
    }
}
 
```



> [!Note]  
> Para interpretar un valor devuelto de error [**mciSendCommand,**](/previous-versions//dd757160(v=vs.85)) enmascara la palabra de orden superior (la palabra de orden bajo contiene el código de error). Sin embargo, si pasa el valor devuelto del error a [**mciGetErrorString,**](/previous-versions//dd757158(v=vs.85))debe pasar todo el valor doubleword.

 

 

 