---
description: Metaarchivos de Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metaarchivos de Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984974"
---
# <a name="enhanced-format-metafiles"></a><span data-ttu-id="d0238-103">Metaarchivos de Enhanced-Format</span><span class="sxs-lookup"><span data-stu-id="d0238-103">Enhanced-Format Metafiles</span></span>

<span data-ttu-id="d0238-104">El *metarchivo con formato mejorado* consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="d0238-104">The *enhanced-format metafile* consists of the following elements:</span></span>

-   <span data-ttu-id="d0238-105">Un encabezado</span><span class="sxs-lookup"><span data-stu-id="d0238-105">A header</span></span>
-   <span data-ttu-id="d0238-106">Una tabla de identificadores para objetos GDI</span><span class="sxs-lookup"><span data-stu-id="d0238-106">A table of handles to GDI objects</span></span>
-   <span data-ttu-id="d0238-107">Una paleta privada</span><span class="sxs-lookup"><span data-stu-id="d0238-107">A private palette</span></span>
-   <span data-ttu-id="d0238-108">Matriz de registros de metarchivo</span><span class="sxs-lookup"><span data-stu-id="d0238-108">An array of metafile records</span></span>

<span data-ttu-id="d0238-109">Los metaarchivos mejorados proporcionan una verdadera independencia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d0238-109">Enhanced metafiles provide true device independence.</span></span> <span data-ttu-id="d0238-110">Puede pensar en la imagen almacenada en un metarchivo mejorado como una "instantánea" de la pantalla de vídeo tomada en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="d0238-110">You can think of the picture stored in an enhanced metafile as a "snapshot" of the video display taken at a particular moment.</span></span> <span data-ttu-id="d0238-111">Esta "instantánea" mantiene sus dimensiones, independientemente de dónde aparezca en una impresora, un trazador, el escritorio o el área cliente de cualquier aplicación.</span><span class="sxs-lookup"><span data-stu-id="d0238-111">This "snapshot" maintains its dimensions no matter where it appears on a printer, a plotter, the desktop, or in the client area of any application.</span></span>

<span data-ttu-id="d0238-112">Puede usar los metaarchivos mejorados para almacenar una imagen creada con las funciones GDI (incluidas las nuevas funciones de trazado y transformación).</span><span class="sxs-lookup"><span data-stu-id="d0238-112">You can use enhanced metafiles to store a picture created by using the GDI functions (including new path and transformation functions).</span></span> <span data-ttu-id="d0238-113">Dado que el formato de metarchivo mejorado está normalizado, las imágenes que se almacenan en este formato se pueden copiar de una aplicación a otra; y, dado que las imágenes son realmente independientes del dispositivo, se garantiza que mantengan su forma y proporción en cualquier dispositivo de salida.</span><span class="sxs-lookup"><span data-stu-id="d0238-113">Because the enhanced metafile format is standardized, pictures that are stored in this format can be copied from one application to another; and, because the pictures are truly device independent, they are guaranteed to maintain their shape and proportion on any output device.</span></span>

-   [<span data-ttu-id="d0238-114">Registros de metarchivos mejorados</span><span class="sxs-lookup"><span data-stu-id="d0238-114">Enhanced Metafile Records</span></span>](enhanced-metafile-records.md)
-   [<span data-ttu-id="d0238-115">Creación mejorada de metarchivos</span><span class="sxs-lookup"><span data-stu-id="d0238-115">Enhanced Metafile Creation</span></span>](enhanced-metafile-creation.md)
-   [<span data-ttu-id="d0238-116">Operaciones de metarchivo mejoradas</span><span class="sxs-lookup"><span data-stu-id="d0238-116">Enhanced Metafile Operations</span></span>](enhanced-metafile-operations.md)

 

 



