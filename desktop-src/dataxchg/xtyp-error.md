---
title: XTYP_ERROR transacción (ddeml. h)
description: Una función de devolución de llamada de Intercambio dinámico de datos (DDE), DdeCallback, recibe la \_ transacción de error XTYP cuando se produce un error crítico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Intercambio de datos de transacciones XTYP_ERROR
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705136"
---
# <a name="xtyp_error-transaction"></a><span data-ttu-id="edd1f-104">\_Transacción de error XTYP</span><span class="sxs-lookup"><span data-stu-id="edd1f-104">XTYP\_ERROR transaction</span></span>

<span data-ttu-id="edd1f-105">Una función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **\_ error XTYP** cuando se produce un error crítico.</span><span class="sxs-lookup"><span data-stu-id="edd1f-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_ERROR** transaction when a critical error occurs.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="edd1f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edd1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd1f-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="edd1f-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-108">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="edd1f-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="edd1f-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="edd1f-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="edd1f-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="edd1f-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="edd1f-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-112">Identificador de la conversación asociada al error.</span><span class="sxs-lookup"><span data-stu-id="edd1f-112">A handle to the conversation associated with the error.</span></span> <span data-ttu-id="edd1f-113">Este parámetro es **null** si el error no está asociado a una conversación.</span><span class="sxs-lookup"><span data-stu-id="edd1f-113">This parameter is **NULL** if the error is not associated with a conversation.</span></span>

</dd> <dt>

<span data-ttu-id="edd1f-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="edd1f-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="edd1f-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="edd1f-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="edd1f-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="edd1f-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="edd1f-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="edd1f-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-119">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="edd1f-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="edd1f-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="edd1f-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-121">Código de error en la palabra de orden inferior.</span><span class="sxs-lookup"><span data-stu-id="edd1f-121">The error code in the low-order word.</span></span> <span data-ttu-id="edd1f-122">Actualmente, solo se admite el siguiente código de error.</span><span class="sxs-lookup"><span data-stu-id="edd1f-122">Currently, only the following error code is supported.</span></span>



| <span data-ttu-id="edd1f-123">Value</span><span class="sxs-lookup"><span data-stu-id="edd1f-123">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="edd1f-124">Significado</span><span class="sxs-lookup"><span data-stu-id="edd1f-124">Meaning</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <span data-ttu-id="edd1f-125"><dt>**DMLERR \_ de \_ memoria insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="edd1f-125"><dt>**DMLERR\_LOW\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="edd1f-126">Memoria insuficiente; es posible que se pierdan los datos de aconsejar, escribir o ejecutar, o bien se puede producir un error en el sistema.</span><span class="sxs-lookup"><span data-stu-id="edd1f-126">Memory is low; advise, poke, or execute data may be lost, or the system may fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="edd1f-127">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="edd1f-127">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="edd1f-128">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="edd1f-128">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="edd1f-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edd1f-129">Remarks</span></span>

<span data-ttu-id="edd1f-130">Una aplicación no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="edd1f-130">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span> <span data-ttu-id="edd1f-131">La biblioteca de administración de Intercambio dinámico de datos (DDEML) intenta liberar memoria quitando recursos no críticos.</span><span class="sxs-lookup"><span data-stu-id="edd1f-131">The Dynamic Data Exchange Management Library (DDEML) attempts to free memory by removing noncritical resources.</span></span> <span data-ttu-id="edd1f-132">Una aplicación que tenga conversaciones bloqueadas debe desbloquearla.</span><span class="sxs-lookup"><span data-stu-id="edd1f-132">An application that has blocked conversations should unblock them.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd1f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edd1f-133">Requirements</span></span>



| <span data-ttu-id="edd1f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd1f-134">Requirement</span></span> | <span data-ttu-id="edd1f-135">Value</span><span class="sxs-lookup"><span data-stu-id="edd1f-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd1f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd1f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="edd1f-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="edd1f-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="edd1f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edd1f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="edd1f-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="edd1f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="edd1f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="edd1f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd1f-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edd1f-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd1f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="edd1f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd1f-143">Información general de la biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="edd1f-143">Dynamic Data Exchange Management Library Overview</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

