---
description: Un nombre de símbolo decorado incluye caracteres que distinguen cómo se ha declarado un símbolo público.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nombres de símbolos decorados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60432788b69f0c8779030f32a190ccfb55859434f714a13f769b328ee246a309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076419"
---
# <a name="decorated-symbol-names"></a>Nombres de símbolos decorados

Un nombre de símbolo decorado incluye caracteres que distinguen cómo se ha declarado un símbolo público. Para \_ \_ las funciones stdcall, los nombres incluyen el carácter "@" y un número decimal que especifica el número de bytes en sus parámetros de función. Por ejemplo, el nombre decorado de la [**función LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) es LoadLibrary@4 . Para las funciones de C++, la decoración de nombres es más compleja y varía de compilador a compilador.

Para recuperar el nombre de símbolo no decorado, use la [**función UnDecorateSymbolName.**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) Como alternativa, puede llamar a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para solicitar que el controlador de símbolos presente siempre símbolos con nombres no decorados. Debe establecer esta opción antes de cargar los símbolos porque el controlador de símbolos crea las tablas de nombres de símbolos en tiempo de carga.

 

 
