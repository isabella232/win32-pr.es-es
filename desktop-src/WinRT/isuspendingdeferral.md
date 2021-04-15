---
description: Administra una operación de suspensión de aplicación retrasada.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interfaz ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648192"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="3087f-103">Interfaz ISuspendingDeferral</span><span class="sxs-lookup"><span data-stu-id="3087f-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="3087f-104">Administra una operación de suspensión de aplicación retrasada.</span><span class="sxs-lookup"><span data-stu-id="3087f-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="3087f-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="3087f-105">Members</span></span>

<span data-ttu-id="3087f-106">La interfaz **ISuspendingDeferral** hereda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="3087f-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="3087f-107">**ISuspendingDeferral** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3087f-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="3087f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3087f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3087f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3087f-109">Methods</span></span>

<span data-ttu-id="3087f-110">La interfaz **ISuspendingDeferral** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3087f-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="3087f-111">Método</span><span class="sxs-lookup"><span data-stu-id="3087f-111">Method</span></span>                                           | <span data-ttu-id="3087f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3087f-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3087f-113">**Completo**</span><span class="sxs-lookup"><span data-stu-id="3087f-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="3087f-114">Notifica al sistema que la aplicación ha guardado sus datos y está listo para su suspensión.</span><span class="sxs-lookup"><span data-stu-id="3087f-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3087f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3087f-115">Requirements</span></span>



| <span data-ttu-id="3087f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3087f-116">Requirement</span></span> | <span data-ttu-id="3087f-117">Value</span><span class="sxs-lookup"><span data-stu-id="3087f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3087f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3087f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3087f-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3087f-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3087f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3087f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3087f-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3087f-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3087f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3087f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3087f-123"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="3087f-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="3087f-124">IDL</span><span class="sxs-lookup"><span data-stu-id="3087f-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3087f-125"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3087f-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3087f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3087f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3087f-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="3087f-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="3087f-128">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="3087f-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="3087f-129">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="3087f-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 
