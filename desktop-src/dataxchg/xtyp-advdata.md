---
title: XTYP_ADVDATA transacción (ddeml. h)
description: Informa al cliente de que el valor del elemento de datos ha cambiado. La función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción después de establecer un bucle de notificaciones con un servidor.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- Intercambio de datos de transacciones XTYP_ADVDATA
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685868"
---
# <a name="xtyp_advdata-transaction"></a><span data-ttu-id="5a58d-105">XTYP \_ ADVDATA</span><span class="sxs-lookup"><span data-stu-id="5a58d-105">XTYP\_ADVDATA transaction</span></span>

<span data-ttu-id="5a58d-106">Informa al cliente de que el valor del elemento de datos ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="5a58d-106">Informs the client that the value of the data item has changed.</span></span> <span data-ttu-id="5a58d-107">La función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción después de establecer un bucle de notificaciones con un servidor.</span><span class="sxs-lookup"><span data-stu-id="5a58d-107">The Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction after establishing an advise loop with a server.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="5a58d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a58d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a58d-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="5a58d-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-110">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="5a58d-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5a58d-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-112">El formato Atom de los datos enviados desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="5a58d-112">The format atom of the data sent from the server.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5a58d-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-114">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="5a58d-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5a58d-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-116">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="5a58d-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5a58d-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-118">Identificador del nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="5a58d-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5a58d-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-120">Identificador de los datos asociados con el par nombre del tema y nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="5a58d-120">A handle to the data associated with the topic name and item name pair.</span></span> <span data-ttu-id="5a58d-121">Este parámetro es **null** si el cliente especificó la marca **\_ NoData de XTYPF** cuando solicitó el bucle de notificación.</span><span class="sxs-lookup"><span data-stu-id="5a58d-121">This parameter is **NULL** if the client specified the **XTYPF\_NODATA** flag when it requested the advise loop.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5a58d-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-123">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5a58d-123">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5a58d-124">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5a58d-124">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5a58d-125">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5a58d-125">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a58d-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a58d-126">Return value</span></span>

<span data-ttu-id="5a58d-127">Una función de devolución de llamada DDE debe devolver **DDE \_ Fack** si procesa esta transacción, **DDE \_ FBUSY** si está demasiado ocupado para procesar esta transacción, **o \_ FNOTPROCESSED DDE** si rechaza esta transacción.</span><span class="sxs-lookup"><span data-stu-id="5a58d-127">A DDE callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a58d-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a58d-128">Remarks</span></span>

<span data-ttu-id="5a58d-129">Una aplicación no debe liberar el identificador de datos obtenido durante esta transacción.</span><span class="sxs-lookup"><span data-stu-id="5a58d-129">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="5a58d-130">Sin embargo, una aplicación debe copiar los datos asociados al identificador de datos si la aplicación debe procesar los datos después de que se devuelva la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="5a58d-130">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="5a58d-131">Una aplicación puede usar la función [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.</span><span class="sxs-lookup"><span data-stu-id="5a58d-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a58d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a58d-132">Requirements</span></span>



| <span data-ttu-id="5a58d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a58d-133">Requirement</span></span> | <span data-ttu-id="5a58d-134">Value</span><span class="sxs-lookup"><span data-stu-id="5a58d-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a58d-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a58d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5a58d-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a58d-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5a58d-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a58d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5a58d-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a58d-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5a58d-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a58d-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a58d-140"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a58d-140"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a58d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a58d-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a58d-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5a58d-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5a58d-143">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="5a58d-143">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="5a58d-144">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="5a58d-144">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="5a58d-145">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="5a58d-145">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="5a58d-146">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5a58d-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5a58d-147">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="5a58d-147">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

