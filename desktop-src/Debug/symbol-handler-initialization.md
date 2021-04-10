---
description: El controlador de símbolos está diseñado para realizar el seguimiento de varios conjuntos de archivos de símbolos.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Inicialización del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152846"
---
# <a name="symbol-handler-initialization"></a>Inicialización del controlador de símbolos

El controlador de símbolos está diseñado para realizar el seguimiento de varios conjuntos de archivos de símbolos.

Para inicializar el controlador de símbolos, llame a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . El parámetro *hProcess* puede ser un número arbitrario único, un valor devuelto por la función [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) o el identificador de cualquier proceso en ejecución. El parámetro *fInvadeProcess* indica si el controlador de símbolos debe enumerar los módulos cargados por el proceso y cargar los símbolos para cada uno de sus módulos. Si *fInvadeProcess* es **true**, el parámetro *hProcess* debe ser el valor devuelto desde **GetCurrentProcess** o el identificador de un proceso existente. Para actualizar esta lista, use la función [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .

El uso de *fInvadeProcess* es una forma sencilla de cargar todos los archivos de símbolos para un proceso. Sin embargo, el controlador de símbolos no intentará cargar símbolos para los módulos cargados posteriormente por la función [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . En este caso, debe usar la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .

 

 
