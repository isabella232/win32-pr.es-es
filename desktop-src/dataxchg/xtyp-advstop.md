---
title: XTYP_ADVSTOP transacción (ddeml. h)
description: Un cliente usa la \_ transacción XTYP ADVSTOP para finalizar un bucle de notificación con un servidor. Una función de devolución de llamada del servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP \_ ADVSTOP en la función DdeClientTransaction.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- Intercambio de datos de transacciones XTYP_ADVSTOP
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61292683377cd6c7243c3e41c5dbd9332a671163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714601"
---
# <a name="xtyp_advstop-transaction"></a><span data-ttu-id="5bbd3-105">XTYP \_ ADVSTOP</span><span class="sxs-lookup"><span data-stu-id="5bbd3-105">XTYP\_ADVSTOP transaction</span></span>

<span data-ttu-id="5bbd3-106">Un cliente usa la transacción **XTYP \_ ADVSTOP** para finalizar un bucle de notificación con un servidor.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-106">A client uses the **XTYP\_ADVSTOP** transaction to end an advise loop with a server.</span></span> <span data-ttu-id="5bbd3-107">Una función de devolución de llamada del servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ ADVSTOP** en la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="5bbd3-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTOP** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a><span data-ttu-id="5bbd3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5bbd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bbd3-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-110">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-112">Formato de datos asociado al bucle de notificación que se va a finalizar.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-112">The data format associated with the advise loop being ended.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-114">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-116">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-118">Identificador del nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5bbd3-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5bbd3-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5bbd3-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5bbd3-124">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bbd3-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5bbd3-125">Remarks</span></span>

<span data-ttu-id="5bbd3-126">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ asesora** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="5bbd3-126">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bbd3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bbd3-127">Requirements</span></span>



| <span data-ttu-id="5bbd3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bbd3-128">Requirement</span></span> | <span data-ttu-id="5bbd3-129">Value</span><span class="sxs-lookup"><span data-stu-id="5bbd3-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bbd3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bbd3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5bbd3-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5bbd3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5bbd3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5bbd3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5bbd3-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5bbd3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5bbd3-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5bbd3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bbd3-135"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5bbd3-135"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bbd3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="5bbd3-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="5bbd3-137">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5bbd3-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5bbd3-138">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="5bbd3-138">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="5bbd3-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="5bbd3-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="5bbd3-140">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="5bbd3-140">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="5bbd3-141">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5bbd3-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5bbd3-142">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="5bbd3-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

