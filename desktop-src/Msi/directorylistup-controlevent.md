---
description: Este evento notifica al control DirectoryList que el usuario desea seleccionar el elemento primario del directorio actual. Para obtener información relacionada, vea cuadro de diálogo examinar.
ms.assetid: 83fdb160-ce3b-42e1-8688-42d3ba39d6dd
title: DirectoryListUp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fa8b3fcb19c46e00ad24030c9608cc73c57e9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003219"
---
# <a name="directorylistup-controlevent"></a><span data-ttu-id="ec14b-104">DirectoryListUp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="ec14b-104">DirectoryListUp ControlEvent</span></span>

<span data-ttu-id="ec14b-105">Este evento notifica al [control DirectoryList](directorylist-control.md) que el usuario desea seleccionar el elemento primario del directorio actual.</span><span class="sxs-lookup"><span data-stu-id="ec14b-105">This event notifies the [DirectoryList control](directorylist-control.md) that the user wants to select the parent of the present directory.</span></span> <span data-ttu-id="ec14b-106">Para obtener información relacionada, vea [cuadro de diálogo examinar](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="ec14b-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="ec14b-107">Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento.</span><span class="sxs-lookup"><span data-stu-id="ec14b-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="ec14b-108">El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec14b-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="ec14b-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ec14b-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ec14b-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="ec14b-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ec14b-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ec14b-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="ec14b-112">Si el directorio actual es el directorio raíz de la unidad, un evento DirectoryListUp deshabilita cualquier otro control que publique un evento DirectoryListUp.</span><span class="sxs-lookup"><span data-stu-id="ec14b-112">If the current directory is the root directory of the drive, a DirectoryListUp event disables any other controls that publish a DirectoryListUp event.</span></span>

## <a name="published-by"></a><span data-ttu-id="ec14b-113">Publicado por</span><span class="sxs-lookup"><span data-stu-id="ec14b-113">Published By</span></span>

[<span data-ttu-id="ec14b-114">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="ec14b-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="ec14b-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="ec14b-115">Argument</span></span>

<span data-ttu-id="ec14b-116">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="ec14b-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ec14b-117">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="ec14b-117">Action on Subscribers</span></span>

<span data-ttu-id="ec14b-118">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="ec14b-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ec14b-119">Uso típico</span><span class="sxs-lookup"><span data-stu-id="ec14b-119">Typical Use</span></span>

<span data-ttu-id="ec14b-120">Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el DirectoryList se usa para desencadenar la ejecución paso a paso en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="ec14b-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping up in the path.</span></span>

 

 



