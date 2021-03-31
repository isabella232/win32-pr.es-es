---
title: XTYP_POKE transacción (ddeml. h)
description: Un cliente usa la transacción de XTYP \_ para enviar datos no solicitados al servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP \_ en la función DdeClientTransaction.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- Intercambio de datos de transacciones XTYP_POKE
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e538f72b7a736ed9be5cf3e1d83e8729f42ef83d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996303"
---
# <a name="xtyp_poke-transaction"></a><span data-ttu-id="0dda0-105">XTYP \_</span><span class="sxs-lookup"><span data-stu-id="0dda0-105">XTYP\_POKE transaction</span></span>

<span data-ttu-id="0dda0-106">Un cliente usa la **transacción \_ de XTYP** para enviar datos no solicitados al servidor.</span><span class="sxs-lookup"><span data-stu-id="0dda0-106">A client uses the **XTYP\_POKE** transaction to send unsolicited data to the server.</span></span> <span data-ttu-id="0dda0-107">Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica [](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) **XTYP \_** en la función DdeClientTransaction.</span><span class="sxs-lookup"><span data-stu-id="0dda0-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_POKE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="0dda0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0dda0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dda0-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="0dda0-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-110">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="0dda0-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="0dda0-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-112">El formato de los datos enviados desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="0dda0-112">The format of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="0dda0-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-114">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="0dda0-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="0dda0-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-116">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="0dda0-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="0dda0-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-118">Identificador del nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="0dda0-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="0dda0-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-120">Identificador de los datos que el cliente envía al servidor.</span><span class="sxs-lookup"><span data-stu-id="0dda0-120">A handle to the data that the client is sending to the server.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="0dda0-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0dda0-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="0dda0-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="0dda0-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="0dda0-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0dda0-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dda0-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0dda0-125">Return value</span></span>

<span data-ttu-id="0dda0-126">Una función de devolución de llamada de servidor debe devolver la marca **DDE \_ Fack** si procesa esta transacción, la marca **\_ FBUSY de DDE** si está demasiado ocupada para procesar esta transacción o la marca **\_ FNOTPROCESSED de DDE** si rechaza esta transacción.</span><span class="sxs-lookup"><span data-stu-id="0dda0-126">A server callback function should return the **DDE\_FACK** flag if it processes this transaction, the **DDE\_FBUSY** flag if it is too busy to process this transaction, or the **DDE\_FNOTPROCESSED** flag if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dda0-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dda0-127">Remarks</span></span>

<span data-ttu-id="0dda0-128">Esta transacción se filtra si la aplicación de servidor especificó la marca de **\_ error CBF \_ fails** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="0dda0-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_POKES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dda0-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dda0-129">Requirements</span></span>



| <span data-ttu-id="0dda0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dda0-130">Requirement</span></span> | <span data-ttu-id="0dda0-131">Value</span><span class="sxs-lookup"><span data-stu-id="0dda0-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dda0-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dda0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0dda0-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0dda0-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0dda0-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dda0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0dda0-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0dda0-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="0dda0-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dda0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dda0-137"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dda0-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dda0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dda0-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="0dda0-139">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0dda0-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0dda0-140">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="0dda0-140">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="0dda0-141">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="0dda0-141">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="0dda0-142">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0dda0-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0dda0-143">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="0dda0-143">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

