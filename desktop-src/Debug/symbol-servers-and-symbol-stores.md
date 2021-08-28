---
description: Configurar los símbolos correctamente para la depuración puede ser una tarea complicada, especialmente para la depuración del kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Servidor de símbolos y almacenes de símbolos"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a54753885fc1771c43223770421eb8c2bfe7feffc5bf39b60d875852ddce22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956954"
---
# <a name="symbol-server-and-symbol-stores"></a>  Servidor de símbolos y almacenes de símbolos

Configurar los símbolos correctamente para la depuración puede ser una tarea complicada, especialmente para la depuración del kernel. A menudo, es necesario conocer los nombres y versiones de todos los productos del equipo. El depurador debe poder localizar los archivos de símbolos correspondientes a cada versión de producto y Service Pack. Esto puede dar lugar a una ruta de acceso de símbolos extremadamente larga que consta de una larga lista de directorios.

Para simplificar estas dificultades en la coordinación de archivos de símbolos, use el *servidor de símbolos*. El servidor de símbolos permite a los depuradores recuperar automáticamente los archivos de símbolos correctos sin nombres de producto, versiones o números de compilación. Herramientas de depuración para Windows contiene el servidor de símbolos SymSrv.

El servidor de símbolos se activa mediante la inclusión de una cadena de texto determinada en la ruta de acceso del símbolo. Cada vez que el depurador necesita cargar símbolos para un módulo recién cargado, llama al servidor de símbolos para buscar los archivos de símbolos adecuados. El servidor de símbolos busca los archivos en un almacén *de símbolos*. Se trata de una colección de archivos de símbolos, un índice y una herramienta que un administrador puede usar para agregar y eliminar archivos. Los archivos se indexan según parámetros únicos, como la marca de tiempo y el tamaño de la imagen. Herramientas de depuración para Windows contiene una herramienta de almacén de símbolos denominada SymStore.

Para más información, consulte:

-   [Uso de SymSrv](using-symsrv.md)
-   [Uso de SymStore](using-symstore.md)
-   [Usar otros almacenes de símbolos](using-other-symbol-stores.md)
-   [Opciones de Command-Line SymStore](symstore-command-line-options.md)
-   [Servidor de símbolos e firewalls de Internet](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos de símbolos](symbol-files.md)
</dt> </dl>

 

 



