---
description: Internamente, un metarchivo es una matriz de estructuras de longitud variable llamadas registros de metarchivo.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: Acerca de los metaarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811347"
---
# <a name="about-metafiles"></a><span data-ttu-id="6c7a8-103">Acerca de los metaarchivos</span><span class="sxs-lookup"><span data-stu-id="6c7a8-103">About Metafiles</span></span>

<span data-ttu-id="6c7a8-104">Internamente, un metarchivo es una matriz de estructuras de longitud variable llamadas *registros de metarchivo*.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-104">Internally, a metafile is an array of variable-length structures called *metafile records*.</span></span> <span data-ttu-id="6c7a8-105">Los primeros registros del metarchivo especifican información general, como la resolución del dispositivo en el que se creó la imagen, las dimensiones de la imagen, etc.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-105">The first records in the metafile specify general information such as the resolution of the device on which the picture was created, the dimensions of the picture, and so on.</span></span> <span data-ttu-id="6c7a8-106">Los registros restantes, que constituyen la mayor parte de los metarchivos, corresponden a las funciones de la interfaz de dispositivo gráfico (GDI) necesarias para dibujar la imagen.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-106">The remaining records, which constitute the bulk of any metafile, correspond to the graphics device interface (GDI) functions required to draw the picture.</span></span> <span data-ttu-id="6c7a8-107">Estos registros se almacenan en el metarchivo una vez que se crea un contexto de dispositivo de metarchivo especial.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-107">These records are stored in the metafile after a special metafile device context is created.</span></span> <span data-ttu-id="6c7a8-108">Este contexto de dispositivo de metarchivo se utiliza para todas las operaciones de dibujo necesarias para crear la imagen.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-108">This metafile device context is then used for all drawing operations required to create the picture.</span></span> <span data-ttu-id="6c7a8-109">Cuando el sistema procesa una función GDI asociada a un DC de metarchivo, convierte la función en los datos adecuados y almacena estos datos en un registro anexado al metarchivo.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-109">When the system processes a GDI function associated with a metafile DC, it converts the function into the appropriate data and stores this data in a record appended to the metafile.</span></span>

<span data-ttu-id="6c7a8-110">Una vez completada una imagen y almacenada en el metarchivo el último registro, puede pasar el metarchivo a otra aplicación:</span><span class="sxs-lookup"><span data-stu-id="6c7a8-110">After a picture is complete and the last record is stored in the metafile, you can pass the metafile to another application by:</span></span>

-   <span data-ttu-id="6c7a8-111">Usar el portapapeles</span><span class="sxs-lookup"><span data-stu-id="6c7a8-111">Using the clipboard</span></span>
-   <span data-ttu-id="6c7a8-112">Incrustarlo en otro archivo</span><span class="sxs-lookup"><span data-stu-id="6c7a8-112">Embedding it within another file</span></span>
-   <span data-ttu-id="6c7a8-113">Almacenar en disco</span><span class="sxs-lookup"><span data-stu-id="6c7a8-113">Storing it on disk</span></span>
-   <span data-ttu-id="6c7a8-114">Reproducción repetida</span><span class="sxs-lookup"><span data-stu-id="6c7a8-114">Playing it repeatedly</span></span>

<span data-ttu-id="6c7a8-115">Se *reproduce* un metarchivo cuando sus registros se convierten en comandos de dispositivo y se procesan mediante el dispositivo adecuado.</span><span class="sxs-lookup"><span data-stu-id="6c7a8-115">A metafile is *played* when its records are converted to device commands and processed by the appropriate device.</span></span>

<span data-ttu-id="6c7a8-116">Hay dos tipos de metaarchivos:</span><span class="sxs-lookup"><span data-stu-id="6c7a8-116">There are two types of metafiles:</span></span>

-   [<span data-ttu-id="6c7a8-117">Metaarchivos con formato mejorado</span><span class="sxs-lookup"><span data-stu-id="6c7a8-117">Enhanced-format metafiles</span></span>](enhanced-format-metafiles.md)
-   [<span data-ttu-id="6c7a8-118">Metaarchivos con formato de Windows</span><span class="sxs-lookup"><span data-stu-id="6c7a8-118">Windows-format metafiles</span></span>](windows-format-metafiles.md)

 

 



