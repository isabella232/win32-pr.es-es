---
description: En el código siguiente se muestra cómo inicializar el controlador de símbolos.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Inicializar el controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998117"
---
# <a name="initializing-the-symbol-handler"></a>Inicializar el controlador de símbolos

En el código siguiente se muestra cómo inicializar el controlador de símbolos. La función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) pospone la carga de símbolos hasta que se solicita información de símbolos. El código carga los símbolos para cada módulo en el proceso especificado pasando un valor de **true** para el parámetro *bInvade* de la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . (Esta función llama a la función [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) para cada módulo que el proceso ha asignado en su espacio de direcciones).

Si el proceso especificado no es el proceso que llamó a [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), el código pasa un identificador de proceso como primer parámetro de **SymInitialize**.

Si se especifica **null** como el segundo parámetro de [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) , se indica que el controlador de símbolos debe usar la ruta de búsqueda predeterminada para buscar archivos de símbolos. Para obtener información detallada sobre cómo el controlador de símbolos busca archivos de símbolos o cómo una aplicación puede especificar una ruta de búsqueda de símbolos, vea rutas de acceso de [símbolos](symbol-paths.md).


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



 

 



