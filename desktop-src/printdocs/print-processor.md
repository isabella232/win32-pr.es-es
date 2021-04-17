---
description: El administrador de trabajos de impresión supervisa los trabajos de impresión actuales y la impresora de destino para determinar el momento adecuado para imprimir un trabajo.
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: Procesador de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652679"
---
# <a name="print-processor"></a><span data-ttu-id="151ba-103">Procesador de impresión</span><span class="sxs-lookup"><span data-stu-id="151ba-103">Print Processor</span></span>

<span data-ttu-id="151ba-104">El administrador de trabajos de impresión supervisa los trabajos de impresión actuales y la impresora de destino para determinar el momento adecuado para imprimir un trabajo.</span><span class="sxs-lookup"><span data-stu-id="151ba-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="151ba-105">Una vez que el administrador de trabajos de impresión determina que se debe imprimir un trabajo, llama al procesador de impresión.</span><span class="sxs-lookup"><span data-stu-id="151ba-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="151ba-106">El procesador de impresión es un complemento que procesa los datos del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="151ba-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="151ba-107">Utilice las siguientes funciones para trabajar con procesadores de impresión.</span><span class="sxs-lookup"><span data-stu-id="151ba-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="151ba-108">Función</span><span class="sxs-lookup"><span data-stu-id="151ba-108">Function</span></span>                                                           | <span data-ttu-id="151ba-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="151ba-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="151ba-110">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="151ba-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="151ba-111">Instala un procesador de impresión en un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="151ba-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="151ba-112">**DeletePrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="151ba-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="151ba-113">Quita un procesador de impresora de un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="151ba-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="151ba-114">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="151ba-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="151ba-115">Enumera los tipos de datos que admite un procesador de impresión especificado.</span><span class="sxs-lookup"><span data-stu-id="151ba-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="151ba-116">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="151ba-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="151ba-117">Enumera los procesadores de impresión instalados en un servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="151ba-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="151ba-118">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="151ba-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="151ba-119">Recupera la ruta de acceso del procesador de impresión en el servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="151ba-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 



