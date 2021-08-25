---
description: La siguiente definición de Winternl.h es la dirección de memoria estática del identificador de sesión de la consola de Terminal Services activo. Este identificador de sesión de consola activo no se define en las versiones del sistema operativo microsoft Windows anterior a Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Obtención del identificador de sesión de la consola activa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002305"
---
# <a name="getting-the-active-console-session-id"></a>Obtención del identificador de sesión de la consola activa

La siguiente definición de Winternl.h es la dirección de memoria estática del identificador de sesión de la consola de Terminal Services activo. Este identificador de sesión de consola activo no se define en las versiones del sistema operativo microsoft Windows anterior a Windows XP.

> [!Note]  
> Esta definición puede cambiar en futuras versiones de Windows. Para asegurarse de que la aplicación seguirá funcionando correctamente en el futuro, la aplicación debe llamar a [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
