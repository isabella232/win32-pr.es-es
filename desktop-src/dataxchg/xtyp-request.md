---
title: XTYP_REQUEST transacción (ddeml. h)
description: Un cliente usa la \_ transacción de solicitud XTYP para solicitar datos de un servidor. Una función de devolución de llamada del servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe esta transacción cuando un cliente especifica XTYP \_ solicitud en la función DdeClientTransaction.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- Intercambio de datos de transacciones XTYP_REQUEST
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801394"
---
# <a name="xtyp_request-transaction"></a><span data-ttu-id="546dd-105">Transacción de solicitud de XTYP \_</span><span class="sxs-lookup"><span data-stu-id="546dd-105">XTYP\_REQUEST transaction</span></span>

<span data-ttu-id="546dd-106">Un cliente usa la transacción de **\_ solicitud XTYP** para solicitar datos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="546dd-106">A client uses the **XTYP\_REQUEST** transaction to request data from a server.</span></span> <span data-ttu-id="546dd-107">Una función de devolución de llamada del servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ solicitud** en la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="546dd-107">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_REQUEST** in the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a><span data-ttu-id="546dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="546dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="546dd-109">*uType*</span><span class="sxs-lookup"><span data-stu-id="546dd-109">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-110">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="546dd-110">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-111">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="546dd-111">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-112">Formato en el que el servidor debe enviar datos al cliente.</span><span class="sxs-lookup"><span data-stu-id="546dd-112">The format in which the server should submit data to the client.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-113">*hconv*</span><span class="sxs-lookup"><span data-stu-id="546dd-113">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-114">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="546dd-114">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-115">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="546dd-115">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-116">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="546dd-116">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="546dd-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-118">Identificador del nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="546dd-118">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-119">*hdata*</span><span class="sxs-lookup"><span data-stu-id="546dd-119">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="546dd-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="546dd-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="546dd-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="546dd-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="546dd-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="546dd-124">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="546dd-124">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="546dd-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="546dd-125">Return value</span></span>

<span data-ttu-id="546dd-126">El servidor debe llamar a la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para crear un identificador de datos que identifique los datos y, a continuación, devuelva el identificador.</span><span class="sxs-lookup"><span data-stu-id="546dd-126">The server should call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function to create a data handle that identifies the data and then return the handle.</span></span> <span data-ttu-id="546dd-127">El servidor debe devolver **null** si no puede completar la transacción.</span><span class="sxs-lookup"><span data-stu-id="546dd-127">The server should return **NULL** if it is unable to complete the transaction.</span></span> <span data-ttu-id="546dd-128">Si el servidor devuelve **null**, el cliente recibirá una \_ marca de FNOTPROCESSED DDE.</span><span class="sxs-lookup"><span data-stu-id="546dd-128">If the server returns **NULL**, the client will receive a DDE\_FNOTPROCESSED flag.</span></span>

## <a name="remarks"></a><span data-ttu-id="546dd-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="546dd-129">Remarks</span></span>

<span data-ttu-id="546dd-130">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ requests** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="546dd-130">This transaction is filtered if the server application specified the **CBF\_FAIL\_REQUESTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="546dd-131">Si la respuesta a esta transacción requiere un procesamiento prolongado, el servidor puede devolver el \_ código de retorno del bloque CBR para suspender las transacciones futuras en la conversación actual y, después, procesar la transacción de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="546dd-131">If responding to this transaction requires lengthy processing, the server can return the CBR\_BLOCK return code to suspend future transactions on the current conversation and then process the transaction asynchronously.</span></span> <span data-ttu-id="546dd-132">Cuando el servidor ha finalizado y los datos están listos para pasar al cliente, el servidor puede llamar a la función [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) para reanudar la conversación.</span><span class="sxs-lookup"><span data-stu-id="546dd-132">When the server has finished and the data is ready to pass to the client, the server can call the [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) function to resume the conversation.</span></span>

## <a name="requirements"></a><span data-ttu-id="546dd-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="546dd-133">Requirements</span></span>



| <span data-ttu-id="546dd-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="546dd-134">Requirement</span></span> | <span data-ttu-id="546dd-135">Value</span><span class="sxs-lookup"><span data-stu-id="546dd-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="546dd-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="546dd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="546dd-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="546dd-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="546dd-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="546dd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="546dd-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="546dd-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="546dd-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="546dd-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="546dd-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="546dd-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="546dd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="546dd-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="546dd-143">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="546dd-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="546dd-144">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="546dd-144">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="546dd-145">**DdeCreateDataHandle**</span><span class="sxs-lookup"><span data-stu-id="546dd-145">**DdeCreateDataHandle**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[<span data-ttu-id="546dd-146">**DdeEnableCallback**</span><span class="sxs-lookup"><span data-stu-id="546dd-146">**DdeEnableCallback**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[<span data-ttu-id="546dd-147">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="546dd-147">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="546dd-148">**Vista**</span><span class="sxs-lookup"><span data-stu-id="546dd-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="546dd-149">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="546dd-149">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

