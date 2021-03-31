---
title: XTYP_DISCONNECT transacción (ddeml. h)
description: La función de devolución de llamada de Intercambio dinámico de datos de la aplicación (DDE), DdeCallback, recibe la \_ transacción XTYP Disconnect cuando el asociado de la aplicación en una conversación usa la función DdeDisconnect para finalizar la conversación.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Intercambio de datos de transacciones XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801399"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="ae184-104">XTYP \_ desconectar transacción</span><span class="sxs-lookup"><span data-stu-id="ae184-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="ae184-105">La función de devolución de llamada de Intercambio dinámico de datos de la aplicación (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción **XTYP \_ Disconnect** cuando el asociado de la aplicación en una conversación usa la función [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) para finalizar la conversación.</span><span class="sxs-lookup"><span data-stu-id="ae184-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="ae184-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae184-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae184-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="ae184-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-108">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="ae184-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="ae184-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ae184-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="ae184-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-112">Identificador de que se ha terminado la conversación.</span><span class="sxs-lookup"><span data-stu-id="ae184-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="ae184-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-114">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ae184-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="ae184-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-116">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ae184-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="ae184-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ae184-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="ae184-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="ae184-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae184-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="ae184-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="ae184-122">Especifica si los asociados de la conversación son la misma instancia de aplicación.</span><span class="sxs-lookup"><span data-stu-id="ae184-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="ae184-123">Si este parámetro es 1, los asociados son la misma instancia.</span><span class="sxs-lookup"><span data-stu-id="ae184-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="ae184-124">Si este parámetro es 0, los asociados son instancias diferentes.</span><span class="sxs-lookup"><span data-stu-id="ae184-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae184-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae184-125">Remarks</span></span>

<span data-ttu-id="ae184-126">Esta transacción se filtra si la aplicación especificó la marca **CBF \_ SKIP \_ desconnects** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="ae184-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="ae184-127">La aplicación puede obtener el estado de la conversación terminada llamando a la función [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) mientras procesa esta transacción.</span><span class="sxs-lookup"><span data-stu-id="ae184-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="ae184-128">El identificador de conversación deja de ser válido después de que la función de devolución de llamada vuelva.</span><span class="sxs-lookup"><span data-stu-id="ae184-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="ae184-129">Una aplicación no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="ae184-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae184-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae184-130">Requirements</span></span>



| <span data-ttu-id="ae184-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae184-131">Requirement</span></span> | <span data-ttu-id="ae184-132">Value</span><span class="sxs-lookup"><span data-stu-id="ae184-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae184-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae184-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ae184-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ae184-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae184-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae184-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ae184-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae184-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ae184-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae184-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae184-138"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae184-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae184-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae184-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="ae184-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ae184-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ae184-141">**DdeDisconnect**</span><span class="sxs-lookup"><span data-stu-id="ae184-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="ae184-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="ae184-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="ae184-143">**DdeQueryConvInfo**</span><span class="sxs-lookup"><span data-stu-id="ae184-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="ae184-144">**Vista**</span><span class="sxs-lookup"><span data-stu-id="ae184-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ae184-145">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="ae184-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

