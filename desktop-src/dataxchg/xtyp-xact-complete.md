---
title: XTYP_XACT_COMPLETE transacción (ddeml. h)
description: Una función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), DdeCallback, recibe la \_ \_ transacción de transacciones completadas de XTYP cuando se ha completado una transacción asincrónica, iniciada por una llamada a la función DdeClientTransaction.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Intercambio de datos de transacciones XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685918"
---
# <a name="xtyp_xact_complete-transaction"></a><span data-ttu-id="5f877-104">\_ \_ Transacción completa XTYP Xact</span><span class="sxs-lookup"><span data-stu-id="5f877-104">XTYP\_XACT\_COMPLETE transaction</span></span>

<span data-ttu-id="5f877-105">Una función de devolución de llamada de cliente de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de transacciones **\_ \_ completadas de XTYP** cuando se ha completado una transacción asincrónica, iniciada por una llamada a la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="5f877-105">A Dynamic Data Exchange (DDE) client callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_XACT\_COMPLETE** transaction when an asynchronous transaction, initiated by a call to the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function, has completed.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a><span data-ttu-id="5f877-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f877-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f877-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="5f877-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-108">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="5f877-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="5f877-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-110">El formato de los datos asociados a la transacción completada (si es aplicable) o **null** si no se intercambiaron datos durante la transacción.</span><span class="sxs-lookup"><span data-stu-id="5f877-110">The format of the data associated with the completed transaction (if applicable) or **NULL** if no data was exchanged during the transaction.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="5f877-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-112">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="5f877-112">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="5f877-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-114">Identificador del nombre de tema implicado en la transacción completada.</span><span class="sxs-lookup"><span data-stu-id="5f877-114">A handle to the topic name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="5f877-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-116">Identificador del nombre de elemento implicado en la transacción completada.</span><span class="sxs-lookup"><span data-stu-id="5f877-116">A handle to the item name involved in the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="5f877-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-118">Identificador de los datos implicados en la transacción completada, si procede.</span><span class="sxs-lookup"><span data-stu-id="5f877-118">A handle to the data involved in the completed transaction, if applicable.</span></span> <span data-ttu-id="5f877-119">Si la transacción se realizó correctamente pero no implicaba ningún dato, este parámetro es **true**.</span><span class="sxs-lookup"><span data-stu-id="5f877-119">If the transaction was successful but involved no data, this parameter is **TRUE**.</span></span> <span data-ttu-id="5f877-120">Este parámetro es **null** si la transacción no se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5f877-120">This parameter is **NULL** if the transaction was unsuccessful.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="5f877-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-122">Identificador de transacción de la transacción completada.</span><span class="sxs-lookup"><span data-stu-id="5f877-122">The transaction identifier of the completed transaction.</span></span>

</dd> <dt>

<span data-ttu-id="5f877-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="5f877-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="5f877-124">Cualquier marca de estado **DDE \_** aplicable en la palabra baja.</span><span class="sxs-lookup"><span data-stu-id="5f877-124">Any applicable **DDE\_** status flags in the low word.</span></span> <span data-ttu-id="5f877-125">Este parámetro proporciona compatibilidad con aplicaciones que dependen de los bits **\_ APPSTATUS de DDE** .</span><span class="sxs-lookup"><span data-stu-id="5f877-125">This parameter provides support for applications dependent on **DDE\_APPSTATUS** bits.</span></span> <span data-ttu-id="5f877-126">Se recomienda que las aplicaciones dejen de usar estos bits, ya que es posible que no se admitan en versiones futuras de DDEML.</span><span class="sxs-lookup"><span data-stu-id="5f877-126">It is recommended that applications no longer use these bits   they may not be supported in future versions of the DDEML.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5f877-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f877-127">Remarks</span></span>

<span data-ttu-id="5f877-128">Una aplicación no debe liberar el identificador de datos obtenido durante esta transacción.</span><span class="sxs-lookup"><span data-stu-id="5f877-128">An application must not free the data handle obtained during this transaction.</span></span> <span data-ttu-id="5f877-129">Sin embargo, una aplicación debe copiar los datos asociados al identificador de datos si la aplicación debe procesar los datos después de que se devuelva la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="5f877-129">An application must, however, copy the data associated with the data handle if the application must process the data after the callback function returns.</span></span> <span data-ttu-id="5f877-130">Una aplicación puede usar la función [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.</span><span class="sxs-lookup"><span data-stu-id="5f877-130">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f877-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f877-131">Requirements</span></span>



| <span data-ttu-id="5f877-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f877-132">Requirement</span></span> | <span data-ttu-id="5f877-133">Value</span><span class="sxs-lookup"><span data-stu-id="5f877-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f877-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f877-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5f877-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f877-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5f877-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f877-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5f877-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f877-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5f877-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f877-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f877-139"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f877-139"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f877-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f877-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f877-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5f877-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f877-142">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="5f877-142">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="5f877-143">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="5f877-143">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

<span data-ttu-id="5f877-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5f877-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f877-145">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="5f877-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

