---
description: El instalador usa este evento para mostrar una cadena informativa mientras se está compilando el script de ejecución de la instalación.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652687"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="85616-103">ScriptInProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="85616-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="85616-104">El instalador usa este evento para mostrar una cadena informativa mientras se está compilando el script de ejecución de la instalación.</span><span class="sxs-lookup"><span data-stu-id="85616-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="85616-105">La cadena informativa se puede mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="85616-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="85616-106">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="85616-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="85616-107">Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="85616-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="85616-108">Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="85616-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="85616-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="85616-109">Published By</span></span>

<span data-ttu-id="85616-110">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="85616-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="85616-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="85616-111">Argument</span></span>

<span data-ttu-id="85616-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="85616-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="85616-113">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="85616-113">Action on Subscribers</span></span>

<span data-ttu-id="85616-114">Un [control de texto](text-control.md) que se suscribe a ScriptInProgress mostrará la cadena de texto especificada en la [tabla UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="85616-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="85616-115">Uso típico</span><span class="sxs-lookup"><span data-stu-id="85616-115">Typical Use</span></span>

<span data-ttu-id="85616-116">Mientras se está compilando el script de ejecución, el instalador muestra un componente ProgressBar que indica el tiempo restante antes del inicio de la ejecución del script.</span><span class="sxs-lookup"><span data-stu-id="85616-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="85616-117">En este momento, el autor del paquete puede mostrar un mensaje preliminar que explica el ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="85616-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="85616-118">Para mostrar un mensaje preliminar, incluya un [control de texto](text-control.md) en el mismo cuadro de diálogo no modal que ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="85616-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="85616-119">Especifica que este control de texto se suscribe a ScriptInProgress ControlEvent, a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="85616-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="85616-120">Incluya una entrada en la [tabla UIText](uitext-table.md) con ScriptInProgress especificado en el campo clave.</span><span class="sxs-lookup"><span data-stu-id="85616-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="85616-121">Especifique el mensaje preliminar como una cadena de texto en el campo de texto de la tabla UIText.</span><span class="sxs-lookup"><span data-stu-id="85616-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="85616-122">Después, durante la compilación del script, el instalador mostrará esta cadena en el control de texto.</span><span class="sxs-lookup"><span data-stu-id="85616-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="85616-123">El texto mostrado desaparece en cuanto finaliza la compilación del script.</span><span class="sxs-lookup"><span data-stu-id="85616-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="85616-124">El mismo control de texto que se suscribe a ScriptInProgress ControlEvent, también puede suscribirse a [TimeRemaining ControlEvent,](timeremaining-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="85616-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="85616-125">En este caso, como el texto de la cadena de ScriptInProgress preliminar desaparece, se reemplaza por la cadena "tiempo restante: XX minutos".</span><span class="sxs-lookup"><span data-stu-id="85616-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



