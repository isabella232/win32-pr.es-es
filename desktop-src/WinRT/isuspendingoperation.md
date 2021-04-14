---
description: Proporciona información sobre una operación de suspensión de la aplicación.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interfaz ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541654"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="d4f64-103">Interfaz ISuspendingOperation</span><span class="sxs-lookup"><span data-stu-id="d4f64-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="d4f64-104">Proporciona información sobre una operación de suspensión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d4f64-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="d4f64-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4f64-105">Members</span></span>

<span data-ttu-id="d4f64-106">La interfaz **ISuspendingOperation** hereda de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="d4f64-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="d4f64-107">**ISuspendingOperation** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d4f64-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="d4f64-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4f64-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="d4f64-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4f64-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d4f64-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="d4f64-110">Methods</span></span>

<span data-ttu-id="d4f64-111">La interfaz **ISuspendingOperation** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d4f64-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="d4f64-112">Método</span><span class="sxs-lookup"><span data-stu-id="d4f64-112">Method</span></span>                                                  | <span data-ttu-id="d4f64-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4f64-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="d4f64-114">**GetDeferral**</span><span class="sxs-lookup"><span data-stu-id="d4f64-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="d4f64-115">Solicita que se retrase la operación de suspensión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d4f64-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d4f64-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4f64-116">Properties</span></span>

<span data-ttu-id="d4f64-117">La interfaz **ISuspendingOperation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d4f64-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="d4f64-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d4f64-118">Property</span></span>                                                     | <span data-ttu-id="d4f64-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d4f64-119">Access type</span></span>           | <span data-ttu-id="d4f64-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4f64-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4f64-121">**Fecha límite**</span><span class="sxs-lookup"><span data-stu-id="d4f64-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="d4f64-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d4f64-122">Read/write</span></span><br/> | <span data-ttu-id="d4f64-123">Obtiene el tiempo restante antes de que continúe una operación de suspensión de aplicación retrasada.</span><span class="sxs-lookup"><span data-stu-id="d4f64-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d4f64-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4f64-124">Requirements</span></span>



| <span data-ttu-id="d4f64-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f64-125">Requirement</span></span> | <span data-ttu-id="d4f64-126">Value</span><span class="sxs-lookup"><span data-stu-id="d4f64-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f64-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4f64-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f64-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d4f64-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d4f64-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4f64-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f64-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4f64-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d4f64-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4f64-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f64-132"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f64-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4f64-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d4f64-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4f64-134"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4f64-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f64-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4f64-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f64-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="d4f64-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="d4f64-137">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="d4f64-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="d4f64-138">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="d4f64-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 
