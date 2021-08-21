---
description: En el código siguiente se muestra cómo inicializar el controlador de símbolos.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inicialización del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f1da864c4550232d278b6bfb9b2006a6d56956e363dcf4fbd72ed0e6b9685d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956984"
---
# <a name="initializing-the-symbol-handler"></a>Inicialización del controlador de símbolos

En el código siguiente se muestra cómo inicializar el controlador de símbolos. La [**función SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) aplaza la carga de símbolos hasta que se solicita información de símbolos. El código carga los símbolos de cada módulo del proceso especificado pasando un valor **de TRUE** para el *parámetro bInvade* de la [**función SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) (Esta función llama a [**la función SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) para cada módulo que el proceso ha asignado a su espacio de direcciones).

Si el proceso especificado no es el que llamó a [**SymInitialize,**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)el código pasa un identificador de proceso como primer parámetro de **SymInitialize**.

Especificar **NULL como** segundo parámetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indica que el controlador de símbolos debe usar la ruta de acceso de búsqueda predeterminada para buscar archivos de símbolos. Para obtener información detallada sobre cómo el controlador de símbolos busca archivos de símbolos o cómo una aplicación puede especificar una ruta de búsqueda de símbolos, vea [Rutas de acceso de símbolos](symbol-paths.md).


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



