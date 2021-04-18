---
title: XTYP_WILDCONNECT transacción (ddeml. h)
description: Permite a un cliente establecer una conversación en cada uno de los pares nombre de servicio y nombre de tema del servidor que coinciden con el nombre de servicio y el nombre de tema especificados.
ms.assetid: 4651e14f-ca13-412e-853d-326a13db78e4
keywords:
- Intercambio de datos de transacciones XTYP_WILDCONNECT
topic_type:
- apiref
api_name:
- XTYP_WILDCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc63d6c367aebc440418beaabb0a06f05b0df967
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705135"
---
# <a name="xtyp_wildconnect-transaction"></a><span data-ttu-id="d98eb-104">XTYP \_ WILDCONNECT</span><span class="sxs-lookup"><span data-stu-id="d98eb-104">XTYP\_WILDCONNECT transaction</span></span>

<span data-ttu-id="d98eb-105">Permite a un cliente establecer una conversación en cada uno de los pares nombre de servicio y nombre de tema del servidor que coinciden con el nombre de servicio y el nombre de tema especificados.</span><span class="sxs-lookup"><span data-stu-id="d98eb-105">Enables a client to establish a conversation on each of the server's service name and topic name pairs that match the specified service name and topic name.</span></span> <span data-ttu-id="d98eb-106">Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica un nombre de servicio **nulo** , un nombre de tema **nulo** o ambos en una llamada a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) .</span><span class="sxs-lookup"><span data-stu-id="d98eb-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a **NULL** service name, a **NULL** topic name, or both in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) or [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) function.</span></span>


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_WILDCONNECT        (0x00E0 | XCLASS_DATA | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="d98eb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d98eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98eb-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="d98eb-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-109">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="d98eb-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="d98eb-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d98eb-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="d98eb-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d98eb-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="d98eb-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-115">Identificador del nombre del tema.</span><span class="sxs-lookup"><span data-stu-id="d98eb-115">A handle to the topic name.</span></span> <span data-ttu-id="d98eb-116">Si este parámetro es **null**, el cliente solicita una conversación en todos los nombres de tema admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="d98eb-116">If this parameter is **NULL**, the client is requesting a conversation on all topic names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-117">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="d98eb-117">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-118">Identificador del nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="d98eb-118">A handle to the service name.</span></span> <span data-ttu-id="d98eb-119">Si este parámetro es **null**, el cliente solicita una conversación en todos los nombres de servicio admitidos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="d98eb-119">If this parameter is **NULL**, the client is requesting a conversation on all service names that the server supports.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-120">*hdata*</span><span class="sxs-lookup"><span data-stu-id="d98eb-120">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-121">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d98eb-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-122">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="d98eb-122">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-123">Puntero a una estructura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contiene información de contexto para la conversación.</span><span class="sxs-lookup"><span data-stu-id="d98eb-123">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="d98eb-124">Si el cliente no es una aplicación DDEML, este parámetro se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="d98eb-124">If the client is not a DDEML application, this parameter is set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="d98eb-125">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="d98eb-125">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="d98eb-126">Especifica si el cliente es la misma instancia de aplicación que el servidor.</span><span class="sxs-lookup"><span data-stu-id="d98eb-126">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="d98eb-127">Si el parámetro es 1, el cliente es la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="d98eb-127">If the parameter is 1, the client is same instance.</span></span> <span data-ttu-id="d98eb-128">Si el parámetro es 0, el cliente es una instancia diferente.</span><span class="sxs-lookup"><span data-stu-id="d98eb-128">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98eb-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d98eb-129">Return value</span></span>

<span data-ttu-id="d98eb-130">El servidor debe devolver un identificador de datos que identifique una matriz de estructuras [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) .</span><span class="sxs-lookup"><span data-stu-id="d98eb-130">The server should return a data handle that identifies an array of [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair) structures.</span></span> <span data-ttu-id="d98eb-131">La matriz debe contener una estructura para cada par de nombre de servicio y nombre de tema que coincida con el par de nombre de servicio y nombre de tema solicitado por el cliente.</span><span class="sxs-lookup"><span data-stu-id="d98eb-131">The array should contain one structure for each service-name and topic-name pair that matches the service-name and topic-name pair requested by the client.</span></span> <span data-ttu-id="d98eb-132">La matriz debe terminar con un identificador de cadena **null** .</span><span class="sxs-lookup"><span data-stu-id="d98eb-132">The array must be terminated by a **NULL** string handle.</span></span> <span data-ttu-id="d98eb-133">El sistema envía la transacción de [**\_ \_ confirmación de conexión de XTYP**](xtyp-connect-confirm.md) al servidor para confirmar cada conversación y pasar los identificadores de conversación al servidor.</span><span class="sxs-lookup"><span data-stu-id="d98eb-133">The system sends the [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server to confirm each conversation and to pass the conversation handles to the server.</span></span> <span data-ttu-id="d98eb-134">El servidor no recibirá estas confirmaciones si especificó la marca **CBF \_ SKIP \_ Connect \_ Confirmations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="d98eb-134">The server will not receive these confirmations if it specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="d98eb-135">El servidor debe devolver **null** para rechazar la transacción **XTYP \_ WILDCONNECT** .</span><span class="sxs-lookup"><span data-stu-id="d98eb-135">The server should return **NULL** to refuse the **XTYP\_WILDCONNECT** transaction.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98eb-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d98eb-136">Remarks</span></span>

<span data-ttu-id="d98eb-137">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ Connections** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="d98eb-137">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="d98eb-138">Un servidor no puede bloquear este tipo de transacción; \_se omite el código de retorno del bloque CBR.</span><span class="sxs-lookup"><span data-stu-id="d98eb-138">A server cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d98eb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d98eb-139">Requirements</span></span>



| <span data-ttu-id="d98eb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98eb-140">Requirement</span></span> | <span data-ttu-id="d98eb-141">Value</span><span class="sxs-lookup"><span data-stu-id="d98eb-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d98eb-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d98eb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d98eb-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d98eb-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d98eb-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d98eb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d98eb-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d98eb-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d98eb-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d98eb-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d98eb-147"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d98eb-147"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98eb-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="d98eb-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="d98eb-149">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d98eb-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d98eb-150">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d98eb-150">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="d98eb-151">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="d98eb-151">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="d98eb-152">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="d98eb-152">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="d98eb-153">**HSZPAIR**</span><span class="sxs-lookup"><span data-stu-id="d98eb-153">**HSZPAIR**</span></span>](/windows/win32/api/ddeml/ns-ddeml-hszpair)
</dt> <dt>

<span data-ttu-id="d98eb-154">**Vista**</span><span class="sxs-lookup"><span data-stu-id="d98eb-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d98eb-155">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="d98eb-155">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

