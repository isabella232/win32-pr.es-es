---
title: Accesibilidad de controles ActiveX sin ventanas
description: En esta sección se describe cómo usar la API de accesibilidad de Windows para asegurarse de que se pueda tener acceso a los controles ActiveX sin ventanas de Microsoft.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421103"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="bcb2b-103">Accesibilidad de controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="bcb2b-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="bcb2b-104">En esta sección se describe cómo usar la API de accesibilidad de Windows para asegurarse de que se pueda tener acceso a los controles ActiveX sin ventanas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="bcb2b-105">Windows 8 incluye nuevas interfaces de API de accesibilidad de Windows que simplifican la tarea de implementar la accesibilidad para controles ActiveX sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="bcb2b-106">La API incluye interfaces que se implementan en un control sin ventanas y en el contenedor de controles, lo que permite que el control sin ventanas y su contenedor funcionen juntos para proporcionar información de accesibilidad sobre el control sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="bcb2b-107">La API admite los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="bcb2b-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="bcb2b-108">Microsoft Active Accessibility controles sin ventanas hospedados en un contenedor de control de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="bcb2b-109">Microsoft Active Accessibility controles sin ventanas hospedados en un contenedor de controles de automatización de la interfaz de usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="bcb2b-110">Controles sin ventana de automatización de la interfaz de usuario hospedados en un contenedor de control de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="bcb2b-111">Controles sin ventana de automatización de la interfaz de usuario hospedados en un contenedor de control de UI Automation.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="bcb2b-112">En la tabla siguiente se enumeran las interfaces que admiten los controles ActiveX sin ventanas y se identifican los objetos que implementan las interfaces.</span><span class="sxs-lookup"><span data-stu-id="bcb2b-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="bcb2b-113">Object</span><span class="sxs-lookup"><span data-stu-id="bcb2b-113">Object</span></span>              | <span data-ttu-id="bcb2b-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="bcb2b-114">MSAA</span></span>                                                                             | <span data-ttu-id="bcb2b-115">automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="bcb2b-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb2b-116">Objeto de control</span><span class="sxs-lookup"><span data-stu-id="bcb2b-116">Control object</span></span>      | [<span data-ttu-id="bcb2b-117">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="bcb2b-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="bcb2b-118">Sitio de control</span><span class="sxs-lookup"><span data-stu-id="bcb2b-118">Control site</span></span>        | [<span data-ttu-id="bcb2b-119">**IAccessibleWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="bcb2b-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="bcb2b-120">**IRawElementProviderWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="bcb2b-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="bcb2b-121">Raíz de la ventana host</span><span class="sxs-lookup"><span data-stu-id="bcb2b-121">Root of host window</span></span> | [<span data-ttu-id="bcb2b-122">**IAccessibleHostingElementProviders**</span><span class="sxs-lookup"><span data-stu-id="bcb2b-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="bcb2b-123">**IRawElementProviderHostingAccessibles**</span><span class="sxs-lookup"><span data-stu-id="bcb2b-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="bcb2b-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="bcb2b-124">In this section</span></span>

-   [<span data-ttu-id="bcb2b-125">Cómo usar la automatización de la interfaz de usuario para hacer que un control ActiveX sin ventanas sea accesible</span><span class="sxs-lookup"><span data-stu-id="bcb2b-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="bcb2b-126">Cómo usar MSAA para hacer que un control ActiveX sin ventanas sea accesible</span><span class="sxs-lookup"><span data-stu-id="bcb2b-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="bcb2b-127">Cómo hospedar un control ActiveX sin ventanas de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="bcb2b-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="bcb2b-128">Cómo hospedar un control ActiveX sin ventanas de MSAA</span><span class="sxs-lookup"><span data-stu-id="bcb2b-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 