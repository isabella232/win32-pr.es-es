---
description: En el siguiente ejemplo se bloquea la estación de trabajo mediante la función LockWorkStation. El sistema muestra el cuadro de diálogo bloquear estación de trabajo. El texto del cuadro de diálogo indica que la estación de trabajo está en uso y que el usuario la ha bloqueado.
ms.assetid: 7cbf9a0a-dfab-42e6-9a71-bb240121f59f
title: Cómo bloquear la estación de trabajo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa6c198816613a13914c44a5a51f5317e2019f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910330"
---
# <a name="how-to-lock-the-workstation"></a>Cómo bloquear la estación de trabajo

En el siguiente ejemplo se bloquea la estación de trabajo mediante la función [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation) . El sistema muestra el cuadro de diálogo **bloquear estación de trabajo** . El texto del cuadro de diálogo indica que la estación de trabajo está en uso y que el usuario la ha bloqueado.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment( lib, "user32.lib" )

void main()
{
    // Lock the workstation.

    if( !LockWorkStation() )
        printf ("LockWorkStation failed with %d\n", GetLastError());
}
```



Para determinar si la estación de trabajo está bloqueada, pruebe si la ventana está visible.

El usuario o un administrador pueden desbloquear la estación de trabajo. Para desbloquear el sistema, presione Ctrl + Alt + Supr e inicie sesión. Para recibir una notificación cuando el usuario inicie sesión, utilice la función [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) para registrarse y recibir los mensajes de [**cambio de \_ WTSSESSION \_ de WM**](../termserv/wm-wtssession-change.md) . Cuando se reciba este mensaje, compruebe si el parámetro *wParam* es igual al bloqueo de la sesión de WTS \_ \_ .

 

 
