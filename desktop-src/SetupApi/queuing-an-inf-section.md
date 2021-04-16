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
# <a name="queuing-an-inf-section"></a><span data-ttu-id="97fa0-103">Poner en cola una sección de INF</span><span class="sxs-lookup"><span data-stu-id="97fa0-103">Queuing an INF Section</span></span>

<span data-ttu-id="97fa0-104">Además de poner en cola las operaciones de archivo individualmente, también puede poner en cola todos los archivos enumerados en una sección INF.</span><span class="sxs-lookup"><span data-stu-id="97fa0-104">In addition to queuing file operations individually, you can also queue all the files listed in an INF section.</span></span>

<span data-ttu-id="97fa0-105">Puede poner en cola todos los archivos enumerados en una sección de **archivos de copia** de un archivo INF llamando a [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span><span class="sxs-lookup"><span data-stu-id="97fa0-105">You can queue all the files listed in a **Copy Files** section of an INF file by calling [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span></span> <span data-ttu-id="97fa0-106">Para que esta función se realice correctamente, la sección **Copy files** debe tener el formato adecuado y el archivo INF, o uno de sus archivos anexados, debe contener las secciones **SourceDisksFiles** y **SourceDisksNames** .</span><span class="sxs-lookup"><span data-stu-id="97fa0-106">For this function to be successful, the **Copy Files** section must be in the proper format and the INF file, or one of its appended files, must contain the **SourceDisksFiles** and **SourceDisksNames** sections.</span></span>

<span data-ttu-id="97fa0-107">Del mismo modo, si desea eliminar todos los archivos especificados en una sección **eliminar archivos** de un archivo INF, puede llamar a [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span><span class="sxs-lookup"><span data-stu-id="97fa0-107">Similarly, if you want to delete all the files specified in a **Delete Files** section of an INF file, you can call [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span></span> <span data-ttu-id="97fa0-108">Para cambiar el nombre de todos los archivos de una sección **Rename files** de un archivo INF, use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="97fa0-108">To rename all the files in a **Rename Files** section of an INF file use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span></span>

 

 



