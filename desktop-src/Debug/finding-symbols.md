---
description: Una vez cargado un archivo de símbolos en el controlador de símbolos, una aplicación puede usar las funciones de localizador de símbolos para devolver información de símbolos para una dirección especificada.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Buscar símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90aae9d2894ca8abc7470b2068b508655a50bcb76e1a122f2307f81273abec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912705"
---
# <a name="finding-symbols"></a>Buscar símbolos

Una vez cargado un archivo de símbolos en el controlador de símbolos, una aplicación puede usar las funciones de localizador de símbolos para devolver información de símbolos para una dirección especificada. Estas funciones también pueden encontrar un nombre de archivo de código fuente y una ubicación de número de línea para una dirección.

## <a name="enumerating-symbol-files"></a>Enumerar archivos de símbolos

Para recuperar una lista de todos los archivos de símbolos cargados por el nombre del módulo, llame a la función [**SymEnumerateModules64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) Para obtener un ejemplo, vea [Enumerar módulos de símbolos](enumerating-symbol-modules.md). Para recuperar una lista de símbolos para un módulo determinado, llame a la [**función SymEnumSymbols.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) Para obtener un ejemplo, vea [Enumerar símbolos](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Recuperar símbolos por dirección

Para recuperar información simbólica de una dirección específica, use la [**función SymFromAddr.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) Esta función recupera información y la almacena en una [**estructura SYMBOL \_ INFO.**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) Dado que los nombres de símbolos tienen una longitud variable, debe proporcionar espacio de búfer adicional después de la **declaración de estructura SYMBOL \_ INFO.** Para obtener un ejemplo, vea [Recuperar información de símbolos por dirección](retrieving-symbol-information-by-address.md).

Tenga en cuenta que la dirección no necesita estar en un límite de símbolos. Si la dirección viene después del principio de un símbolo pero antes del final del símbolo (el principio del símbolo más el tamaño del símbolo), la función buscará el símbolo.

## <a name="retrieving-symbols-by-symbol-name"></a>Recuperar símbolos por nombre de símbolo

Para recuperar información simbólica en una estructura [**SYMBOL \_ INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) para un módulo específico y un nombre de símbolo, use la [**función SymFromName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) Si se establece la carga diferida de símbolos, **SymFromName** intentará cargar el archivo de símbolos de un módulo si aún no se ha cargado. Para especificar un nombre de módulo junto con un nombre de símbolo, use la sintaxis *Module*! *SymName*. El carácter "!" delimita el nombre del módulo del nombre del símbolo. Para obtener un ejemplo, vea [Recuperar información de símbolos por nombre.](retrieving-symbol-information-by-name.md)

## <a name="retrieving-line-numbers-by-address"></a>Recuperar números de línea por dirección

Para recuperar la ubicación del código fuente de una dirección específica, use la [**función SymGetLineFromAddr64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) Esta función rellena una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) que incluye el nombre de archivo de origen y la ubicación del número de línea a la que hace referencia la dirección especificada. Para obtener un ejemplo, vea [Recuperar información de símbolos por dirección](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Recuperar números de línea por nombre de símbolo

Para recuperar la ubicación del código fuente de un nombre de símbolo específico, use la [**función SymGetLineFromName64.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) Esta función es similar a [**SymGetSymFromName64,**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)pero recupera una [**estructura IMAGEHLP \_ LINE64.**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) Para usar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) o **SymGetLineFromName64,** debe establecer la opción de líneas de carga (SYMOPT LOAD LINES) mediante la \_ función \_ [**SymSetOptions.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) Para obtener un ejemplo, vea [Recuperar información de símbolos por nombre.](retrieving-symbol-information-by-name.md)

 

 



