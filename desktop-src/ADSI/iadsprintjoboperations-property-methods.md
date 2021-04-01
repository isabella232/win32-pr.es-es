---
title: Métodos de la propiedad IADsPrintJobOperations (iAds. h)
description: Los métodos de propiedad de la interfaz IADsPrintJobOperations leen y escriben las propiedades que se muestran en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPrintJobOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905464"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="d2e76-105">Métodos de propiedad IADsPrintJobOperations</span><span class="sxs-lookup"><span data-stu-id="d2e76-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="d2e76-106">Los métodos de propiedad de la interfaz [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) leen y escriben las propiedades que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d2e76-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="d2e76-107">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d2e76-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d2e76-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2e76-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d2e76-109">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="d2e76-109">**PagesPrinted**</span></span>
<span data-ttu-id="d2e76-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d2e76-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d2e76-111">Contiene el número de páginas impresas.</span><span class="sxs-lookup"><span data-stu-id="d2e76-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="d2e76-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2e76-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2e76-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d2e76-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2e76-114">**Position**</span><span class="sxs-lookup"><span data-stu-id="d2e76-114">**Position**</span></span>
<span data-ttu-id="d2e76-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d2e76-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d2e76-116">Contiene la posición de este trabajo de impresión en la cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="d2e76-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="d2e76-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d2e76-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d2e76-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d2e76-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2e76-119">**Estado**</span><span class="sxs-lookup"><span data-stu-id="d2e76-119">**Status**</span></span>
<span data-ttu-id="d2e76-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d2e76-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d2e76-121">Contiene el estado actual del trabajo de impresión indicado por uno de los valores de [**constantes de estado del trabajo de impresión de ADSI**](adsi-print-job-status-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e76-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="d2e76-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2e76-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2e76-123">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d2e76-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d2e76-124">**TimeElapsed**</span><span class="sxs-lookup"><span data-stu-id="d2e76-124">**TimeElapsed**</span></span>
<span data-ttu-id="d2e76-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d2e76-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="d2e76-126">Contiene el número de milisegundos transcurridos desde que se inició el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="d2e76-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="d2e76-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2e76-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2e76-128">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d2e76-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d2e76-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2e76-129">Examples</span></span>

<span data-ttu-id="d2e76-130">En el ejemplo de código siguiente se muestra cómo se pueden usar las propiedades de [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) .</span><span class="sxs-lookup"><span data-stu-id="d2e76-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a><span data-ttu-id="d2e76-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2e76-131">Requirements</span></span>



| <span data-ttu-id="d2e76-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2e76-132">Requirement</span></span> | <span data-ttu-id="d2e76-133">Value</span><span class="sxs-lookup"><span data-stu-id="d2e76-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e76-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2e76-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d2e76-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2e76-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="d2e76-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2e76-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d2e76-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2e76-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d2e76-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2e76-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2e76-139"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2e76-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="d2e76-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2e76-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2e76-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2e76-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d2e76-142">IID</span><span class="sxs-lookup"><span data-stu-id="d2e76-142">IID</span></span><br/>                      | <span data-ttu-id="d2e76-143">IID \_ IADsPrintJobOperations se define como 32FB6780-1ED0-11cf-A988-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="d2e76-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d2e76-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2e76-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2e76-145">**IADsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="d2e76-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="d2e76-146">**IADsPrintJobOperations**</span><span class="sxs-lookup"><span data-stu-id="d2e76-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="d2e76-147">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="d2e76-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="d2e76-148">**Constantes de estado del trabajo de impresión ADSI**</span><span class="sxs-lookup"><span data-stu-id="d2e76-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





