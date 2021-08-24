---
description: En el ejemplo de código siguiente se muestra el uso de un objeto mutex para determinar si el Explorador de MSN ha iniciado sesión.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Determinar si MSN está en estado de inicio de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654204"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Determinar si MSN está en estado de inicio de sesión

En el ejemplo de código siguiente se muestra el uso de un objeto mutex para determinar si el Explorador de MSN ha iniciado sesión. Cuando haya terminado de usar el identificador, asegúrese de llamar a la [**función CloseHandle.**](/windows/win32/api/handleapi/nf-handleapi-closehandle)

> [!Note]  
> Este objeto mutex está disponible para su uso en la comprobación de MSN Explorer 7. *x* estado de inicio de sesión. Puede que no esté disponible en versiones posteriores.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
