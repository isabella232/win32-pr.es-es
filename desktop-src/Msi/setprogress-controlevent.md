---
description: El instalador usa el evento SetProgress para publicar información sobre el progreso de la instalación.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002366"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="457e4-103">SetProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="457e4-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="457e4-104">El instalador usa el evento SetProgress para publicar información sobre el progreso de la instalación.</span><span class="sxs-lookup"><span data-stu-id="457e4-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="457e4-105">Un [control ProgressBar](progressbar-control.md) o un control de la [cartelera](billboard-control.md) debe suscribirse al evento a través de la [tabla EventMapping](eventmapping-table.md) mediante el nombre de la acción cuyo progreso se está indicando.</span><span class="sxs-lookup"><span data-stu-id="457e4-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="457e4-106">Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="457e4-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="457e4-107">Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="457e4-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="457e4-108">Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="457e4-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="457e4-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="457e4-109">Published By</span></span>

<span data-ttu-id="457e4-110">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="457e4-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="457e4-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="457e4-111">Argument</span></span>

<span data-ttu-id="457e4-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="457e4-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="457e4-113">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="457e4-113">Action on Subscribers</span></span>

<span data-ttu-id="457e4-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="457e4-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="457e4-115">Uso típico</span><span class="sxs-lookup"><span data-stu-id="457e4-115">Typical Use</span></span>

<span data-ttu-id="457e4-116">Un control [ProgressBar](progressbar-control.md) de un cuadro de diálogo no modal se suscribe a este evento mediante el atributo [Progress](progress-control-attribute.md) para recibir la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="457e4-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



