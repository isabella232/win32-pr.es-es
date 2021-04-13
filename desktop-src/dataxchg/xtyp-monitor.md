---
title: XTYP_MONITOR transacción (ddeml. h)
description: Una función de devolución de llamada DDE del depurador de Intercambio dinámico de datos (DDE), DdeCallback, recibe la transacción de XTYP \_ monitor cada vez que se produce un evento DDE en el sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Intercambio de datos de transacciones XTYP_MONITOR
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422201"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="dd5b3-104">Transacción de supervisión de XTYP \_</span><span class="sxs-lookup"><span data-stu-id="dd5b3-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="dd5b3-105">Una función de devolución de llamada DDE del depurador de Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción de **XTYP \_ monitor** cada vez que se produce un evento DDE en el sistema.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="dd5b3-106">Para recibir esta transacción, una aplicación debe especificar el valor del **\_ monitor APPCLASS** cuando llama a la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="dd5b3-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="dd5b3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd5b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd5b3-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-109">El tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-111">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-117">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-119">Identificador de un objeto DDE que contiene información sobre el evento DDE.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="dd5b3-120">La aplicación debe usar la función [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obtener un puntero al objeto.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-122">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd5b3-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="dd5b3-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="dd5b3-124">El evento DDE.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-124">The DDE event.</span></span> <span data-ttu-id="dd5b3-125">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="dd5b3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dd5b3-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="dd5b3-127">Significado</span><span class="sxs-lookup"><span data-stu-id="dd5b3-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="dd5b3-128"><dt>**MF \_ Devoluciones de llamada**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="dd5b3-129">El sistema envió una transacción a una función de devolución de llamada DDE.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="dd5b3-130">El objeto DDE contiene una estructura [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) que proporciona información sobre la transacción.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="dd5b3-131"><dt>**MF \_ CONV**</dt> <dt></dt> .</span><span class="sxs-lookup"><span data-stu-id="dd5b3-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="dd5b3-132">Una conversación DDE se estableció o finalizó.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="dd5b3-133">El objeto DDE contiene una estructura [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) que proporciona información sobre la conversación.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="dd5b3-134"><dt>**MF \_ ERRORES**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="dd5b3-135">Error de DDE.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-135">A DDE error occurred.</span></span> <span data-ttu-id="dd5b3-136">El objeto DDE contiene una estructura [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) que proporciona información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="dd5b3-137"><dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="dd5b3-138">Una aplicación DDE creada, liberada o incrementada el recuento de uso de un identificador de cadena o un identificador de cadena se liberó como resultado de una llamada a la función [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="dd5b3-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="dd5b3-139">El objeto DDE contiene una estructura [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) que proporciona información sobre el identificador de cadena.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="dd5b3-140"><dt>**MF \_ VÍNCULOS**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="dd5b3-141">Una aplicación DDE inició o detuvo un bucle de notificación.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="dd5b3-142">El objeto DDE contiene una estructura [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) que proporciona información sobre el bucle de notificación.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="dd5b3-143"><dt>**MF \_ POSTMSGS**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="dd5b3-144">El sistema o una aplicación publicaron un mensaje DDE.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="dd5b3-145">El objeto DDE contiene una estructura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que proporciona información sobre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="dd5b3-146"><dt>**MF \_ SENDMSGS**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="dd5b3-147">El sistema o una aplicación enviaron un mensaje DDE.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="dd5b3-148">El objeto DDE contiene una estructura [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que proporciona información sobre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd5b3-149">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd5b3-149">Return value</span></span>

<span data-ttu-id="dd5b3-150">Si la función de devolución de llamada procesa esta transacción, debe devolver 0.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5b3-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd5b3-151">Requirements</span></span>



| <span data-ttu-id="dd5b3-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd5b3-152">Requirement</span></span> | <span data-ttu-id="dd5b3-153">Value</span><span class="sxs-lookup"><span data-stu-id="dd5b3-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd5b3-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd5b3-154">Minimum supported client</span></span><br/> | <span data-ttu-id="dd5b3-155">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd5b3-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dd5b3-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd5b3-156">Minimum supported server</span></span><br/> | <span data-ttu-id="dd5b3-157">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd5b3-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="dd5b3-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd5b3-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd5b3-159"><dt>Ddeml. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd5b3-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd5b3-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd5b3-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd5b3-161">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dd5b3-162">**DdeAccessData**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="dd5b3-163">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="dd5b3-164">**DdeUninitialize**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="dd5b3-165">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="dd5b3-166">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="dd5b3-167">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="dd5b3-168">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="dd5b3-169">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="dd5b3-170">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="dd5b3-171">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dd5b3-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dd5b3-172">Biblioteca de administración de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="dd5b3-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

