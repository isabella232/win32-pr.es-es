---
description: Las funcionalidades de control de símbolos de dbgHelp API han evolucionado a lo largo de los años.
ms.assetid: 6dc41682-6104-418b-b045-7afe8c2b11e9
title: Símbolos públicos, globales y locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ecaa40549b091af204f2e318aefef8a256408e5f81b461e63a54c333719dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406105"
---
# <a name="public-global-and-local-symbols"></a>Símbolos públicos, globales y locales

Las funcionalidades de control de símbolos de dbgHelp API han evolucionado a lo largo de los años. Para asegurarse de que el código funciona en una variedad de escenarios y proporciona detalles completos sobre los símbolos, use las funciones más nuevas siempre que sea posible. Por ejemplo, [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) reemplaza [**a SymEnumerateSymbols64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols) [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) reemplaza [**a SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)y [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) reemplaza [**a SymGetSymFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)

## <a name="public-symbols"></a>Símbolos públicos

Las versiones iniciales de DbgHelp.dll solo admiten el examen de símbolos públicos. Estos símbolos se generan para cualquier elemento del código que se debe exponer entre distintos archivos de origen. También incluyen todos los elementos que se exportan fuera del módulo.

Los símbolos se incrustan en la imagen o se almacenan por separado en un archivo .dbg o .pdb. La única información almacenada es el nombre y la dirección del símbolo. Los nombres están disponibles como nombres decorados. Para ver nombres no decorados, llame a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT UNDNAME o use la función \_ [**UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)

Tenga en cuenta que la API DbgHelp no se diseñó inicialmente para admitir varias instancias del mismo símbolo dentro de un módulo. Esto se debe a que los símbolos públicos están restringidos a nombres únicos dentro de un módulo. Por lo [**tanto, SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname) devuelve solo el primer símbolo que coincide. Para recuperar todos los símbolos que coinciden, llame a [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols).

## <a name="global-and-local-symbols"></a>Símbolos globales y locales

Las versiones más recientes DbgHelp.dll admiten símbolos globales y locales al usar archivos .pdb. Estas nuevas versiones incluyen funciones estáticas, funciones con ámbito dentro de un archivo de código fuente, parámetros de función y variables locales. Cuando DbgHelp busca un símbolo, comprueba las tablas de símbolos globales y locales antes de comprobar la tabla de símbolos públicos. Esto se debe a que hay más información disponible para estos tipos de símbolos que para símbolos públicos.

Los símbolos globales y locales se almacenan con nombres no decorados. Por lo tanto, la marca \_ SYMOPT UNDNAME no tiene ningún efecto. Para obtener nombres de símbolos decorados, debe usar la marca SOLO SYMOPT \_ \_ PUBLICS. Esto hace que DbgHelp busque solo los símbolos públicos.

Para ver símbolos locales o parámetros de función, llame a la función [**SymSetContext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext) con el miembro **InstructionOffset** de la estructura [**IMAGEHLP \_ STACK \_ FRAME**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_stack_frame) establecida en la dirección de cualquier símbolo de función. Las llamadas [**posteriores a SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) y [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) pueden funcionar en el contexto de esta dirección. Para ello, establezca el *parámetro BaseOfDll* en **NULL** y omita el especificador de módulo del *parámetro Name* *o Mask.* Esto obliga a DbgHelp a buscar símbolos que coincidan dentro del ámbito indicado por **SymSetContext**.

Para determinar si un símbolo es un parámetro, compruebe el **miembro Flags** de la [**estructura SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Si el símbolo es un parámetro, el miembro contiene SYMFLAG \_ PARAMETER. Si es un símbolo local, el miembro contiene SYMFLAG \_ LOCAL.

 

 



