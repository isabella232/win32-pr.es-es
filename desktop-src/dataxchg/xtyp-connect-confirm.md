---
title: XTYP_CONNECT_CONFIRM transacción (ddeml. h)
description: Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), DdeCallback, recibe la transacción de confirmación de XTYP \_ Connect \_ para confirmar que se ha establecido una conversación con un cliente y para proporcionar al servidor el identificador de conversación.
ms.assetid: 4db67539-9322-44d7-bf2b-749bd6cfcbb4
keywords:
- Intercambio de datos de transacciones XTYP_CONNECT_CONFIRM
topic_type:
- apiref
api_name:
- XTYP_CONNECT_CONFIRM
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e880dfffc7f7825c99ab9e4e3bf980baa978b786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422373"
---
# <a name="xtyp_connect_confirm-transaction"></a><span data-ttu-id="4da1e-104">XTYP \_ conectar \_ confirmar transacción</span><span class="sxs-lookup"><span data-stu-id="4da1e-104">XTYP\_CONNECT\_CONFIRM transaction</span></span>

<span data-ttu-id="4da1e-105">Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **confirmación de XTYP \_ Connect \_** para confirmar que se ha establecido una conversación con un cliente y para proporcionar al servidor el identificador de conversación.</span><span class="sxs-lookup"><span data-stu-id="4da1e-105">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_CONNECT\_CONFIRM** transaction to confirm that a conversation has been established with a client and to provide the server with the conversation handle.</span></span> <span data-ttu-id="4da1e-106">El sistema envía esta transacción como resultado de una transacción [**XTYP \_ Connect**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="4da1e-106">The system sends this transaction as a result of a previous [**XTYP\_CONNECT**](xtyp-connect.md) or [**XTYP\_WILDCONNECT**](xtyp-wildconnect.md) transaction.</span></span>


```C++
#define     XTYPF_NOBLOCK            0x0002
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_CONNECT_CONFIRM    (0x0070 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="4da1e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4da1e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da1e-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="4da1e-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-109">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="4da1e-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="4da1e-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4da1e-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="4da1e-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-113">Identificador de la nueva conversación.</span><span class="sxs-lookup"><span data-stu-id="4da1e-113">A handle to the new conversation.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="4da1e-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-115">Identificador del nombre del tema en el que se ha establecido la conversación.</span><span class="sxs-lookup"><span data-stu-id="4da1e-115">A handle to the topic name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="4da1e-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-117">Identificador del nombre del servicio en el que se ha establecido la conversación.</span><span class="sxs-lookup"><span data-stu-id="4da1e-117">A handle to the service name on which the conversation has been established.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="4da1e-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-119">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4da1e-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="4da1e-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-121">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="4da1e-121">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4da1e-122">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="4da1e-122">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="4da1e-123">Especifica si el cliente es la misma instancia de aplicación que el servidor.</span><span class="sxs-lookup"><span data-stu-id="4da1e-123">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="4da1e-124">Si el parámetro es 1, el cliente es la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="4da1e-124">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="4da1e-125">Si el parámetro es 0, el cliente es una instancia diferente.</span><span class="sxs-lookup"><span data-stu-id="4da1e-125">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4da1e-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4da1e-126">Remarks</span></span>

<span data-ttu-id="4da1e-127">Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ SKIP \_ Connect \_ Confirmations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="4da1e-127">This transaction is filtered if the server application specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="4da1e-128">Un servidor no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="4da1e-128">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da1e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da1e-129">Requirements</span></span>



| <span data-ttu-id="4da1e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da1e-130">Requirement</span></span> | <span data-ttu-id="4da1e-131">Value</span><span class="sxs-lookup"><span data-stu-id="4da1e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4da1e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4da1e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4da1e-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4da1e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4da1e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4da1e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4da1e-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4da1e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4da1e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4da1e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da1e-137"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4da1e-137"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da1e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4da1e-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="4da1e-139">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="4da1e-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4da1e-140">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="4da1e-140">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="4da1e-141">**DdeConnectList**</span><span class="sxs-lookup"><span data-stu-id="4da1e-141">**DdeConnectList**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist)
</dt> <dt>

[<span data-ttu-id="4da1e-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="4da1e-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="4da1e-143">**Vista**</span><span class="sxs-lookup"><span data-stu-id="4da1e-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4da1e-144">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="4da1e-144">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

