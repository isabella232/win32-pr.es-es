---
title: XTYP_UNREGISTER transacción (ddeml. h)
description: Una función de devolución de llamada de Intercambio dinámico de datos (DDE), DdeCallback, recibe la \_ transacción de anulación del registro de XTYP cada vez que una aplicación de servidor de biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función DdeNameService para anular el registro de un nombre de servicio o cuando se termina una aplicación que no es de ddeml que admite el tema del sistema.
ms.assetid: a57a5d53-7919-4698-8c84-6142dd29bb2a
keywords:
- Intercambio de datos de transacciones XTYP_UNREGISTER
topic_type:
- apiref
api_name:
- XTYP_UNREGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eeba96b26c019aa0a3050a83f726745b749efa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803302"
---
# <a name="xtyp_unregister-transaction"></a><span data-ttu-id="3fc06-104">XTYP \_ anular el registro de la transacción</span><span class="sxs-lookup"><span data-stu-id="3fc06-104">XTYP\_UNREGISTER transaction</span></span>

<span data-ttu-id="3fc06-105">Una función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **\_ anulación del registro de XTYP** cada vez que una aplicación de servidor de biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para anular el registro de un nombre de servicio o cuando se termina una aplicación que no es de ddeml que admite el tema del sistema.</span><span class="sxs-lookup"><span data-stu-id="3fc06-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_UNREGISTER** transaction whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to unregister a service name, or whenever a non-DDEML application that supports the System topic is terminated.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_UNREGISTER         (0x00D0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="3fc06-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fc06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fc06-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="3fc06-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-108">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="3fc06-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="3fc06-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3fc06-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="3fc06-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3fc06-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="3fc06-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-114">Identificador del nombre del servicio base cuya registro se va a anular.</span><span class="sxs-lookup"><span data-stu-id="3fc06-114">A handle to the base service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="3fc06-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-116">Identificador del nombre del servicio específico de la instancia que se va a eliminar del registro.</span><span class="sxs-lookup"><span data-stu-id="3fc06-116">A handle to the instance-specific service name being unregistered.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="3fc06-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3fc06-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="3fc06-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3fc06-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3fc06-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="3fc06-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="3fc06-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="3fc06-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fc06-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fc06-123">Remarks</span></span>

<span data-ttu-id="3fc06-124">Esta transacción se filtra si la aplicación especificó la marca **CBF \_ SKIP \_ registrations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="3fc06-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="3fc06-125">Una aplicación no puede bloquear este tipo de transacción; \_se omite el código de retorno del bloque CBR.</span><span class="sxs-lookup"><span data-stu-id="3fc06-125">A application cannot block this transaction type; the CBR\_BLOCK return code is ignored.</span></span>

<span data-ttu-id="3fc06-126">Una aplicación debe usar el parámetro *hsz1* para quitar el nombre del servicio de la lista de servidores disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="3fc06-126">An application should use the *hsz1* parameter to remove the service name from the list of servers available to the user.</span></span> <span data-ttu-id="3fc06-127">Una aplicación debe usar el parámetro *hsz2* para identificar la instancia de la aplicación que ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="3fc06-127">An application should use the *hsz2* parameter to identify which application instance has terminated.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc06-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fc06-128">Requirements</span></span>



| <span data-ttu-id="3fc06-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fc06-129">Requirement</span></span> | <span data-ttu-id="3fc06-130">Value</span><span class="sxs-lookup"><span data-stu-id="3fc06-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc06-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fc06-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc06-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3fc06-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3fc06-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3fc06-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc06-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3fc06-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3fc06-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fc06-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc06-136"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fc06-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc06-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fc06-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="3fc06-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3fc06-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3fc06-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="3fc06-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="3fc06-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="3fc06-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="3fc06-141">**Vista**</span><span class="sxs-lookup"><span data-stu-id="3fc06-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3fc06-142">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="3fc06-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

