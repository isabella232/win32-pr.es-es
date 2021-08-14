---
description: El controlador de símbolos está diseñado para realizar un seguimiento de varios conjuntos de archivos de símbolos.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inicialización del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d3664a564b0198d97549f2815abebf0e5e6058beb197ed33ca191a64407f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406085"
---
# <a name="symbol-handler-initialization"></a>Inicialización del controlador de símbolos

El controlador de símbolos está diseñado para realizar un seguimiento de varios conjuntos de archivos de símbolos.

Para inicializar el controlador de símbolos, llame a [**la función SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) El *parámetro hProcess* puede ser un número arbitrario único, un valor devuelto por la función [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o el identificador de cualquier proceso en ejecución. El *parámetro fInvadeProcess* indica si el controlador de símbolos debe enumerar los módulos cargados por el proceso y cargar símbolos para cada uno de sus módulos. Si *fInvadeProcess* es **TRUE,** el *parámetro hProcess* debe ser el valor devuelto por **GetCurrentProcess** o el identificador de un proceso existente. Para actualizar esta lista, use la [**función SymRefreshModuleList.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)

El *uso de fInvadeProcess* es una manera sencilla de cargar todos los archivos de símbolos de un proceso. Sin embargo, el controlador de símbolos no intentará cargar símbolos para los módulos cargados posteriormente por la [**función LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) En este caso, debe usar la función [**SymLoadModuleEx.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)

 

 
