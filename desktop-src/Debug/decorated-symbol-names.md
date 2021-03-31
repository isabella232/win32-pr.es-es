---
description: Un nombre de símbolo representativo incluye caracteres que distinguen el modo en que se ha declarado un símbolo público.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Nombres de símbolos representativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495802"
---
# <a name="decorated-symbol-names"></a>Nombres de símbolos representativos

Un nombre de símbolo representativo incluye caracteres que distinguen el modo en que se ha declarado un símbolo público. En el caso de \_ \_ las funciones Stdcall, los nombres incluyen el carácter "@" y un número decimal que especifica el número de bytes en sus parámetros de función. Por ejemplo, el nombre representativo de la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) es LoadLibrary@4 . En las funciones de C++, la decoración del nombre es más compleja y varía de un compilador a un compilador.

Para recuperar el nombre de símbolo no representativo, utilice la función [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) . Como alternativa, puede llamar a la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para solicitar que el controlador de símbolos presente siempre símbolos con nombres no representativos. Debe establecer esta opción antes de cargar los símbolos, ya que el controlador de símbolos crea las tablas de nombres de símbolos en el momento de la carga.

 

 
