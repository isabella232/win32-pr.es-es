---
description: Cuando sea necesario, la biblioteca DbgHelp se ha ensandado para admitir las bibliotecas de 32 y 64 Windows.
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: Actualización de la compatibilidad para plataformas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44389b0b46782318b3f017fe1baf8c2c0580d6993f9de4dfaa9ece64feae8c17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912383"
---
# <a name="updated-platform-support"></a>Actualización de la compatibilidad para plataformas

Cuando sea necesario, la biblioteca DbgHelp se ha ensandado para admitir las bibliotecas de 32 y 64 Windows. Las definiciones de función y estructura originales todavía están en DbgHelp.h, pero también hay versiones actualizadas de estas definiciones que son compatibles con las definiciones de 64 bits Windows. Si usa las funciones actualizadas en el código, se puede compilar para las funciones de 32 y 64 Windows. El código también será más eficaz, ya que las funciones originales simplemente llaman a las funciones actualizadas para realizar el trabajo.

Por ejemplo, DbgHelp.h contiene definiciones de **SymUnloadModule** (función original) y **SymUnloadModule64** (función actualizada). Estas definiciones son casi idénticas, pero usan tipos diferentes para el *parámetro BaseOfDll.* (**SymUnloadModule usa** el **tipo DWORD,** mientras **que SymUnloadModule64** usa el **tipo DWORD64).** Si escribe el código para usar **SymUnloadModule64,** se puede compilar para archivos de 32 y 64 Windows. El código también es más eficaz que si llamara a **SymUnloadModule**.

A continuación se muestra una lista de las funciones actualizadas:

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

A continuación se muestra una lista de las estructuras actualizadas:

<dl>

[**ADDRESS64**](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[**IMAGEHLP \_ DEFERRED \_ SYMBOL \_ LOAD64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[**IMAGEHLP \_ DUPLICATE \_ SYMBOL64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[**IMAGEHLP \_ MODULE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[**IMAGEHLP \_ SYMBOL64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[**KDHELP64**](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[**STACKFRAME64**](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



