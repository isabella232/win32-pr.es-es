---
description: 'Más información sobre: macros de API de archivo. cab'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros de API de archivo. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538302"
---
# <a name="cabinet-api-macros"></a><span data-ttu-id="5c498-103">Macros de API de archivo. cab</span><span class="sxs-lookup"><span data-stu-id="5c498-103">Cabinet API Macros</span></span>

<span data-ttu-id="5c498-104">En esta sección se detallan las macros usadas por la API del archivo. cab:</span><span class="sxs-lookup"><span data-stu-id="5c498-104">This section details the macros used by the Cabinet API:</span></span>

## <a name="fci-macros"></a><span data-ttu-id="5c498-105">Macros FCI</span><span class="sxs-lookup"><span data-stu-id="5c498-105">FCI Macros</span></span>

<span data-ttu-id="5c498-106">Las siguientes macros las usa FCI:</span><span class="sxs-lookup"><span data-stu-id="5c498-106">The following macros are used by FCI:</span></span>



| <span data-ttu-id="5c498-107">Macro</span><span class="sxs-lookup"><span data-stu-id="5c498-107">Macro</span></span>                                              | <span data-ttu-id="5c498-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c498-108">Description</span></span>                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c498-109">**FNFCIALLOC**</span><span class="sxs-lookup"><span data-stu-id="5c498-109">**FNFCIALLOC**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | <span data-ttu-id="5c498-110">Se usa para asignar memoria en un contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="5c498-110">Used to allocate memory in an FCI context.</span></span><br/>                                          |
| [<span data-ttu-id="5c498-111">**FNFCICLOSE**</span><span class="sxs-lookup"><span data-stu-id="5c498-111">**FNFCICLOSE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | <span data-ttu-id="5c498-112">Se utiliza para cerrar un archivo.</span><span class="sxs-lookup"><span data-stu-id="5c498-112">Used to close a file.</span></span><br/>                                                               |
| [<span data-ttu-id="5c498-113">**FNFCIDELETE**</span><span class="sxs-lookup"><span data-stu-id="5c498-113">**FNFCIDELETE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | <span data-ttu-id="5c498-114">Se usa para eliminar un archivo.</span><span class="sxs-lookup"><span data-stu-id="5c498-114">Used to delete a file.</span></span><br/>                                                              |
| [<span data-ttu-id="5c498-115">**FNFCIFILEPLACED**</span><span class="sxs-lookup"><span data-stu-id="5c498-115">**FNFCIFILEPLACED**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | <span data-ttu-id="5c498-116">Se usa para notificar cuando se coloca un archivo en el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="5c498-116">Used to notify when a file is placed in the cabinet.</span></span><br/>                                |
| [<span data-ttu-id="5c498-117">**FNFCIFREE**</span><span class="sxs-lookup"><span data-stu-id="5c498-117">**FNFCIFREE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | <span data-ttu-id="5c498-118">Se usa para liberar memoria asignada previamente en un contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="5c498-118">Used to free previously allocated memory in an FCI context.</span></span><br/>                         |
| [<span data-ttu-id="5c498-119">**FNFCIGETNEXTCABINET**</span><span class="sxs-lookup"><span data-stu-id="5c498-119">**FNFCIGETNEXTCABINET**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | <span data-ttu-id="5c498-120">Se usa para solicitar información para el siguiente archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="5c498-120">Used to request information for the next cabinet.</span></span><br/>                                   |
| [<span data-ttu-id="5c498-121">**FNFCIGETOPENINFO**</span><span class="sxs-lookup"><span data-stu-id="5c498-121">**FNFCIGETOPENINFO**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | <span data-ttu-id="5c498-122">Se usa para abrir un archivo y recuperar la fecha, la hora y los atributos del archivo.</span><span class="sxs-lookup"><span data-stu-id="5c498-122">Used to open a file and retrieve file date, time, and attributes.</span></span><br/>                   |
| [<span data-ttu-id="5c498-123">**FNFCIGETTEMPFILE**</span><span class="sxs-lookup"><span data-stu-id="5c498-123">**FNFCIGETTEMPFILE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | <span data-ttu-id="5c498-124">Se utiliza para obtener un nombre de archivo temporal.</span><span class="sxs-lookup"><span data-stu-id="5c498-124">Used to obtain a temporary file name.</span></span><br/>                                               |
| [<span data-ttu-id="5c498-125">**FNFCIOPEN**</span><span class="sxs-lookup"><span data-stu-id="5c498-125">**FNFCIOPEN**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | <span data-ttu-id="5c498-126">Se usa para abrir un archivo en un contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="5c498-126">Used to open a file in an FCI context.</span></span><br/>                                              |
| [<span data-ttu-id="5c498-127">**FNFCIREAD**</span><span class="sxs-lookup"><span data-stu-id="5c498-127">**FNFCIREAD**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciread)                     | <span data-ttu-id="5c498-128">Se utiliza para leer datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="5c498-128">Used to read data from a file.</span></span><br/>                                                      |
| [<span data-ttu-id="5c498-129">**FNFCISEEK**</span><span class="sxs-lookup"><span data-stu-id="5c498-129">**FNFCISEEK**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | <span data-ttu-id="5c498-130">Se usa para trasladar un puntero de archivo a una ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="5c498-130">Used to move a file pointer to a specified location.</span></span><br/>                                |
| [<span data-ttu-id="5c498-131">**FNFCISTATUS**</span><span class="sxs-lookup"><span data-stu-id="5c498-131">**FNFCISTATUS**</span></span>](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | <span data-ttu-id="5c498-132">Se usa para actualizar el usuario.</span><span class="sxs-lookup"><span data-stu-id="5c498-132">Used to update the user.</span></span><br/>                                                            |
| [<span data-ttu-id="5c498-133">**FNFCIWRITE**</span><span class="sxs-lookup"><span data-stu-id="5c498-133">**FNFCIWRITE**</span></span>](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | <span data-ttu-id="5c498-134">Se utiliza para escribir datos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="5c498-134">Used to write data to a file.</span></span><br/>                                                       |
| [<span data-ttu-id="5c498-135">**TCOMPfromLZXWindow**</span><span class="sxs-lookup"><span data-stu-id="5c498-135">**TCOMPfromLZXWindow**</span></span>](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | <span data-ttu-id="5c498-136">Convierte el tamaño de Windows en un valor de LXZ TCOMP para [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span><span class="sxs-lookup"><span data-stu-id="5c498-136">Converts windows size into an LXZ TCOMP value for [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).</span></span><br/> |



 

## <a name="fdi-macros"></a><span data-ttu-id="5c498-137">Macros FDI</span><span class="sxs-lookup"><span data-stu-id="5c498-137">FDI Macros</span></span>

<span data-ttu-id="5c498-138">FDI utiliza las siguientes macros:</span><span class="sxs-lookup"><span data-stu-id="5c498-138">The following macros are used by FDI:</span></span>



| <span data-ttu-id="5c498-139">Macro</span><span class="sxs-lookup"><span data-stu-id="5c498-139">Macro</span></span>                              | <span data-ttu-id="5c498-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c498-140">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c498-141">**FNALLOC**</span><span class="sxs-lookup"><span data-stu-id="5c498-141">**FNALLOC**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | <span data-ttu-id="5c498-142">Se usa para asignar memoria en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-142">Used to allocate memory in an FDI context.</span></span><br/>                               |
| [<span data-ttu-id="5c498-143">**FNCLOSE**</span><span class="sxs-lookup"><span data-stu-id="5c498-143">**FNCLOSE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnclose)         | <span data-ttu-id="5c498-144">Se utiliza para cerrar un archivo en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-144">Used to close a file in an FDI context.</span></span><br/>                                  |
| [<span data-ttu-id="5c498-145">**FNFDINOTIFY**</span><span class="sxs-lookup"><span data-stu-id="5c498-145">**FNFDINOTIFY**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | <span data-ttu-id="5c498-146">Se utiliza para actualizar la aplicación en el estado del descodificador.</span><span class="sxs-lookup"><span data-stu-id="5c498-146">Used to update the application on the status of the decoder.</span></span><br/>             |
| [<span data-ttu-id="5c498-147">**FNFREE**</span><span class="sxs-lookup"><span data-stu-id="5c498-147">**FNFREE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnfree)           | <span data-ttu-id="5c498-148">Se usa para liberar memoria asignada previamente en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-148">Used to free previously allocated memory in an FDI context.</span></span><br/>              |
| [<span data-ttu-id="5c498-149">**FNOPEN**</span><span class="sxs-lookup"><span data-stu-id="5c498-149">**FNOPEN**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnopen)           | <span data-ttu-id="5c498-150">Se usa para abrir un archivo en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-150">Used to open a file in an FDI context.</span></span><br/>                                   |
| [<span data-ttu-id="5c498-151">**FNREAD**</span><span class="sxs-lookup"><span data-stu-id="5c498-151">**FNREAD**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnread)           | <span data-ttu-id="5c498-152">Se utiliza para leer datos de un archivo en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-152">Used to read data from a file in an FDI context.</span></span><br/>                         |
| [<span data-ttu-id="5c498-153">**FNSEEK**</span><span class="sxs-lookup"><span data-stu-id="5c498-153">**FNSEEK**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnseek)           | <span data-ttu-id="5c498-154">Se usa para trasladar un puntero de archivo a la ubicación especificada en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-154">Used to move a file pointer to the specified location in an FDI context.</span></span><br/> |
| [<span data-ttu-id="5c498-155">**FNWRITE**</span><span class="sxs-lookup"><span data-stu-id="5c498-155">**FNWRITE**</span></span>](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | <span data-ttu-id="5c498-156">Se utiliza para escribir datos en un archivo en un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="5c498-156">Used to write data to a file in an FDI context.</span></span><br/>                          |



 

## <a name="related-topics"></a><span data-ttu-id="5c498-157">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c498-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c498-158">Referencia de la API de contenedor</span><span class="sxs-lookup"><span data-stu-id="5c498-158">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="5c498-159">Uso de la API de archivo. cab</span><span class="sxs-lookup"><span data-stu-id="5c498-159">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




