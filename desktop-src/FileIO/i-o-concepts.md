---
description: Describe los conceptos básicos de e/s.
ms.assetid: 61b286a0-2f0d-48d1-a0b9-bb13f1ea1b0e
title: Conceptos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727ae7f2b34b7938de444a82c9c4dfdf89f52ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688461"
---
# <a name="io-concepts"></a><span data-ttu-id="addbd-103">Conceptos de e/s</span><span class="sxs-lookup"><span data-stu-id="addbd-103">I/O Concepts</span></span>

<span data-ttu-id="addbd-104">En esta sección se describen los siguientes conceptos de e/s.</span><span class="sxs-lookup"><span data-stu-id="addbd-104">The following I/O concepts are described in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="addbd-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="addbd-105">In this section</span></span>



| <span data-ttu-id="addbd-106">Tema</span><span class="sxs-lookup"><span data-stu-id="addbd-106">Topic</span></span>                                                                               | <span data-ttu-id="addbd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="addbd-107">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="addbd-108">Almacenamiento en búfer de archivo</span><span class="sxs-lookup"><span data-stu-id="addbd-108">File Buffering</span></span>](file-buffering.md)<br/>                                     | <span data-ttu-id="addbd-109">Describe las consideraciones para el control de aplicaciones del almacenamiento en búfer de archivos, también conocido como entrada/salida (e/s) de archivo no almacenado en búfer.</span><span class="sxs-lookup"><span data-stu-id="addbd-109">Describes considerations for application control of file buffering, also known as unbuffered file input/output (I/O).</span></span><br/>                                    |
| [<span data-ttu-id="addbd-110">Almacenamiento en caché de archivos</span><span class="sxs-lookup"><span data-stu-id="addbd-110">File Caching</span></span>](file-caching.md)<br/>                                         | <span data-ttu-id="addbd-111">Windows almacena en caché los datos de archivos que se leen de los discos y se escriben en los discos.</span><span class="sxs-lookup"><span data-stu-id="addbd-111">Windows caches file data that is read from disks and written to disks.</span></span><br/>                                                                                   |
| [<span data-ttu-id="addbd-112">E/s sincrónica y asincrónica</span><span class="sxs-lookup"><span data-stu-id="addbd-112">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)<br/> | <span data-ttu-id="addbd-113">Hay dos tipos de sincronización de entrada/salida (e/s): e/s sincrónica y de e/s asincrónica.</span><span class="sxs-lookup"><span data-stu-id="addbd-113">There are two types of input/output (I/O) synchronization: synchronous I/O and asynchronous I/O.</span></span> <span data-ttu-id="addbd-114">La e/s asincrónica también se conoce como e/s superpuesta.</span><span class="sxs-lookup"><span data-stu-id="addbd-114">Asynchronous I/O is also referred to as overlapped I/O.</span></span><br/> |
| [<span data-ttu-id="addbd-115">Cancelar operaciones de e/s pendientes</span><span class="sxs-lookup"><span data-stu-id="addbd-115">Canceling Pending I/O Operations</span></span>](canceling-pending-i-o-operations.md)<br/> | <span data-ttu-id="addbd-116">Permitir a los usuarios cancelar las solicitudes de e/s que son lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="addbd-116">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span><br/>                             |
| [<span data-ttu-id="addbd-117">E/s de alertas</span><span class="sxs-lookup"><span data-stu-id="addbd-117">Alertable I/O</span></span>](alertable-i-o.md)<br/>                                       | <span data-ttu-id="addbd-118">La e/s de alertas es el método por el que los subprocesos de la aplicación procesan las solicitudes de e/s asincrónicas solo cuando se encuentran en un estado de alerta.</span><span class="sxs-lookup"><span data-stu-id="addbd-118">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span><br/>                     |
| [<span data-ttu-id="addbd-119">Puertos de finalización de e/s</span><span class="sxs-lookup"><span data-stu-id="addbd-119">I/O Completion Ports</span></span>](i-o-completion-ports.md)<br/>                         | <span data-ttu-id="addbd-120">Los puertos de finalización de e/s proporcionan un modelo de subprocesos eficaz para procesar varias solicitudes de e/s asincrónicas en un sistema de varios procesadores.</span><span class="sxs-lookup"><span data-stu-id="addbd-120">I/O completion ports provide an efficient threading model for processing multiple asynchronous I/O requests on a multiprocessor system.</span></span><br/>                  |



 

 

 




