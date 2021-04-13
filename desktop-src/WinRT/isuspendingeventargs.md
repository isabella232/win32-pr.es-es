---
description: Proporciona datos para un evento de suspensión de la aplicación.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interfaz ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648191"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="d620c-103">Interfaz ISuspendingEventArgs</span><span class="sxs-lookup"><span data-stu-id="d620c-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="d620c-104">Proporciona datos para un evento de suspensión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d620c-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="d620c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="d620c-105">Members</span></span>

<span data-ttu-id="d620c-106">La interfaz **ISuspendingEventArgs** hereda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="d620c-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="d620c-107">**ISuspendingEventArgs** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d620c-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="d620c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d620c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d620c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d620c-109">Properties</span></span>

<span data-ttu-id="d620c-110">La interfaz **ISuspendingEventArgs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d620c-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="d620c-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d620c-111">Property</span></span>                                                                           | <span data-ttu-id="d620c-112">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d620c-112">Access type</span></span>           | <span data-ttu-id="d620c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d620c-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="d620c-114">**SuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="d620c-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="d620c-115">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d620c-115">Read/write</span></span><br/> | <span data-ttu-id="d620c-116">Obtiene la operación de suspensión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d620c-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d620c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d620c-117">Remarks</span></span>

<span data-ttu-id="d620c-118">Se tiene acceso a este objeto cuando se implementan controladores de eventos como [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)y se produce la [**\_ suspensión**](/previous-versions//hh438376(v=vs.85)) para responder a eventos de suspensión de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d620c-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="d620c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d620c-119">Requirements</span></span>



| <span data-ttu-id="d620c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d620c-120">Requirement</span></span> | <span data-ttu-id="d620c-121">Value</span><span class="sxs-lookup"><span data-stu-id="d620c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d620c-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d620c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d620c-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d620c-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d620c-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d620c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d620c-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d620c-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d620c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d620c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d620c-127"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d620c-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d620c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d620c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d620c-129"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d620c-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d620c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d620c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d620c-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="d620c-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="d620c-132">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="d620c-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="d620c-133">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="d620c-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 
