---
description: Una página de referencia de eventos (ERP) es un documento HTML que proporciona Monitor de red información acerca de los eventos detectados durante la operación de experto o de supervisión.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Páginas de referencia de eventos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910086"
---
# <a name="about-event-reference-pages"></a><span data-ttu-id="31001-103">Páginas de referencia de eventos, acerca de</span><span class="sxs-lookup"><span data-stu-id="31001-103">About Event Reference Pages</span></span>

<span data-ttu-id="31001-104">Una página de referencia de eventos (ERP) es un documento HTML que proporciona Monitor de red información acerca de los eventos detectados durante la operación de experto o de supervisión.</span><span class="sxs-lookup"><span data-stu-id="31001-104">An event reference page (ERP) is an HTML document that provides Network Monitor information about events detected during expert or monitor operation.</span></span>

<span data-ttu-id="31001-105">Puede ver O ERP e en el Visor de eventos de Monitor de red, herramienta de control de supervisión o en cualquier explorador que admita las características HTML de Microsoft Internet Explorer versión 4,01 o posterior.</span><span class="sxs-lookup"><span data-stu-id="31001-105">You can view ERPs in the Event Viewer of Network Monitor, Monitor Control Tool, or in any browser that supports the HTML features of Microsoft Internet Explorer Version 4.01 or later.</span></span> <span data-ttu-id="31001-106">Es decir, puede Agregar controles admitidos o lenguajes con scripts en el ERP.</span><span class="sxs-lookup"><span data-stu-id="31001-106">That is, you can add supported controls or scripted languages into your ERP.</span></span>

<span data-ttu-id="31001-107">Sin embargo, O ERP e solo aparece si el experto designa el documento HTML por nombre.</span><span class="sxs-lookup"><span data-stu-id="31001-107">However, ERPs appear only if the expert designates the HTML document by name.</span></span> <span data-ttu-id="31001-108">Cuando se designa correctamente, el ERP aparece en el panel inferior cuando se selecciona el evento en el Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="31001-108">When properly designated, the ERP appears in the lower pane when the event in the Event Viewer is selected.</span></span> <span data-ttu-id="31001-109">En la ilustración siguiente se muestra un ERP asociado al monitor de intervalo del Protocolo de Internet (IP).</span><span class="sxs-lookup"><span data-stu-id="31001-109">The figure below shows an ERP associated with the Internet Protocol (IP) Range monitor.</span></span>

![un ERP asociado con el monitor de intervalo de IP](images/exview2.png)

## <a name="expert-events"></a><span data-ttu-id="31001-111">Eventos de expertos</span><span class="sxs-lookup"><span data-stu-id="31001-111">Expert Events</span></span>

<span data-ttu-id="31001-112">El miembro **EventIdent** de una estructura [**NMEVENTDATA**](nmeventdata.md) identifica los eventos de expertos.</span><span class="sxs-lookup"><span data-stu-id="31001-112">Expert events are identified by the **EventIdent** member of an [**NMEVENTDATA**](nmeventdata.md) structure.</span></span> <span data-ttu-id="31001-113">Al escribir un experto, se determinan los valores de **EventIdent** , que normalmente se numeran como 1, 2, 3, etc.</span><span class="sxs-lookup"><span data-stu-id="31001-113">When you write an expert you determine the **EventIdent** values, which are typically numbered 1, 2, 3, and so on.</span></span> <span data-ttu-id="31001-114">Por ejemplo, supongamos que un experto genera dos eventos (**EventIdent1** y **EventIdent2**).</span><span class="sxs-lookup"><span data-stu-id="31001-114">For example, suppose that an expert generates two events (**EventIdent1** and **EventIdent2**).</span></span> <span data-ttu-id="31001-115">Si desea que el Visor de eventos muestre los eventos por separado, debe crear dos documentos ERP independientes.</span><span class="sxs-lookup"><span data-stu-id="31001-115">If you want the Event Viewer to display the events separately, you must create two separate ERP documents.</span></span>

 

 



