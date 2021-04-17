---
title: XTYP_ADVREQ transacción (ddeml. h)
description: La \_ transacción XTYP ADVREQ informa al servidor de que una transacción de notificación está pendiente en el par nombre de tema y nombre de elemento especificado y que han cambiado los datos correspondientes a los pares nombre de tema y nombre de elemento.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- Intercambio de datos de transacciones XTYP_ADVREQ
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422375"
---
# <a name="xtyp_advreq-transaction"></a><span data-ttu-id="1f84c-104">XTYP \_ ADVREQ</span><span class="sxs-lookup"><span data-stu-id="1f84c-104">XTYP\_ADVREQ transaction</span></span>

<span data-ttu-id="1f84c-105">La transacción **XTYP \_ ADVREQ** informa al servidor de que una transacción de notificación está pendiente en el par nombre de tema y nombre de elemento especificado y que han cambiado los datos correspondientes a los pares nombre de tema y nombre de elemento.</span><span class="sxs-lookup"><span data-stu-id="1f84c-105">The **XTYP\_ADVREQ** transaction informs the server that an advise transaction is outstanding on the specified topic name and item name pair and that data corresponding to the topic name and item name pair has changed.</span></span> <span data-ttu-id="1f84c-106">El sistema envía esta transacción a la función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), una vez que el servidor llama a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="1f84c-106">The system sends this transaction to the Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), after the server calls the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a><span data-ttu-id="1f84c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f84c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f84c-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="1f84c-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-109">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="1f84c-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="1f84c-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-111">Formato en el que se deben enviar los datos al cliente.</span><span class="sxs-lookup"><span data-stu-id="1f84c-111">The format in which the data should be submitted to the client.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="1f84c-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-113">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="1f84c-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="1f84c-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-115">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="1f84c-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="1f84c-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-117">Identificador del nombre del elemento que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1f84c-117">A handle to the item name that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="1f84c-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-119">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1f84c-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="1f84c-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-121">El recuento, en la palabra de orden inferior, de las transacciones de **XTYP \_ ADVREQ** que quedan por procesarse en el mismo tema, elemento y nombre de formato establecidos en el contexto de la llamada actual a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .</span><span class="sxs-lookup"><span data-stu-id="1f84c-121">The count, in the low-order word, of **XTYP\_ADVREQ** transactions that remain to be processed on the same topic, item, and format name set within the context of the current call to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function.</span></span> <span data-ttu-id="1f84c-122">El recuento es cero si la transacción actual de **XTYP \_ ADVREQ** es la última.</span><span class="sxs-lookup"><span data-stu-id="1f84c-122">The count is zero if the current **XTYP\_ADVREQ** transaction is the last one.</span></span> <span data-ttu-id="1f84c-123">Un servidor puede usar este recuento para determinar si se debe crear un identificador de datos de **HDATA \_ APPOWNED** para los datos de notificación.</span><span class="sxs-lookup"><span data-stu-id="1f84c-123">A server can use this count to determine whether to create an **HDATA\_APPOWNED** data handle to the advise data.</span></span>

<span data-ttu-id="1f84c-124">La palabra de orden inferior se establece en **CADV \_ LATEACK** si el objeto ddeml emitió la transacción **XTYP \_ ADVREQ** debido a un mensaje de confirmación de DDE de llegada tardía \_ desde un cliente que se Outrun por el servidor.</span><span class="sxs-lookup"><span data-stu-id="1f84c-124">The low-order word is set to **CADV\_LATEACK** if the DDEML issued the **XTYP\_ADVREQ** transaction because of a late-arriving DDE\_ACK message from a client being outrun by the server.</span></span>

<span data-ttu-id="1f84c-125">No se usa la palabra de orden superior.</span><span class="sxs-lookup"><span data-stu-id="1f84c-125">The high-order word is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f84c-126">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="1f84c-126">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="1f84c-127">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1f84c-127">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f84c-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f84c-128">Return value</span></span>

<span data-ttu-id="1f84c-129">El servidor debe llamar primero a la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para crear un identificador de datos que identifique los datos modificados y, a continuación, devuelva el identificador.</span><span class="sxs-lookup"><span data-stu-id="1f84c-129">The server should first call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the changed data and then return the handle.</span></span> <span data-ttu-id="1f84c-130">El servidor debe devolver **null** si no puede completar la transacción.</span><span class="sxs-lookup"><span data-stu-id="1f84c-130">The server should return **NULL** if it is unable to complete the transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f84c-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f84c-131">Remarks</span></span>

<span data-ttu-id="1f84c-132">Un servidor no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="1f84c-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f84c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f84c-133">Requirements</span></span>



| <span data-ttu-id="1f84c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f84c-134">Requirement</span></span> | <span data-ttu-id="1f84c-135">Value</span><span class="sxs-lookup"><span data-stu-id="1f84c-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f84c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f84c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1f84c-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1f84c-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f84c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f84c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1f84c-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f84c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="1f84c-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f84c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f84c-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f84c-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f84c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f84c-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f84c-143">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1f84c-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f84c-144">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="1f84c-144">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="1f84c-145">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="1f84c-145">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="1f84c-146">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="1f84c-146">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="1f84c-147">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1f84c-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1f84c-148">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="1f84c-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

