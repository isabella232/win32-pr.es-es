---
description: Las funciones de configuración incluyen la funcionalidad de cola de archivos.
ms.assetid: 628850ab-eb66-4b60-9298-1a44a7f6a390
title: Colas de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7177e0bb267167ce5b37cf5213ea942c972ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002325"
---
# <a name="file-queues"></a><span data-ttu-id="1bd77-103">Colas de archivos</span><span class="sxs-lookup"><span data-stu-id="1bd77-103">File Queues</span></span>

<span data-ttu-id="1bd77-104">Las funciones de configuración incluyen la funcionalidad de cola de archivos.</span><span class="sxs-lookup"><span data-stu-id="1bd77-104">The setup functions include file queue functionality.</span></span> <span data-ttu-id="1bd77-105">Una cola de archivos es una lista de operaciones de copia, cambio de nombre y eliminación de archivos.</span><span class="sxs-lookup"><span data-stu-id="1bd77-105">A file queue is a list of file copying, renaming, and deletion operations.</span></span> <span data-ttu-id="1bd77-106">Estas operaciones se pueden enviar a la cola en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="1bd77-106">These operations can be sent to the queue in any order.</span></span> <span data-ttu-id="1bd77-107">Cuando se confirma la cola, estas operaciones se procesan como un lote, en orden del tipo de operación.</span><span class="sxs-lookup"><span data-stu-id="1bd77-107">When the queue is committed, these operations are processed as a batch, in order of the operation type.</span></span>

<span data-ttu-id="1bd77-108">En las secciones siguientes se explica qué es una cola y cómo utilizarla al crear una aplicación de instalación.</span><span class="sxs-lookup"><span data-stu-id="1bd77-108">The following sections explain what a queue is and how to use it when creating a setup application.</span></span> <span data-ttu-id="1bd77-109">También se describe el orden en el que se procesan las operaciones de archivo en cola a medida que se confirman las colas y las notificaciones que la cola envía a una rutina de devolución de llamada en cada fase.</span><span class="sxs-lookup"><span data-stu-id="1bd77-109">Also discussed is the order in which the enqueued file operations are processed as the queue commits and what notifications the queue sends to a callback routine at each stage.</span></span>

-   [<span data-ttu-id="1bd77-110">Acerca de las colas de archivos</span><span class="sxs-lookup"><span data-stu-id="1bd77-110">About File Queues</span></span>](about-file-queues.md)
-   [<span data-ttu-id="1bd77-111">Usar colas de archivos</span><span class="sxs-lookup"><span data-stu-id="1bd77-111">Using File Queues</span></span>](using-file-queues.md)
-   [<span data-ttu-id="1bd77-112">Referencia de cola de archivos</span><span class="sxs-lookup"><span data-stu-id="1bd77-112">File Queue Reference</span></span>](file-queue-reference.md)

 

 



