---
description: El mensaje de línea de \_ CALLHUBCLOSE TAPI se envía cuando se ha cerrado un centro de llamadas.
ms.assetid: 738dcb20-99b5-44fe-8ad9-b14b8d977f53
title: Mensaje de LINE_CALLHUBCLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b538d6f154f3dacb2d779b6233722df16cc635d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680181"
---
# <a name="line_callhubclose-message"></a><span data-ttu-id="14a55-103">Mensaje de línea \_ CALLHUBCLOSE</span><span class="sxs-lookup"><span data-stu-id="14a55-103">LINE\_CALLHUBCLOSE message</span></span>

<span data-ttu-id="14a55-104">El mensaje de **línea de \_ CALLHUBCLOSE** TAPI se envía cuando se ha cerrado un centro de llamadas.</span><span class="sxs-lookup"><span data-stu-id="14a55-104">The TAPI **LINE\_CALLHUBCLOSE** message is sent when a call hub has been closed.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="14a55-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14a55-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a55-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="14a55-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="14a55-107">Identificador de la llamada.</span><span class="sxs-lookup"><span data-stu-id="14a55-107">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="14a55-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="14a55-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="14a55-109">Instancia de devolución de llamada proporcionada al abrir la línea de la llamada.</span><span class="sxs-lookup"><span data-stu-id="14a55-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="14a55-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="14a55-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="14a55-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="14a55-111">Reserved.</span></span> <span data-ttu-id="14a55-112">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="14a55-112">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="14a55-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="14a55-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="14a55-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="14a55-114">Reserved.</span></span> <span data-ttu-id="14a55-115">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="14a55-115">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="14a55-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="14a55-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="14a55-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="14a55-117">Reserved.</span></span> <span data-ttu-id="14a55-118">Establecer en 0.</span><span class="sxs-lookup"><span data-stu-id="14a55-118">Set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a55-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14a55-119">Return value</span></span>

<span data-ttu-id="14a55-120">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="14a55-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a55-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14a55-121">Remarks</span></span>

<span data-ttu-id="14a55-122">Este mensaje se origina con TAPI en lugar de con un proveedor de servicios, por lo que no hay ningún mensaje TSPI correspondiente.</span><span class="sxs-lookup"><span data-stu-id="14a55-122">This message originates with TAPI rather than with a service provider, so there is no corresponding TSPI message.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a55-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a55-123">Requirements</span></span>



| <span data-ttu-id="14a55-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a55-124">Requirement</span></span> | <span data-ttu-id="14a55-125">Value</span><span class="sxs-lookup"><span data-stu-id="14a55-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="14a55-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="14a55-126">TAPI version</span></span><br/> | <span data-ttu-id="14a55-127">Requiere TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="14a55-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="14a55-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14a55-128">Header</span></span><br/>       | <dl> <span data-ttu-id="14a55-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="14a55-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




