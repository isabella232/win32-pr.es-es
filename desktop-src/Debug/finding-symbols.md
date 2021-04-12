---
description: Una vez cargado un archivo de símbolos en el controlador de símbolos, una aplicación puede usar las funciones del localizador de símbolos para devolver información de símbolos para una dirección especificada.
ms.assetid: bfc068e1-eced-4ab2-80a3-acc2ed07c841
title: Buscar símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f65830032cf363771b14f779726c59d976e8d30
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152729"
---
# <a name="finding-symbols"></a>Buscar símbolos

Una vez cargado un archivo de símbolos en el controlador de símbolos, una aplicación puede usar las funciones del localizador de símbolos para devolver información de símbolos para una dirección especificada. Estas funciones también pueden encontrar un nombre de archivo de código fuente y la ubicación del número de línea de una dirección.

## <a name="enumerating-symbol-files"></a>Enumerar archivos de símbolos

Para recuperar una lista de todos los archivos de símbolos cargados por el nombre del módulo, llame a la función [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) . Para obtener un ejemplo, consulte [enumeración de módulos de símbolos](enumerating-symbol-modules.md). Para recuperar una lista de símbolos para un módulo determinado, llame a la función [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) . Para obtener un ejemplo, vea [enumerar símbolos](enumerating-symbols.md).

## <a name="retrieving-symbols-by-address"></a>Recuperar símbolos por dirección

Para recuperar información simbólica para una dirección concreta, use la función [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) . Esta función recupera información y la almacena en una estructura [**de \_ información de símbolos**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) . Dado que los nombres de símbolo son de longitud variable, debe proporcionar espacio adicional en el búfer después de la declaración de la estructura de **\_ información de símbolos** . Para obtener un ejemplo, vea [recuperar información de símbolos por dirección](retrieving-symbol-information-by-address.md).

Tenga en cuenta que no es necesario que la dirección esté en un límite de símbolos. Si la dirección va después del principio de un símbolo, pero antes del final del símbolo (el principio del símbolo más el tamaño del símbolo), la función buscará el símbolo.

## <a name="retrieving-symbols-by-symbol-name"></a>Recuperar símbolos por nombre de símbolo

Para recuperar información simbólica en una estructura de [**\_ información de símbolos**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) para un módulo específico y un nombre de símbolo, use la función [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) . Si se establece la carga de símbolos diferida, **SymFromName** intentará cargar el archivo de símbolos para un módulo si aún no se ha cargado. Para especificar un nombre de módulo junto con un nombre de símbolo, use el *módulo* de sintaxis. *SymName*. El carácter "!" delimita el nombre del módulo a partir del nombre del símbolo. Para obtener un ejemplo, vea [recuperar información de símbolos por nombre](retrieving-symbol-information-by-name.md).

## <a name="retrieving-line-numbers-by-address"></a>Recuperar números de línea por dirección

Para recuperar la ubicación del código fuente para una dirección específica, utilice la función [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) . Esta función rellena una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) que incluye el nombre del archivo de código fuente y la ubicación del número de línea a la que se hace referencia en la dirección especificada. Para obtener un ejemplo, vea [recuperar información de símbolos por dirección](retrieving-symbol-information-by-address.md).

## <a name="retrieving-line-numbers-by-symbol-name"></a>Recuperar números de línea por nombre de símbolo

Para recuperar la ubicación del código fuente para un nombre de símbolo concreto, use la función [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) . Esta función es similar a [**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname), pero recupera una estructura [**IMAGEHLP \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) . Para usar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) o **SymGetLineFromName64**, debe establecer la opción cargar líneas (SYMOPT \_ cargar \_ líneas) mediante la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) . Para obtener un ejemplo, vea [recuperar información de símbolos por nombre](retrieving-symbol-information-by-name.md).

 

 



