---
description: La configuración correcta de los símbolos para la depuración puede ser una tarea desafiante, especialmente para la depuración del kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Servidor de símbolos y almacenes de símbolos"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274909"
---
# <a name="symbol-server-and-symbol-stores"></a>  Servidor de símbolos y almacenes de símbolos

La configuración correcta de los símbolos para la depuración puede ser una tarea desafiante, especialmente para la depuración del kernel. A menudo, es necesario conocer los nombres y las versiones de todos los productos del equipo. El depurador debe ser capaz de encontrar los archivos de símbolos que corresponden a cada versión de producto y Service Pack. Esto puede dar lugar a una ruta de acceso de símbolos extremadamente larga formada por una larga lista de directorios.

Para simplificar estas dificultades en la coordinación de archivos de símbolos, use el *servidor de símbolos*. El servidor de símbolos permite que los depuradores recuperen automáticamente los archivos de símbolos correctos sin los nombres de producto, las versiones o los números de compilación. Herramientas de depuración para Windows contiene el servidor de símbolos SymSrv.

El servidor de símbolos se activa mediante la inclusión de una cadena de texto determinada en la ruta de acceso de símbolos. Cada vez que el depurador necesita cargar símbolos para un módulo recién cargado, llama al servidor de símbolos para buscar los archivos de símbolos adecuados. El servidor de símbolos ubica los archivos en un *almacén de símbolos*. Se trata de una colección de archivos de símbolos, un índice y una herramienta que un administrador puede usar para agregar y eliminar archivos. Los archivos se indexan según parámetros únicos, como la marca de tiempo y el tamaño de la imagen. Herramientas de depuración para Windows contiene una herramienta de almacén de símbolos denominada SymStore.

Para más información, consulte:

-   [Usar SymSrv](using-symsrv.md)
-   [Usar SymStore](using-symstore.md)
-   [Usar otros almacenes de símbolos](using-other-symbol-stores.md)
-   [Opciones de Command-Line de SymStore](symstore-command-line-options.md)
-   [Servidor de símbolos y firewalls de Internet](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos de símbolos](symbol-files.md)
</dt> </dl>

 

 



