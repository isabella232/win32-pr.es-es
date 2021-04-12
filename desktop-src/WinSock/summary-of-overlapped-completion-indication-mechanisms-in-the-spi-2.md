---
description: Resumen de los mecanismos de indicación de finalización superpuestos en el SPI de Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Resumen de los mecanismos de indicación de finalización superpuestos en el SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154245"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a><span data-ttu-id="a2c3d-103">Resumen de los mecanismos de indicación de finalización superpuestos en el SPI</span><span class="sxs-lookup"><span data-stu-id="a2c3d-103">Summary of Overlapped Completion Indication Mechanisms in the SPI</span></span>

<span data-ttu-id="a2c3d-104">En la tabla siguiente se resume la semántica de finalización de un socket superpuesto, que muestra la combinación de *lpOverlapped*, **hEvent** y *lpCompletionRoutine*.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-104">The following table summarizes the completion semantics for an overlapped socket, showing the various combination of *lpOverlapped*, **hEvent**, and *lpCompletionRoutine*.</span></span>



| <span data-ttu-id="a2c3d-105">*lpOverlapped*</span><span class="sxs-lookup"><span data-stu-id="a2c3d-105">*lpOverlapped*</span></span> | <span data-ttu-id="a2c3d-106">**hEvent**</span><span class="sxs-lookup"><span data-stu-id="a2c3d-106">**hEvent**</span></span>     | <span data-ttu-id="a2c3d-107">*lpCompletionRoutine*</span><span class="sxs-lookup"><span data-stu-id="a2c3d-107">*lpCompletionRoutine*</span></span> | <span data-ttu-id="a2c3d-108">Indicación de finalización</span><span class="sxs-lookup"><span data-stu-id="a2c3d-108">Completion indication</span></span>                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c3d-109">NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-109">NULL</span></span>           | <span data-ttu-id="a2c3d-110">No aplicable</span><span class="sxs-lookup"><span data-stu-id="a2c3d-110">Not applicable</span></span> | <span data-ttu-id="a2c3d-111">Omitido</span><span class="sxs-lookup"><span data-stu-id="a2c3d-111">Ignored</span></span>               | <span data-ttu-id="a2c3d-112">La operación se completa de forma sincrónica, es decir, se comporta como si fuera un socket nonoverlapped.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-112">Operation completes synchronously, that is, it behaves as if it were a nonoverlapped socket.</span></span>                                                                                                                                 |
| <span data-ttu-id="a2c3d-113">no NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-113">not NULL</span></span>       | <span data-ttu-id="a2c3d-114">NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-114">NULL</span></span>           | <span data-ttu-id="a2c3d-115">NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-115">NULL</span></span>                  | <span data-ttu-id="a2c3d-116">La operación se completa superpuesta, pero no hay ningún mecanismo de finalización compatible con Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-116">Operation completes overlapped, but there is no Windows Sockets 2-supported completion mechanism.</span></span> <span data-ttu-id="a2c3d-117">En este caso, se puede usar el mecanismo de puerto de finalización (si se admite); de lo contrario, no habrá ninguna notificación de finalización.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-117">The completion port mechanism (if supported) may be used in this case, otherwise there will be no completion notification.</span></span> |
| <span data-ttu-id="a2c3d-118">no NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-118">not NULL</span></span>       | <span data-ttu-id="a2c3d-119">no NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-119">not NULL</span></span>       | <span data-ttu-id="a2c3d-120">NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-120">NULL</span></span>                  | <span data-ttu-id="a2c3d-121">La operación se completa y se notifica mediante un objeto de evento de señalización.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-121">Operation completes overlapped, notification by signaling event object.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a2c3d-122">no NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-122">not NULL</span></span>       | <span data-ttu-id="a2c3d-123">Omitido</span><span class="sxs-lookup"><span data-stu-id="a2c3d-123">Ignored</span></span>        | <span data-ttu-id="a2c3d-124">no NULL</span><span class="sxs-lookup"><span data-stu-id="a2c3d-124">not NULL</span></span>              | <span data-ttu-id="a2c3d-125">La operación se completa y se notifica mediante la programación de la rutina de finalización.</span><span class="sxs-lookup"><span data-stu-id="a2c3d-125">Operation completes overlapped, notification by scheduling completion routine.</span></span>                                                                                                                                               |



 

 

 



