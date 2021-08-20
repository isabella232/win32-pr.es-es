---
description: Además de poner en cola las operaciones de archivos individualmente, también puede poner en cola todos los archivos enumerados en una sección INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Cola de una sección INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c419f23fe48057eec382c83b4da5e219114c186a9b7bc07c04fc5d7088b17e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964962"
---
# <a name="queuing-an-inf-section"></a>Cola de una sección INF

Además de poner en cola las operaciones de archivos individualmente, también puede poner en cola todos los archivos enumerados en una sección INF.

Puede poner en cola todos los archivos enumerados en una **sección Copiar archivos** de un archivo INF llamando a [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona). Para que esta función  se haga correctamente, la sección Copiar archivos debe tener el formato adecuado y el archivo INF, o uno de sus archivos anexados, debe contener las secciones **SourceDisksFiles** y **SourceDisksNames.**

De forma similar, si desea eliminar todos los archivos especificados en una sección Eliminar archivos de un archivo INF, puede llamar **a** [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona). Para cambiar el nombre de todos los archivos de una **sección Cambiar** nombre de archivos de un archivo INF, use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).

 

 



