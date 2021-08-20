---
description: Para poder poner en cola las operaciones de archivos, debe abrir una cola de archivos. Al llamar a la función SetupOpenFileQueue se devuelve un identificador a un archivo de cola. Este identificador lo usan las funciones de cola posteriores para hacer referencia a la cola abierta y agregarle operaciones o examinarla.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Abrir y cerrar una cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8465446842521adbd320816a76d7f545819eebf68b55aee0c3a057fc0ca3ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965158"
---
# <a name="opening-and-closing-a-queue"></a>Abrir y cerrar una cola

Para poder poner en cola las operaciones de archivos, debe abrir una cola de archivos. Al llamar [**a la función SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) se devuelve un identificador a un archivo de cola. Este identificador lo usan las funciones de cola posteriores para hacer referencia a la cola abierta y agregarle operaciones o examinarla.

Una vez que todas las operaciones de archivo especificadas se hayan puesto en cola y confirmado, debe llamar a la función [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) para liberar los recursos asignados durante la llamada a [**SetupOpenFileQueue.**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)

> [!Note]  
> La [**función SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) no confirma la cola de archivos. No se realizará ninguna operación que no esté confirmada cuando se llame a **SetupCloseFileQueue.**

 

 

 



