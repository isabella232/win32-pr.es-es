---
title: Interfaz IWMDRMIndividualizationStatus
description: La interfaz IWMDRMIndividualizationStatus permite la recuperación de información de estado avanzada sobre el progreso de la individualización. Esta interfaz se entrega con eventos MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Interfaz IWMDRMIndividualizationStatus formato de Windows Media
- Interfaz IWMDRMIndividualizationStatus formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995505"
---
# <a name="iwmdrmindividualizationstatus-interface"></a><span data-ttu-id="eca9a-105">Interfaz IWMDRMIndividualizationStatus</span><span class="sxs-lookup"><span data-stu-id="eca9a-105">IWMDRMIndividualizationStatus interface</span></span>

<span data-ttu-id="eca9a-106">La interfaz **IWMDRMIndividualizationStatus** permite la recuperación de información de estado avanzada sobre el progreso de la individualización.</span><span class="sxs-lookup"><span data-stu-id="eca9a-106">The **IWMDRMIndividualizationStatus** interface enables retrieval of advanced status information about the progress of individualization.</span></span>

<span data-ttu-id="eca9a-107">Esta interfaz se entrega con eventos MEWMDRMIndividualizationProgress.</span><span class="sxs-lookup"><span data-stu-id="eca9a-107">This interface is delivered with MEWMDRMIndividualizationProgress events.</span></span> <span data-ttu-id="eca9a-108">Muchos de estos eventos se generan entre una llamada a [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) y la finalización del proceso de individualización, que está señalado por la generación de un evento **MEWMDRMIndividualizationCompleted** .</span><span class="sxs-lookup"><span data-stu-id="eca9a-108">Many such events are generated between a call to [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) and the completion of the individualization process, which is signaled by the generation of an **MEWMDRMIndividualizationCompleted** event.</span></span>

<span data-ttu-id="eca9a-109">Para recuperar un puntero a una instancia de la interfaz **IWMDRMIndividualizationStatus** , primero debe llamar al método **IMFMediaEvent:: GetValue** del evento progress.</span><span class="sxs-lookup"><span data-stu-id="eca9a-109">To retrieve a pointer to an instance of the **IWMDRMIndividualizationStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="eca9a-110">El valor que se recupera del evento es un puntero a la interfaz **IUnknown** del objeto que implementa la interfaz **IWMDRMIndividualizationStatus** .</span><span class="sxs-lookup"><span data-stu-id="eca9a-110">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMIndividualizationStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="eca9a-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="eca9a-111">Members</span></span>

<span data-ttu-id="eca9a-112">La interfaz **IWMDRMIndividualizationStatus** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eca9a-112">The **IWMDRMIndividualizationStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eca9a-113">**IWMDRMIndividualizationStatus** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="eca9a-113">**IWMDRMIndividualizationStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="eca9a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="eca9a-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eca9a-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="eca9a-115">Methods</span></span>

<span data-ttu-id="eca9a-116">La interfaz **IWMDRMIndividualizationStatus** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="eca9a-116">The **IWMDRMIndividualizationStatus** interface has these methods.</span></span>



| <span data-ttu-id="eca9a-117">Método</span><span class="sxs-lookup"><span data-stu-id="eca9a-117">Method</span></span>                                                       | <span data-ttu-id="eca9a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="eca9a-118">Description</span></span>                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="eca9a-119">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="eca9a-119">**GetStatus**</span></span>](iwmdrmindividualizationstatus-getstatus.md) | <span data-ttu-id="eca9a-120">Recupera información detallada sobre la individualización.</span><span class="sxs-lookup"><span data-stu-id="eca9a-120">Retrieves detailed information about individualization.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="eca9a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="eca9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca9a-122">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="eca9a-122">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

