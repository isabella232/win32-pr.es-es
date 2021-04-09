---
description: En los temas siguientes se describen los archivos de símbolos y la funcionalidad proporcionada por las funciones DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Acerca de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152911"
---
# <a name="about-dbghelp"></a>Acerca de DbgHelp

En los temas siguientes se describen los archivos de símbolos y la funcionalidad proporcionada por las [funciones DbgHelp](dbghelp-functions.md).

-   [Versiones de DbgHelp](dbghelp-versions.md)
-   [Archivos de símbolos](symbol-files.md)
-   [Control de símbolos](symbol-handling.md)
-   [Servidores de símbolos y almacenes de símbolos](symbol-servers-and-symbol-stores.md)
-   [Archivos de minivolcado](minidump-files.md)
-   [Servidor de origen](source-server-and-source-indexing.md)
-   [Actualización de la compatibilidad para plataformas](updated-platform-support.md)

Tenga en cuenta que todas [las funciones DbgHelp](dbghelp-functions.md) tienen un único subproceso. Por lo tanto, las llamadas desde más de un subproceso a esta función probablemente producirán un comportamiento inesperado o daños en la memoria. Para evitar esto, debe sincronizar todas las llamadas simultáneas de más de un subproceso a esta función.

 

 



