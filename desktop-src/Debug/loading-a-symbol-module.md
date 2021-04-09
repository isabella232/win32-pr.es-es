---
description: Si una aplicación no llama a la función SymInitialize con el parámetro fInvadeProcess establecido en TRUE, debe cargar los símbolos para un módulo cuando sea necesario.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Cargar un módulo de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152820"
---
# <a name="loading-a-symbol-module"></a>Cargar un módulo de símbolos

Si una aplicación no llama a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con el parámetro *FInvadeProcess* establecido en **true**, debe cargar los símbolos para un módulo cuando sea necesario. Para cargar un módulo de símbolos a petición, la aplicación puede llamar a la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) con una ruta de acceso completa a un nombre de módulo. Cuando se carga el módulo, el controlador de símbolos cargará los símbolos inmediatamente o aplazará la carga, dependiendo de las opciones establecidas mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

En el código siguiente se carga un módulo de símbolos. Tenga en cuenta que se supone que ha inicializado el controlador de símbolos mediante el código en la [inicialización del controlador de símbolos](initializing-the-symbol-handler.md).


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



Tenga en cuenta que *szImageName* puede ser una ruta de acceso a cualquier módulo ejecutable que tenga información de depuración (. exe,. dll,. drv,. sys,. SCR,. cpl,. com). Además, *dwBaseAddr* es la dirección base del módulo de símbolos que se va a cargar. Si este valor es 0, el controlador de símbolos obtendrá la dirección base del módulo de símbolos especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descargar un módulo de símbolos](unloading-a-symbol-module.md)
</dt> </dl>

 

 



