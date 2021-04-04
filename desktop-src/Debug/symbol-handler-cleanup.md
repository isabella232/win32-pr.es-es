---
description: Para liberar toda la memoria usada por el controlador de símbolos para un proceso, utilice la función SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Limpieza del controlador de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907128"
---
# <a name="symbol-handler-cleanup"></a>Limpieza del controlador de símbolos

Para liberar toda la memoria usada por el controlador de símbolos para un proceso, utilice la función [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Esta función enumera todos los módulos cargados, libera cada módulo y libera la memoria asignada para la lista de módulos. Después de llamar a **SymCleanup**, no puede usar el identificador de proceso en las funciones de control de símbolos hasta que llame a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



