---
description: Además de poner en cola las operaciones de archivo individualmente, también puede poner en cola todos los archivos enumerados en una sección INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Poner en cola una sección de INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546395"
---
# <a name="queuing-an-inf-section"></a>Poner en cola una sección de INF

Además de poner en cola las operaciones de archivo individualmente, también puede poner en cola todos los archivos enumerados en una sección INF.

Puede poner en cola todos los archivos enumerados en una sección de **archivos de copia** de un archivo INF llamando a [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Para que esta función se realice correctamente, la sección **Copy files** debe tener el formato adecuado y el archivo INF, o uno de sus archivos anexados, debe contener las secciones **SourceDisksFiles** y **SourceDisksNames** .

Del mismo modo, si desea eliminar todos los archivos especificados en una sección **eliminar archivos** de un archivo INF, puede llamar a [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Para cambiar el nombre de todos los archivos de una sección **Rename files** de un archivo INF, use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



