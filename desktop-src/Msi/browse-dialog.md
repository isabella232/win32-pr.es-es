---
description: Un cuadro de diálogo examinar permite al usuario seleccionar un directorio. El directorio no tiene que existir y se puede crear con este control.
ms.assetid: 35b991b8-d291-44ef-b1c0-8128bed3c3c8
title: Cuadro de diálogo examinar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f6d3c3d95caec7e9a439621f6741b0dceb0c83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423876"
---
# <a name="browse-dialog"></a><span data-ttu-id="91159-104">Cuadro de diálogo examinar</span><span class="sxs-lookup"><span data-stu-id="91159-104">Browse Dialog</span></span>

<span data-ttu-id="91159-105">Un cuadro de diálogo examinar permite al usuario seleccionar un directorio.</span><span class="sxs-lookup"><span data-stu-id="91159-105">A Browse dialog box enables the user to select a directory.</span></span> <span data-ttu-id="91159-106">El directorio no tiene que existir y se puede crear con este control.</span><span class="sxs-lookup"><span data-stu-id="91159-106">The directory does not have to exist and may be created by using this control.</span></span>

<span data-ttu-id="91159-107">Este tipo de cuadro de diálogo contiene normalmente los tres controles siguientes.</span><span class="sxs-lookup"><span data-stu-id="91159-107">This type of dialog box commonly contains the following three controls.</span></span> <span data-ttu-id="91159-108">Estos controles se conectan a la misma propiedad.</span><span class="sxs-lookup"><span data-stu-id="91159-108">These controls are connected to the same property.</span></span> <span data-ttu-id="91159-109">Esa propiedad es la ruta de acceso que se selecciona.</span><span class="sxs-lookup"><span data-stu-id="91159-109">That property is the path being selected.</span></span>

-   <span data-ttu-id="91159-110">Un [control PathEdit](pathedit-control.md) para seleccionar la sección tail del trazado.</span><span class="sxs-lookup"><span data-stu-id="91159-110">A [PathEdit control](pathedit-control.md) to select the tail section of the path.</span></span> <span data-ttu-id="91159-111">Este control no puede perder el foco si la cola introducida no es válida en el volumen actual.</span><span class="sxs-lookup"><span data-stu-id="91159-111">This control cannot lose focus if the entered tail is not valid on the present volume.</span></span>
-   <span data-ttu-id="91159-112">Un [control DirectoryCombo](directorycombo-control.md) para mostrar la ruta de acceso seleccionada actualmente que muestra el control PathEdit.</span><span class="sxs-lookup"><span data-stu-id="91159-112">A [DirectoryCombo control](directorycombo-control.md) to show the presently selected path that is displayed by the PathEdit control.</span></span> <span data-ttu-id="91159-113">Este control no muestra el último segmento de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="91159-113">This control does not show the last segment of the path.</span></span>
-   <span data-ttu-id="91159-114">Un [control DirectoryList](directorylist-control.md) para mostrar las carpetas debajo del directorio mostrado actualmente por el DirectoryCombo.</span><span class="sxs-lookup"><span data-stu-id="91159-114">A [DirectoryList control](directorylist-control.md) to show the folders below the directory currently displayed by the DirectoryCombo.</span></span> <span data-ttu-id="91159-115">Esto también puede mostrar una carpeta que aún no se ha creado.</span><span class="sxs-lookup"><span data-stu-id="91159-115">This can also show a folder that is not yet created.</span></span>

<span data-ttu-id="91159-116">Un cuadro de diálogo de exploración también contiene normalmente un [control DirectoryCombo](directorycombo-control.md) que especifica los tipos de volúmenes que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="91159-116">A Browse dialog box also usually contains a [DirectoryCombo control](directorycombo-control.md) that specifies the volume types to display.</span></span> <span data-ttu-id="91159-117">Es habitual que todos los tipos de volúmenes se muestren en un cuadro de diálogo de exploración.</span><span class="sxs-lookup"><span data-stu-id="91159-117">It is common for all volume types to be displayed on a Browse dialog box.</span></span>

<span data-ttu-id="91159-118">Los cuadros de diálogo de exploración suelen contener tres [controles de pulsador](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="91159-118">Browse dialog boxes commonly contain three [PushButton controls](pushbutton-control.md).</span></span> <span data-ttu-id="91159-119">Estos botones están vinculados a sus respectivas ControlEvents en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="91159-119">These buttons are linked to their respective ControlEvents in [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="91159-120">Estos botones se utilizan para activar las siguientes opciones de control.</span><span class="sxs-lookup"><span data-stu-id="91159-120">These buttons are used for activating the following control options.</span></span>



| <span data-ttu-id="91159-121">Opción de control</span><span class="sxs-lookup"><span data-stu-id="91159-121">Control option</span></span> | <span data-ttu-id="91159-122">ControlEvent</span><span class="sxs-lookup"><span data-stu-id="91159-122">ControlEvent</span></span>                                            |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="91159-123">Subir un nivel</span><span class="sxs-lookup"><span data-stu-id="91159-123">Up One Level</span></span>   | [<span data-ttu-id="91159-124">DirectoryListUp</span><span class="sxs-lookup"><span data-stu-id="91159-124">DirectoryListUp</span></span>](directorylistup-controlevent.md)     |
| <span data-ttu-id="91159-125">Nueva carpeta</span><span class="sxs-lookup"><span data-stu-id="91159-125">New Folder</span></span>     | [<span data-ttu-id="91159-126">DirectoryListNew</span><span class="sxs-lookup"><span data-stu-id="91159-126">DirectoryListNew</span></span>](directorylistnew-controlevent.md)   |
| <span data-ttu-id="91159-127">Abrir</span><span class="sxs-lookup"><span data-stu-id="91159-127">Open</span></span>           | [<span data-ttu-id="91159-128">DirectoryListOpen</span><span class="sxs-lookup"><span data-stu-id="91159-128">DirectoryListOpen</span></span>](directorylistopen-controlevent.md) |



 

<span data-ttu-id="91159-129">Para que la opción nueva carpeta funcione con un nombre de carpeta no predeterminado, se debe especificar la ruta de acceso de la nueva carpeta en la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="91159-129">For the New Folder option to work with a non-default folder name, the new folder's path must be specified in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="91159-130">La cadena de ruta de acceso debe usar el \| formato de nombre de archivo largo de nombre corto de archivo para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="91159-130">The path string should use the "short file name\|long file name" form for the file name.</span></span> <span data-ttu-id="91159-131">Por ejemplo, use un nombre de archivo como "mi Prod ~ 1 \| My aventuras Product".</span><span class="sxs-lookup"><span data-stu-id="91159-131">For example, use a file name such as "MyProd~1\|My Fabulous Product".</span></span> <span data-ttu-id="91159-132">Vea el tipo de datos de la columna [filename](filename.md) para obtener más información sobre el formato de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="91159-132">See the [Filename](filename.md) column data type for more information about the file name format.</span></span> <span data-ttu-id="91159-133">Si la ruta de acceso no está presente en la tabla UIText, o si está establecida en un valor no válido, se establece en un valor de "FLDR \| nueva carpeta" de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="91159-133">If the path is not present in the UIText table, or if it is set to an invalid value, then it is set to a value of "Fldr\|New Folder" by default.</span></span> <span data-ttu-id="91159-134">Se puede omitir el botón **nueva carpeta** si el cuadro de diálogo solo necesita buscar carpetas existentes.</span><span class="sxs-lookup"><span data-stu-id="91159-134">The **New Folder** button can be omitted if the dialog box only need to search for existing folders.</span></span>

 

 



