---
description: Habilita la finalización de tareas.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interfaz TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278490"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="dc309-103">Interfaz TaskCompletionClient</span><span class="sxs-lookup"><span data-stu-id="dc309-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="dc309-104">Habilita la finalización de tareas.</span><span class="sxs-lookup"><span data-stu-id="dc309-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="dc309-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="dc309-105">Members</span></span>

<span data-ttu-id="dc309-106">La interfaz **TaskCompletionClient** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dc309-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dc309-107">**TaskCompletionClient** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dc309-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="dc309-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc309-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dc309-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dc309-109">Methods</span></span>

<span data-ttu-id="dc309-110">La interfaz **TaskCompletionClient** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dc309-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="dc309-111">Método</span><span class="sxs-lookup"><span data-stu-id="dc309-111">Method</span></span>                                                                    | <span data-ttu-id="dc309-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc309-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="dc309-113">**ApplyTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="dc309-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="dc309-114">Comienza la finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="dc309-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="dc309-115">**RevokeTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="dc309-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="dc309-116">Finaliza la finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="dc309-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="dc309-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc309-117">Remarks</span></span>

<span data-ttu-id="dc309-118">El GUID para esta interfaz es "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span><span class="sxs-lookup"><span data-stu-id="dc309-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="dc309-119">Esta API está en desuso y puede que no esté disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc309-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="dc309-120">En su lugar, las aplicaciones deben usar las API en el espacio de nombres [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="dc309-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc309-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc309-121">Requirements</span></span>



| <span data-ttu-id="dc309-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc309-122">Requirement</span></span> | <span data-ttu-id="dc309-123">Value</span><span class="sxs-lookup"><span data-stu-id="dc309-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc309-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc309-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dc309-125">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc309-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc309-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc309-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dc309-127">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc309-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc309-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc309-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc309-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc309-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
