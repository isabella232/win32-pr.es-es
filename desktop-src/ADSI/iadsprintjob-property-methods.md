---
title: Métodos de la propiedad IADsPrintJob (iAds. h)
description: Los métodos de propiedad de la interfaz IADsPrintJob obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPrintJob ADSI
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492011"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="601d1-105">Métodos de propiedad IADsPrintJob</span><span class="sxs-lookup"><span data-stu-id="601d1-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="601d1-106">Los métodos de propiedad de la interfaz [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="601d1-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="601d1-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="601d1-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="601d1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="601d1-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="601d1-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="601d1-109">**Description**</span></span>
<span data-ttu-id="601d1-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-111">La descripción del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="601d1-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="601d1-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="601d1-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="601d1-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-114">**HostPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="601d1-114">**HostPrintQueue**</span></span>
<span data-ttu-id="601d1-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-116">Cadena ADsPath de la cola de impresión que procesa el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="601d1-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="601d1-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="601d1-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="601d1-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-119">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="601d1-119">**Notify**</span></span>
<span data-ttu-id="601d1-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-121">El usuario al que se va a notificar cuando se complete el trabajo.</span><span class="sxs-lookup"><span data-stu-id="601d1-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="601d1-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="601d1-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="601d1-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="601d1-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-124">**NotifyPath**</span><span class="sxs-lookup"><span data-stu-id="601d1-124">**NotifyPath**</span></span>
<span data-ttu-id="601d1-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-126">Cadena ADsPath del objeto de usuario al que se va a notificar cuando se complete el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="601d1-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="601d1-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="601d1-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="601d1-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-129">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="601d1-129">**Priority**</span></span>
<span data-ttu-id="601d1-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-131">Prioridad del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="601d1-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="601d1-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="601d1-133">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="601d1-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-134">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="601d1-134">**Size**</span></span>
<span data-ttu-id="601d1-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-136">Tamaño, en bytes, del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="601d1-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="601d1-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="601d1-138">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="601d1-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="601d1-139">**StartTime**</span></span>
<span data-ttu-id="601d1-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-141">Hora más temprana en la que se debe iniciar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="601d1-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="601d1-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="601d1-143">Tipo de datos de scripting: **fecha**</span><span class="sxs-lookup"><span data-stu-id="601d1-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-144">**TimeSubmitted**</span><span class="sxs-lookup"><span data-stu-id="601d1-144">**TimeSubmitted**</span></span>
<span data-ttu-id="601d1-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-146">La hora a la que se envió el trabajo a la cola.</span><span class="sxs-lookup"><span data-stu-id="601d1-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="601d1-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="601d1-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="601d1-148">Tipo de datos de scripting: **fecha**</span><span class="sxs-lookup"><span data-stu-id="601d1-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="601d1-149">**TotalPages**</span></span>
<span data-ttu-id="601d1-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-151">Número total de páginas en el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="601d1-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="601d1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="601d1-153">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="601d1-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-154">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="601d1-154">**UntilTime**</span></span>
<span data-ttu-id="601d1-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-156">La hora más reciente en la que se debe iniciar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="601d1-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="601d1-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="601d1-158">Tipo de datos de scripting: **fecha**</span><span class="sxs-lookup"><span data-stu-id="601d1-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-159">**User**</span><span class="sxs-lookup"><span data-stu-id="601d1-159">**User**</span></span>
<span data-ttu-id="601d1-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-161">Nombre del usuario que envió el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="601d1-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="601d1-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="601d1-163">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="601d1-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="601d1-164">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="601d1-164">**UserPath**</span></span>
<span data-ttu-id="601d1-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="601d1-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="601d1-166">Cadena ADsPath del objeto de usuario que envió este trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="601d1-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="601d1-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="601d1-168">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="601d1-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="601d1-169">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="601d1-169">Examples</span></span>

<span data-ttu-id="601d1-170">En el ejemplo de código siguiente se muestra cómo trabajar con las propiedades de un objeto de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="601d1-171">En el ejemplo de código siguiente se muestra cómo trabajar con las propiedades de un objeto de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="601d1-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="601d1-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="601d1-172">Requirements</span></span>



| <span data-ttu-id="601d1-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="601d1-173">Requirement</span></span> | <span data-ttu-id="601d1-174">Value</span><span class="sxs-lookup"><span data-stu-id="601d1-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="601d1-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="601d1-175">Minimum supported client</span></span><br/> | <span data-ttu-id="601d1-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="601d1-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="601d1-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="601d1-177">Minimum supported server</span></span><br/> | <span data-ttu-id="601d1-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="601d1-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="601d1-179">Encabezado</span><span class="sxs-lookup"><span data-stu-id="601d1-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="601d1-180"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="601d1-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="601d1-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="601d1-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="601d1-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601d1-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="601d1-183">IID</span><span class="sxs-lookup"><span data-stu-id="601d1-183">IID</span></span><br/>                      | <span data-ttu-id="601d1-184">IID \_ IADsPrintJob se define como 32FB6780-1ED0-11cf-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="601d1-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="601d1-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="601d1-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601d1-186">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="601d1-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="601d1-187">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="601d1-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





