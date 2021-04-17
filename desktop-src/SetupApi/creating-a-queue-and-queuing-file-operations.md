---
description: Poner en cola las operaciones de archivo es útil porque le permite procesar la instalación en conjunto, en lugar de en la sección INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Creación de una cola y operaciones de archivo de colas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667658"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>Creación de una cola y operaciones de archivo de colas

Poner en cola las operaciones de archivo es útil porque le permite procesar la instalación en conjunto, en lugar de en la sección INF.

Para crear una cola de archivos, declare una variable para almacenar el identificador de la cola y, a continuación, llame a la función [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) . Una vez creada la cola, puede poner en cola las operaciones de copia, cambio de nombre y eliminación, así como examinar la cola de archivos para comprobar las operaciones en cola.

Para agregar operaciones de archivo único a la cola, use las funciones [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)y [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .

Todas las operaciones de archivo enumeradas en una sección **copiar archivos**, **eliminar archivos** o **cambiar nombre de archivos** se pueden agregar a la cola mediante [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)o [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectivamente.

Otra manera de poner en cola todos los archivos de las secciones **Copy files** enumeradas en una sección **install** de un archivo INF es usar la función [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).

En el ejemplo siguiente se usa la función [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) para poner en cola las operaciones de copia de todos los archivos enumerados en una sección **Copy files** de un archivo INF.

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

En el ejemplo, la cola es la cola a la que se agregan las operaciones de copia, "A: \\ " especifica la ruta de acceso al origen y MyInf es el identificador del archivo INF abierto. El parámetro *ListInfHandle* se establece en **null**, lo que indica que la sección para copiar está en MyInf. Mi sección es la sección de MyInf que contiene los archivos que se van a poner en cola para copiarlos.

Las marcas de SP \_ Copy \_ noskip y SP \_ Copy \_ nobrowse se han combinado con un operador OR para indicar que no se deben ofrecer opciones al usuario para omitir o buscar archivos si se producen errores.

 

 



