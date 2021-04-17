---
description: El instalador usa este evento para publicar datos en la acción más reciente. Los datos se pueden mostrar en un cuadro de diálogo mediante un control de texto que se suscribe a este ControlEvent,. Este evento debe crearse en la tabla EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667061"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="07ebf-105">ActionData ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="07ebf-105">ActionData ControlEvent</span></span>

<span data-ttu-id="07ebf-106">El instalador usa este evento para publicar datos en la acción más reciente.</span><span class="sxs-lookup"><span data-stu-id="07ebf-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="07ebf-107">Los datos se pueden mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="07ebf-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="07ebf-108">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="07ebf-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="07ebf-109">Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="07ebf-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="07ebf-110">Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="07ebf-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="07ebf-111">Publicado por</span><span class="sxs-lookup"><span data-stu-id="07ebf-111">Published By</span></span>

<span data-ttu-id="07ebf-112">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="07ebf-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="07ebf-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="07ebf-113">Argument</span></span>

<span data-ttu-id="07ebf-114">Este ControlEvent, no utiliza un argumento.</span><span class="sxs-lookup"><span data-stu-id="07ebf-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="07ebf-115">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="07ebf-115">Action on Subscribers</span></span>

<span data-ttu-id="07ebf-116">Los suscriptores se ocultan cuando se inicia una nueva acción y se muestran cuando llegan nuevos datos de acción desde el instalador.</span><span class="sxs-lookup"><span data-stu-id="07ebf-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="07ebf-117">Uso típico</span><span class="sxs-lookup"><span data-stu-id="07ebf-117">Typical Use</span></span>

<span data-ttu-id="07ebf-118">Un [control de texto](text-control.md) en un cuadro de diálogo no modal se suscribe a este evento a través de la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="07ebf-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="07ebf-119">El [atributo control de texto](text-control-attribute.md) se muestra en el campo atributos de esta tabla para recibir los datos de la acción actual.</span><span class="sxs-lookup"><span data-stu-id="07ebf-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="07ebf-120">Normalmente se usa para mostrar los nombres de los archivos copiados durante la copia de archivos.</span><span class="sxs-lookup"><span data-stu-id="07ebf-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



