---
description: En los temas siguientes se describen los archivos de símbolos y la funcionalidad proporcionada por las funciones dbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Acerca de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162703"
---
# <a name="about-dbghelp"></a>Acerca de DbgHelp

En los temas siguientes se describen los archivos de símbolos y la funcionalidad proporcionada por [las funciones dbgHelp](dbghelp-functions.md).

-   [Versiones de DbgHelp](dbghelp-versions.md)
-   [Archivos de símbolos](symbol-files.md)
-   [Control de símbolos](symbol-handling.md)
-   [Servidores de símbolos y almacenes de símbolos](symbol-servers-and-symbol-stores.md)
-   [Archivos de minivolfón](minidump-files.md)
-   [Servidor de origen](source-server-and-source-indexing.md)
-   [Actualización de la compatibilidad para plataformas](updated-platform-support.md)

Tenga en cuenta que [todas las funciones de DbgHelp](dbghelp-functions.md) son de un solo subproceso. Por lo tanto, las llamadas de más de un subproceso a esta función probablemente darán lugar a un comportamiento inesperado o daños en la memoria. Para evitar esto, debe sincronizar todas las llamadas simultáneas de más de un subproceso a esta función.

 

 



