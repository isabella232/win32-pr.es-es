---
description: Representa el método al que se llama cuando se completa una acción asincrónica.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interfaz AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715157"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="7a987-103">Interfaz AsyncActionCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="7a987-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="7a987-104">Representa el método al que se llama cuando se completa una acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7a987-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="7a987-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a987-105">Members</span></span>

<span data-ttu-id="7a987-106">La interfaz **AsyncActionCompletedHandler** hereda de [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span><span class="sxs-lookup"><span data-stu-id="7a987-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="7a987-107">**AsyncActionCompletedHandler** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7a987-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="7a987-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7a987-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7a987-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="7a987-109">Methods</span></span>

<span data-ttu-id="7a987-110">La interfaz **AsyncActionCompletedHandler** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7a987-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="7a987-111">Método</span><span class="sxs-lookup"><span data-stu-id="7a987-111">Method</span></span>                                               | <span data-ttu-id="7a987-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a987-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7a987-113">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="7a987-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="7a987-114">Invoca el método al que se llama cuando se completa la acción asincrónica especificada.</span><span class="sxs-lookup"><span data-stu-id="7a987-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7a987-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a987-115">Remarks</span></span>

<span data-ttu-id="7a987-116">Asigne un **AsyncActionCompletedHandler** a un [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) para recibir una notificación cuando se complete la acción asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7a987-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a987-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a987-117">Requirements</span></span>



| <span data-ttu-id="7a987-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a987-118">Requirement</span></span> | <span data-ttu-id="7a987-119">Value</span><span class="sxs-lookup"><span data-stu-id="7a987-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a987-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a987-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a987-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7a987-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="7a987-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a987-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a987-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a987-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="7a987-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a987-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a987-125"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7a987-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a987-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a987-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a987-127">**IAsyncInfo**</span><span class="sxs-lookup"><span data-stu-id="7a987-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

