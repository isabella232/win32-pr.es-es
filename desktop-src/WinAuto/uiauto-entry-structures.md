---
title: Estructuras de UI Automation
description: En esta sección se describen las estructuras utilizadas por las aplicaciones cliente de automatización de la interfaz de usuario y el proveedor de UI Automation para Microsoft Win32.
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486678"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="8aaad-103">Estructuras de UI Automation</span><span class="sxs-lookup"><span data-stu-id="8aaad-103">UI Automation Structures</span></span>

<span data-ttu-id="8aaad-104">En esta sección se describen las estructuras utilizadas por las aplicaciones cliente de automatización de la interfaz de usuario y el proveedor de UI Automation para Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="8aaad-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8aaad-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8aaad-105">In this section</span></span>



| <span data-ttu-id="8aaad-106">Estructura</span><span class="sxs-lookup"><span data-stu-id="8aaad-106">Structure</span></span>                                                                            | <span data-ttu-id="8aaad-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8aaad-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8aaad-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="8aaad-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="8aaad-109">Contiene información sobre una propiedad extendida.</span><span class="sxs-lookup"><span data-stu-id="8aaad-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="8aaad-110">**UIAutomationEventInfo**</span><span class="sxs-lookup"><span data-stu-id="8aaad-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="8aaad-111">Contiene información sobre un evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="8aaad-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="8aaad-112">**UIAutomationMethodInfo**</span><span class="sxs-lookup"><span data-stu-id="8aaad-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="8aaad-113">Contiene información sobre un método que es compatible con un patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="8aaad-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="8aaad-114">**UIAutomationParameter**</span><span class="sxs-lookup"><span data-stu-id="8aaad-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="8aaad-115">Contiene información sobre un parámetro de un patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="8aaad-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="8aaad-116">**UIAutomationPatternInfo**</span><span class="sxs-lookup"><span data-stu-id="8aaad-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="8aaad-117">Contiene información sobre un patrón de control personalizado.</span><span class="sxs-lookup"><span data-stu-id="8aaad-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="8aaad-118">**UIAutomationPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="8aaad-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="8aaad-119">Contiene información sobre una propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="8aaad-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="8aaad-120">**UiaChangeInfo**</span><span class="sxs-lookup"><span data-stu-id="8aaad-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="8aaad-121">Contiene datos sobre un cambio en la automatización de la interfaz de usuario que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="8aaad-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="8aaad-122">**UiaPoint**</span><span class="sxs-lookup"><span data-stu-id="8aaad-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="8aaad-123">Contiene las coordenadas de un punto.</span><span class="sxs-lookup"><span data-stu-id="8aaad-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="8aaad-124">**UiaRect**</span><span class="sxs-lookup"><span data-stu-id="8aaad-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="8aaad-125">Contiene la posición y el tamaño de un rectángulo, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8aaad-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 





