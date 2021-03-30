---
description: Este evento selecciona y resalta un directorio en el control DirectoryList que el usuario ha elegido abrir. Para obtener información relacionada, vea cuadro de diálogo examinar.
ms.assetid: 95cdf345-e1bb-41d8-b1e0-2acf97e33110
title: DirectoryListOpen ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeb3a570f49032adb0f5208514c26dd9cc16726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279656"
---
# <a name="directorylistopen-controlevent"></a><span data-ttu-id="2a4e4-104">DirectoryListOpen ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="2a4e4-104">DirectoryListOpen ControlEvent</span></span>

<span data-ttu-id="2a4e4-105">Este evento selecciona y resalta un directorio en el [control DirectoryList](directorylist-control.md) que el usuario ha elegido abrir.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-105">This event selects and highlights a directory in the [DirectoryList control](directorylist-control.md) that the user has chosen to open.</span></span> <span data-ttu-id="2a4e4-106">Para obtener información relacionada, vea [cuadro de diálogo examinar](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="2a4e4-106">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="2a4e4-107">Este evento debe publicarse con un [control Pushbutton](pushbutton-control.md) situado en el mismo cuadro de diálogo que el control que se suscribe a este evento.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-107">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="2a4e4-108">El evento debe crearse en la [tabla ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a4e4-108">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="2a4e4-109">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2a4e4-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="2a4e4-110">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="2a4e4-111">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="2a4e4-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="2a4e4-112">Si no se ha seleccionado ningún directorio en el [control DirectoryList](directorylist-control.md), un evento DirectoryListOpen deshabilita cualquier otro control que publique un evento DirectoryListOpen.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-112">If no directory has been selected in the [DirectoryList control](directorylist-control.md), a DirectoryListOpen event disables any other controls that publish a DirectoryListOpen event.</span></span>

## <a name="published-by"></a><span data-ttu-id="2a4e4-113">Publicado por</span><span class="sxs-lookup"><span data-stu-id="2a4e4-113">Published By</span></span>

[<span data-ttu-id="2a4e4-114">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="2a4e4-114">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="2a4e4-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="2a4e4-115">Argument</span></span>

<span data-ttu-id="2a4e4-116">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-116">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="2a4e4-117">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="2a4e4-117">Action on Subscribers</span></span>

<span data-ttu-id="2a4e4-118">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-118">This ControlEvent performs no action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="2a4e4-119">Uso típico</span><span class="sxs-lookup"><span data-stu-id="2a4e4-119">Typical Use</span></span>

<span data-ttu-id="2a4e4-120">Un control [Pushbutton](pushbutton-control.md) en el mismo cuadro de diálogo modal que el DirectoryList se usa para desencadenar la ejecución paso a paso en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="2a4e4-120">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger stepping down in the path.</span></span>

 

 



