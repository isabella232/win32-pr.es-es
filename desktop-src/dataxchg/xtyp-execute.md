---
title: XTYP_EXECUTE transacción (ddeml. h)
description: Un cliente usa la \_ transacción de ejecución XTYP para enviar una cadena de comandos al servidor. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP \_ Execute en la función DdeClientTransaction.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- Intercambio de datos de transacciones XTYP_EXECUTE
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079627"
---
# <a name="xtyp_execute-transaction"></a><span data-ttu-id="567ef-105">XTYP \_ Ejecutar transacción</span><span class="sxs-lookup"><span data-stu-id="567ef-105">XTYP\_EXECUTE transaction</span></span>

<span data-ttu-id="567ef-106">Un cliente usa la transacción de **\_ ejecución XTYP** para enviar una cadena de comandos al servidor.</span><span class="sxs-lookup"><span data-stu-id="567ef-106">A client uses the **XTYP\_EXECUTE** transaction to send a command string to the server.</span></span> <span data-ttu-id="567ef-107">Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ Execute** en la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="567ef-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_EXECUTE** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a><span data-ttu-id="567ef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="567ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="567ef-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="567ef-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-110">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="567ef-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="567ef-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="567ef-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="567ef-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-114">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="567ef-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="567ef-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-116">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="567ef-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="567ef-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="567ef-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="567ef-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-120">Identificador de la cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="567ef-120">A handle to the command string.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="567ef-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="567ef-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="567ef-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="567ef-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="567ef-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="567ef-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="567ef-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="567ef-125">Return value</span></span>

<span data-ttu-id="567ef-126">Una función de devolución de llamada de servidor debe devolver **DDE \_ Fack** si procesa esta transacción, **DDE \_ FBUSY** si está demasiado ocupado para procesar esta transacción o **\_ FNOTPROCESSED de DDE** si rechaza esta transacción.</span><span class="sxs-lookup"><span data-stu-id="567ef-126">A server callback function should return **DDE\_FACK** if it processes this transaction, **DDE\_FBUSY** if it is too busy to process this transaction, or **DDE\_FNOTPROCESSED** if it rejects this transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="567ef-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="567ef-127">Remarks</span></span>

<span data-ttu-id="567ef-128">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ executes** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="567ef-128">This transaction is filtered if the server application specified the **CBF\_FAIL\_EXECUTES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="567ef-129">Una aplicación debe liberar el identificador de datos obtenido durante esta transacción.</span><span class="sxs-lookup"><span data-stu-id="567ef-129">An application must free the data handle obtained during this transaction.</span></span> <span data-ttu-id="567ef-130">Sin embargo, una aplicación debe copiar la cadena de comandos asociada al identificador de datos si la aplicación debe procesar la cadena después de que la función de devolución de llamada vuelva.</span><span class="sxs-lookup"><span data-stu-id="567ef-130">An application must, however, copy the command string associated with the data handle if the application must process the string after the callback function returns.</span></span> <span data-ttu-id="567ef-131">Una aplicación puede usar la función [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) para copiar los datos.</span><span class="sxs-lookup"><span data-stu-id="567ef-131">An application can use the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function to copy the data.</span></span>

<span data-ttu-id="567ef-132">Dado que la mayoría de las aplicaciones cliente esperan que una aplicación de servidor realice sincrónicamente una transacción de **\_ ejecución XTYP** , un servidor debe intentar realizar todo el procesamiento de la transacción de **\_ ejecución XTYP** desde la función de devolución de llamada DDE o devolviendo el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="567ef-132">Because most client applications expect a server application to perform an **XTYP\_EXECUTE** transaction synchronously, a server should attempt to perform all processing of the **XTYP\_EXECUTE** transaction either from within the DDE callback function or by returning the **CBR\_BLOCK** return code.</span></span> <span data-ttu-id="567ef-133">Si el parámetro *hdata* es un comando que indica al servidor que finalice, el servidor debe hacerlo después de procesar la transacción **de \_ ejecución XTYP** .</span><span class="sxs-lookup"><span data-stu-id="567ef-133">If the *hdata* parameter is a command that instructs the server to terminate, the server should do so after processing the **XTYP\_EXECUTE** transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="567ef-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="567ef-134">Requirements</span></span>



| <span data-ttu-id="567ef-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="567ef-135">Requirement</span></span> | <span data-ttu-id="567ef-136">Value</span><span class="sxs-lookup"><span data-stu-id="567ef-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="567ef-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="567ef-137">Minimum supported client</span></span><br/> | <span data-ttu-id="567ef-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="567ef-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="567ef-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="567ef-139">Minimum supported server</span></span><br/> | <span data-ttu-id="567ef-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="567ef-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="567ef-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="567ef-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="567ef-142"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="567ef-142"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="567ef-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="567ef-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="567ef-144">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="567ef-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="567ef-145">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="567ef-145">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="567ef-146">**DdeGetData**</span><span class="sxs-lookup"><span data-stu-id="567ef-146">**DdeGetData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[<span data-ttu-id="567ef-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="567ef-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="567ef-148">**Vista**</span><span class="sxs-lookup"><span data-stu-id="567ef-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="567ef-149">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="567ef-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

