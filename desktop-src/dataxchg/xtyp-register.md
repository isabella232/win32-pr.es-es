---
title: XTYP_REGISTER transacción (ddeml. h)
description: Una función de devolución de llamada de Intercambio dinámico de datos (DDE), DdeCallback, recibe el \_ tipo de transacción de registro XTYP cada vez que una aplicación de servidor de la biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función DdeNameService para registrar un nombre de servicio, o cuando se inicia una aplicación que no es de ddeml que admite el tema del sistema.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- Intercambio de datos de transacciones XTYP_REGISTER
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490072"
---
# <a name="xtyp_register-transaction"></a><span data-ttu-id="81996-104">XTYP \_ registrar transacción</span><span class="sxs-lookup"><span data-stu-id="81996-104">XTYP\_REGISTER transaction</span></span>

<span data-ttu-id="81996-105">Una función de devolución de llamada de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe el tipo de transacción de **\_ registro XTYP** cada vez que una aplicación de servidor de la biblioteca de administración de intercambio dinámico de datos (ddeml) utiliza la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar un nombre de servicio, o cuando se inicia una aplicación que no es de ddeml que admite el tema del sistema.</span><span class="sxs-lookup"><span data-stu-id="81996-105">A Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_REGISTER** transaction type whenever a Dynamic Data Exchange Management Library (DDEML) server application uses the [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) function to register a service name, or whenever a non-DDEML application that supports the System topic is started.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="81996-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81996-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81996-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="81996-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-108">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="81996-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="81996-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="81996-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-110">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="81996-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81996-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="81996-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-112">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="81996-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81996-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="81996-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-114">Identificador del nombre del servicio base que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="81996-114">A handle to the base service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="81996-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="81996-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-116">Identificador del nombre de servicio específico de la instancia que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="81996-116">A handle to the instance-specific service name being registered.</span></span>

</dd> <dt>

<span data-ttu-id="81996-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="81996-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-118">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="81996-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81996-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="81996-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-120">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="81996-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="81996-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="81996-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="81996-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="81996-122">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81996-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81996-123">Remarks</span></span>

<span data-ttu-id="81996-124">Esta transacción se filtra si la aplicación especificó la marca **CBF \_ SKIP \_ registrations** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="81996-124">This transaction is filtered if the application specified the **CBF\_SKIP\_REGISTRATIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="81996-125">Una aplicación no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .</span><span class="sxs-lookup"><span data-stu-id="81996-125">A application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

<span data-ttu-id="81996-126">Una aplicación debe usar el parámetro *hsz1* para agregar el nombre de servicio a la lista de servidores disponibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="81996-126">An application should use the *hsz1* parameter to add the service name to the list of servers available to the user.</span></span> <span data-ttu-id="81996-127">Una aplicación debe usar el parámetro *hsz2* para identificar la instancia de la aplicación que se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="81996-127">An application should use the *hsz2* parameter to identify which application instance has started.</span></span>

## <a name="requirements"></a><span data-ttu-id="81996-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81996-128">Requirements</span></span>



| <span data-ttu-id="81996-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="81996-129">Requirement</span></span> | <span data-ttu-id="81996-130">Value</span><span class="sxs-lookup"><span data-stu-id="81996-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81996-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81996-131">Minimum supported client</span></span><br/> | <span data-ttu-id="81996-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="81996-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="81996-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81996-133">Minimum supported server</span></span><br/> | <span data-ttu-id="81996-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="81996-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="81996-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81996-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="81996-136"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81996-136"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81996-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="81996-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="81996-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="81996-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81996-139">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="81996-139">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="81996-140">**DdeNameService**</span><span class="sxs-lookup"><span data-stu-id="81996-140">**DdeNameService**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

<span data-ttu-id="81996-141">**Vista**</span><span class="sxs-lookup"><span data-stu-id="81996-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="81996-142">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="81996-142">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

