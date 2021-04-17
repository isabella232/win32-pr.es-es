---
description: El control DirectoryList publica IgnoreChange ControlEvent, cuando se cambia la carpeta seleccionada de un directorio a otro en el control. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652586"
---
# <a name="ignorechange-controlevent"></a><span data-ttu-id="665c3-104">IgnoreChange ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="665c3-104">IgnoreChange ControlEvent</span></span>

<span data-ttu-id="665c3-105">El [control DirectoryList](directorylist-control.md) publica IgnoreChange ControlEvent, cuando se cambia la carpeta seleccionada de un directorio a otro en el control.</span><span class="sxs-lookup"><span data-stu-id="665c3-105">The IgnoreChange ControlEvent is published by the [DirectoryList control](directorylist-control.md) when the selected folder is changed from one directory to another directory in the control.</span></span> <span data-ttu-id="665c3-106">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="665c3-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="665c3-107">Este ControlEvent, requiere que la interfaz de usuario se ejecute en el nivel de interfaz de usuario [*completo*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="665c3-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="665c3-108">Este evento no funcionará con una [*interfaz*](r-gly.md) de usuario [*básica*](b-gly.md)o no reducida.</span><span class="sxs-lookup"><span data-stu-id="665c3-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="665c3-109">Para obtener más información, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="665c3-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="665c3-110">Publicado por</span><span class="sxs-lookup"><span data-stu-id="665c3-110">Published By</span></span>

[<span data-ttu-id="665c3-111">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="665c3-111">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="665c3-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="665c3-112">Argument</span></span>

<span data-ttu-id="665c3-113">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="665c3-113">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="665c3-114">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="665c3-114">Action on Subscribers</span></span>

<span data-ttu-id="665c3-115">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="665c3-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="665c3-116">Uso típico</span><span class="sxs-lookup"><span data-stu-id="665c3-116">Typical Use</span></span>

<span data-ttu-id="665c3-117">Normalmente, el [control DirectoryCombo](directorycombo-control.md) emplea el ControlEvent, de IgnoreChange.</span><span class="sxs-lookup"><span data-stu-id="665c3-117">The [DirectoryCombo control](directorycombo-control.md) commonly employs the IgnoreChange ControlEvent.</span></span>

 

 



