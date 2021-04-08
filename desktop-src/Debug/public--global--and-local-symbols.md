---
description: La funcionalidad de control de símbolos de la API de DbgHelp ha evolucionado a lo largo de los años.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Símbolos públicos, globales y locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bf93ec8f11d1cec9c5fec64e2479dd91ee5cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080156"
---
# <a name="public-global-and-local-symbols"></a>Símbolos públicos, globales y locales

La funcionalidad de control de símbolos de la API de DbgHelp ha evolucionado a lo largo de los años. Para asegurarse de que el código funciona en diversos escenarios y proporciona detalles completos sobre los símbolos, utilice las funciones más recientes siempre que sea posible. Por ejemplo, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) reemplaza a [**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols), [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) reemplaza a [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)y [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) reemplaza [**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr).

## <a name="public-symbols"></a>Símbolos públicos

Las versiones iniciales de DbgHelp.dll admiten el examen de solo símbolos públicos. Estos símbolos se generan para cualquier elemento del código que se debe exponer entre distintos archivos de código fuente. También incluyen todos los elementos que se exportan fuera del módulo.

Los símbolos se incrustan en la imagen o se almacenan por separado en un archivo. dbg o. pdb. La única información almacenada es el nombre y la dirección del símbolo. Los nombres están disponibles como nombres representativos. Para ver los nombres no representativos, llame a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT \_ UNDNAME o use la función [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .

Tenga en cuenta que la API de DbgHelp no se diseñó inicialmente para admitir varias instancias del mismo símbolo dentro de un módulo. Esto se debe a que los símbolos públicos están restringidos a nombres únicos dentro de un módulo. Por lo tanto, [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) devuelve solo el primer símbolo que coincide con. Para recuperar todos los símbolos que coinciden, llame a [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Símbolos globales y locales

Las versiones más recientes de DbgHelp.dll admiten símbolos globales y locales al utilizar archivos. pdb. Estas nuevas versiones incluyen funciones estáticas, con ámbito dentro de un archivo de código fuente, parámetros de función y variables locales. Cuando DbgHelp busca un símbolo, comprueba las tablas de símbolos globales y locales antes de comprobar la tabla de símbolos públicos. Esto se debe a que hay más información disponible para estos tipos de símbolos que está disponible para los símbolos públicos.

Los símbolos globales y locales se almacenan con nombres no representativos. Por lo tanto, la \_ marca SYMOPT UNDNAME no tiene ningún efecto. Para obtener nombres representativos de símbolos, debe usar la \_ marca SYMOPT Public \_ only. Esto hace que DbgHelp busque solo los símbolos públicos.

Para ver los símbolos locales o los parámetros de función, llame a la función [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) con el miembro **InstructionOffset** de la estructura de [**\_ \_ marco de pila IMAGEHLP**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) establecida en la dirección de cualquier símbolo de función. Las llamadas subsiguientes a [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) y [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) pueden funcionar en el contexto de esta dirección. Para ello, establezca el parámetro *BaseOfDll* en **null** y omita el especificador de módulo del parámetro *Name* o *Mask* . Esto obliga a DbgHelp a buscar símbolos coincidentes dentro del ámbito indicado por **SymSetContext**.

Para determinar si un símbolo es un parámetro, compruebe el miembro **Flags** de la estructura [**Symbol \_ info**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Si el símbolo es un parámetro, el miembro contiene el \_ parámetro SYMFLAG. Si es un símbolo local, el miembro contiene SYMFLAG \_ local.

 

 



