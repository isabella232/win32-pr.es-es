---
title: XTYP_CONNECT transacción (ddeml. h)
description: Un cliente usa la \_ transacción XTYP Connect para establecer una conversación.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Intercambio de datos de transacciones XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150418"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="dda61-104">Transacción de conexión de XTYP \_</span><span class="sxs-lookup"><span data-stu-id="dda61-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="dda61-105">Un cliente usa la transacción **XTYP \_ Connect** para establecer una conversación.</span><span class="sxs-lookup"><span data-stu-id="dda61-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="dda61-106">Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica un nombre de servicio que admite el servidor (y un nombre de tema que no es **null**) en una llamada a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="dda61-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="dda61-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dda61-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda61-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="dda61-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-109">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="dda61-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="dda61-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dda61-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="dda61-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dda61-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="dda61-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-115">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="dda61-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="dda61-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-117">Identificador del nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="dda61-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="dda61-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-119">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dda61-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="dda61-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-121">Puntero a una estructura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contiene información de contexto para la conversación.</span><span class="sxs-lookup"><span data-stu-id="dda61-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="dda61-122">Si el cliente no es una aplicación DDEML, este parámetro es 0.</span><span class="sxs-lookup"><span data-stu-id="dda61-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="dda61-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="dda61-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="dda61-124">Especifica si el cliente es la misma instancia de aplicación que el servidor.</span><span class="sxs-lookup"><span data-stu-id="dda61-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="dda61-125">Si el parámetro es 1, el cliente es la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="dda61-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="dda61-126">Si el parámetro es 0, el cliente es una instancia diferente.</span><span class="sxs-lookup"><span data-stu-id="dda61-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda61-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dda61-127">Return value</span></span>

<span data-ttu-id="dda61-128">Una función de devolución de llamada de servidor debe devolver **true** para permitir que el cliente establezca una conversación en el nombre de servicio especificado y el par de nombre de tema, o la función debe devolver **false** para denegar la conversación.</span><span class="sxs-lookup"><span data-stu-id="dda61-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="dda61-129">Si la función de devolución de llamada devuelve **true** y se establece una conversación correctamente, el sistema pasa el identificador de conversación al servidor mediante la emisión de una transacción de confirmación de conexión de XTYP a la función de devolución de llamada del servidor (a menos que el servidor haya especificado el marcador **CBF \_ SKIP \_ Connect \_** [**\_ \_ CONFIRM**](xtyp-connect-confirm.md) en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).</span><span class="sxs-lookup"><span data-stu-id="dda61-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="dda61-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dda61-130">Remarks</span></span>

<span data-ttu-id="dda61-131">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ Connections** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="dda61-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="dda61-132">Un servidor no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="dda61-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda61-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dda61-133">Requirements</span></span>



| <span data-ttu-id="dda61-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="dda61-134">Requirement</span></span> | <span data-ttu-id="dda61-135">Value</span><span class="sxs-lookup"><span data-stu-id="dda61-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dda61-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dda61-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dda61-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dda61-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dda61-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dda61-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dda61-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dda61-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="dda61-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dda61-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dda61-141"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dda61-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda61-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="dda61-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="dda61-143">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dda61-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dda61-144">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="dda61-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="dda61-145">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="dda61-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="dda61-146">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="dda61-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="dda61-147">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dda61-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dda61-148">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="dda61-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

