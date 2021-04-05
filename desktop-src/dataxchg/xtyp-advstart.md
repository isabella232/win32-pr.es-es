---
title: XTYP_ADVSTART transacción (ddeml. h)
description: Un cliente usa la \_ transacción XTYP ADVSTART para establecer un bucle de notificación con un servidor.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- Intercambio de datos de transacciones XTYP_ADVSTART
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802545"
---
# <a name="xtyp_advstart-transaction"></a><span data-ttu-id="a5c8c-104">XTYP \_ ADVSTART</span><span class="sxs-lookup"><span data-stu-id="a5c8c-104">XTYP\_ADVSTART transaction</span></span>

<span data-ttu-id="a5c8c-105">Un cliente usa la transacción **XTYP \_ ADVSTART** para establecer un bucle de notificación con un servidor.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-105">A client uses the **XTYP\_ADVSTART** transaction to establish an advise loop with a server.</span></span> <span data-ttu-id="a5c8c-106">Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica **XTYP \_ ADVSTART** como parámetro *wType* de la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .</span><span class="sxs-lookup"><span data-stu-id="a5c8c-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies **XTYP\_ADVSTART** as the *wType* parameter of the [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a><span data-ttu-id="a5c8c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5c8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5c8c-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-109">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-111">El formato de datos solicitado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-111">The data format requested by the client.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-113">Identificador de la conversación.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-113">A handle to the conversation.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-115">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-117">Identificador del nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-117">A handle to the item name.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-119">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-121">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a5c8c-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="a5c8c-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="a5c8c-123">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-123">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5c8c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5c8c-124">Return value</span></span>

<span data-ttu-id="a5c8c-125">Una función de devolución de llamada de servidor debe devolver **true** para permitir un bucle de notificaciones en el nombre de tema especificado y en el par de nombre de elemento, o **false** para denegar el bucle de notificación.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-125">A server callback function should return **TRUE** to allow an advise loop on the specified topic name and item name pair, or **FALSE** to deny the advise loop.</span></span> <span data-ttu-id="a5c8c-126">Si la función de devolución de llamada devuelve **true**, las llamadas subsiguientes a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) del servidor en el mismo nombre de tema y nombre de elemento hacen que el sistema envíe transacciones de [**XTYP \_ ADVREQ**](xtyp-advreq.md) al servidor.</span><span class="sxs-lookup"><span data-stu-id="a5c8c-126">If the callback function returns **TRUE**, any subsequent calls to the [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) function by the server on the same topic name and item name pair causes the system to send [**XTYP\_ADVREQ**](xtyp-advreq.md) transactions to the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c8c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5c8c-127">Remarks</span></span>

<span data-ttu-id="a5c8c-128">Si un cliente solicita un bucle de notificaciones en el nombre de un tema, el nombre del elemento y el formato de datos de un bucle de notificaciones que ya está establecido, la biblioteca de administración de Intercambio dinámico de datos (DDEML) no crea un bucle de notificaciones de notificación, sino que modifica las marcas de bucle de aviso (**XTYPF \_ ACKREQ** y **XTYPF \_ NoData**) para que coincidan con la solicitud más</span><span class="sxs-lookup"><span data-stu-id="a5c8c-128">If a client requests an advise loop on a topic name, item name, and data format for an advise loop that is already established, the Dynamic Data Exchange Management Library (DDEML) does not create a duplicate advise loop but instead alters the advise loop flags (**XTYPF\_ACKREQ** and **XTYPF\_NODATA**) to match the latest request.</span></span>

<span data-ttu-id="a5c8c-129">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ asesora** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="a5c8c-129">This transaction is filtered if the server application specified the **CBF\_FAIL\_ADVISES** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c8c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5c8c-130">Requirements</span></span>



| <span data-ttu-id="a5c8c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5c8c-131">Requirement</span></span> | <span data-ttu-id="a5c8c-132">Value</span><span class="sxs-lookup"><span data-stu-id="a5c8c-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c8c-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5c8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c8c-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a5c8c-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a5c8c-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5c8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c8c-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5c8c-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a5c8c-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5c8c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5c8c-138"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5c8c-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c8c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a5c8c-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="a5c8c-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="a5c8c-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a5c8c-141">**DdeClientTransaction**</span><span class="sxs-lookup"><span data-stu-id="a5c8c-141">**DdeClientTransaction**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[<span data-ttu-id="a5c8c-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="a5c8c-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="a5c8c-143">**DdePostAdvise**</span><span class="sxs-lookup"><span data-stu-id="a5c8c-143">**DdePostAdvise**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

<span data-ttu-id="a5c8c-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="a5c8c-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a5c8c-145">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="a5c8c-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

