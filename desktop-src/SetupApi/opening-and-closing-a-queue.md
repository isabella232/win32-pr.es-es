---
description: Antes de poder poner en cola las operaciones de archivo, debe abrir una cola de archivos. La llamada a la función SetupOpenFileQueue devuelve un identificador a un archivo de cola. Este identificador lo usan las funciones de cola subsiguientes para hacer referencia a la cola abierta y agregarle operaciones o examinarla.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Abrir y cerrar una cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667989"
---
# <a name="opening-and-closing-a-queue"></a>Abrir y cerrar una cola

Antes de poder poner en cola las operaciones de archivo, debe abrir una cola de archivos. La llamada a la función [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) devuelve un identificador a un archivo de cola. Este identificador lo usan las funciones de cola subsiguientes para hacer referencia a la cola abierta y agregarle operaciones o examinarla.

Una vez que todas las operaciones de archivo especificadas se han puesto en cola y confirmado, debe llamar a la función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) para liberar los recursos asignados durante la llamada a [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).

> [!Note]  
> La función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) no confirma la cola de archivos. Las operaciones que no se confirman cuando se llama a **SetupCloseFileQueue** no se realizarán.

 

 

 



