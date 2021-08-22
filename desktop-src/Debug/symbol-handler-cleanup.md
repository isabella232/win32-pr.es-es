---
description: Para liberar toda la memoria utilizada por el controlador de símbolos para un proceso, use la función SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Limpieza del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956964"
---
# <a name="symbol-handler-cleanup"></a>Limpieza del controlador de símbolos

Para liberar toda la memoria utilizada por el controlador de símbolos para un proceso, use la [**función SymCleanup.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) Esta función enumera todos los módulos cargados, libera cada módulo y libera la memoria asignada para la lista de módulos. Después de llamar a **SymCleanup,** no puede usar el identificador de proceso en las funciones de control de símbolos hasta que llame a la [**función SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)

 

 



