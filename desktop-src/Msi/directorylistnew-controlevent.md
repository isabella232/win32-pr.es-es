---
description: Este evento notifica al control DirectoryList que se debe crear una nueva carpeta; crea la nueva carpeta y selecciona el campo de nombre de la carpeta para su edición.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670000"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="54062-103">DirectoryListNew ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="54062-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="54062-104">Este evento notifica al [control DirectoryList](directorylist-control.md) que se debe crear una nueva carpeta; crea la nueva carpeta y selecciona el campo de nombre de la carpeta para su edición.</span><span class="sxs-lookup"><span data-stu-id="54062-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="54062-105">El nombre predeterminado de la nueva carpeta se puede crear en la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="54062-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="54062-106">Escriba "NuevaCarpeta" en la columna de clave.</span><span class="sxs-lookup"><span data-stu-id="54062-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="54062-107">Escriba el valor del nombre predeterminado de la nueva carpeta en la columna de texto.</span><span class="sxs-lookup"><span data-stu-id="54062-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="54062-108">Este valor debe tener el formato de un tipo de datos de columna de [nombre de archivo](filename.md) y usar la sintaxis de SFN \| LFN.</span><span class="sxs-lookup"><span data-stu-id="54062-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="54062-109">Si este valor no se encuentra en la tabla UIText o es un valor no válido, el instalador usa un valor predeterminado de "FLDR \| nueva carpeta".</span><span class="sxs-lookup"><span data-stu-id="54062-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="54062-110">Para obtener información relacionada, vea [cuadro de diálogo examinar](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="54062-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="54062-111">Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento.</span><span class="sxs-lookup"><span data-stu-id="54062-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="54062-112">El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="54062-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="54062-113">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="54062-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="54062-114">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="54062-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="54062-115">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="54062-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="54062-116">Tenga en cuenta que si se vuelve a llamar a este ControlEvent, cuando ya existe una nueva carpeta, no se creará una segunda carpeta nueva.</span><span class="sxs-lookup"><span data-stu-id="54062-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="54062-117">En este caso, al llamar a DirectoryListNew se selecciona el nombre de la nueva carpeta existente para su edición.</span><span class="sxs-lookup"><span data-stu-id="54062-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="54062-118">Publicado por</span><span class="sxs-lookup"><span data-stu-id="54062-118">Published By</span></span>

[<span data-ttu-id="54062-119">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="54062-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="54062-120">Argumento</span><span class="sxs-lookup"><span data-stu-id="54062-120">Argument</span></span>

<span data-ttu-id="54062-121">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="54062-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="54062-122">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="54062-122">Action on Subscribers</span></span>

<span data-ttu-id="54062-123">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="54062-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="54062-124">Uso típico</span><span class="sxs-lookup"><span data-stu-id="54062-124">Typical Use</span></span>

<span data-ttu-id="54062-125">Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el DirectoryList se usa para desencadenar la creación de una nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="54062-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



