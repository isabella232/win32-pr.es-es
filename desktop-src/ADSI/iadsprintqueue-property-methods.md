---
title: Métodos de la propiedad IADsPrintQueue (iAds. h)
description: Los métodos de propiedad de la interfaz IADsPrintQueue obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPrintQueue ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274533"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="96783-105">Métodos de propiedad IADsPrintQueue</span><span class="sxs-lookup"><span data-stu-id="96783-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="96783-106">Los métodos de propiedad de la interfaz [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="96783-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="96783-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="96783-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="96783-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96783-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="96783-109">**BannerPage**</span><span class="sxs-lookup"><span data-stu-id="96783-109">**BannerPage**</span></span>
<span data-ttu-id="96783-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-111">Ruta de acceso del sistema de archivos que apunta a la página de encabezado utilizada para separar los trabajos de impresión.</span><span class="sxs-lookup"><span data-stu-id="96783-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="96783-112">Si es **null**, no se utiliza ninguna página de encabezado.</span><span class="sxs-lookup"><span data-stu-id="96783-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="96783-113">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-114">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-115">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="96783-115">**Datatype**</span></span>
<span data-ttu-id="96783-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-117">El tipo de datos que puede ser procesado por esta cola.</span><span class="sxs-lookup"><span data-stu-id="96783-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="96783-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-119">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-120">**DefaultJobPriority**</span><span class="sxs-lookup"><span data-stu-id="96783-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="96783-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-122">La prioridad predeterminada asignada a cada trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="96783-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="96783-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-124">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="96783-125">**Description**</span></span>
<span data-ttu-id="96783-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-127">La descripción de texto de esta cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="96783-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="96783-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-129">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-129">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="96783-130">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="96783-130">**HostComputer**</span></span>
<span data-ttu-id="96783-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-132">Cadena ADsPath que hace referencia al equipo host.</span><span class="sxs-lookup"><span data-stu-id="96783-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="96783-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-134">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-134">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-135">**Ubicación**</span><span class="sxs-lookup"><span data-stu-id="96783-135">**Location**</span></span>
<span data-ttu-id="96783-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-137">La ubicación de la cola tal como la describe un administrador.</span><span class="sxs-lookup"><span data-stu-id="96783-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="96783-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-139">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-140">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="96783-140">**Model**</span></span>
<span data-ttu-id="96783-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-142">Nombre del controlador utilizado por esta cola de impresión.</span><span class="sxs-lookup"><span data-stu-id="96783-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="96783-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-144">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-145">**PrintDevices**</span><span class="sxs-lookup"><span data-stu-id="96783-145">**PrintDevices**</span></span>
<span data-ttu-id="96783-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-147">SAFEARRAY de **BSTR** que contiene los nombres de los dispositivos de impresión en los que esta cola de impresión pone en cola los trabajos.</span><span class="sxs-lookup"><span data-stu-id="96783-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="96783-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-149">Tipo de datos de scripting: **variante**</span><span class="sxs-lookup"><span data-stu-id="96783-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-150">**PrinterPath**</span><span class="sxs-lookup"><span data-stu-id="96783-150">**PrinterPath**</span></span>
<span data-ttu-id="96783-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-152">Cadena que hace referencia a la ruta de acceso por la que se puede tener acceso a una impresora compartida.</span><span class="sxs-lookup"><span data-stu-id="96783-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="96783-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-154">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-155">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="96783-155">**PrintProcessor**</span></span>
<span data-ttu-id="96783-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-157">El procesador de impresión asociado a esta cola.</span><span class="sxs-lookup"><span data-stu-id="96783-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="96783-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-159">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96783-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96783-160">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="96783-160">**Priority**</span></span>
<span data-ttu-id="96783-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-162">La prioridad de esta cola de trabajos de objeto de impresora para cualquier dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="96783-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="96783-163">En primer lugar, se procesarán todos los trabajos de los objetos de cola de impresión de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="96783-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="96783-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-165">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="96783-165">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="96783-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="96783-166">**StartTime**</span></span>
<span data-ttu-id="96783-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-168">La hora a la que la cola debe empezar a procesar los trabajos.</span><span class="sxs-lookup"><span data-stu-id="96783-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="96783-169">Se omite la parte de la fecha de la hora.</span><span class="sxs-lookup"><span data-stu-id="96783-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="96783-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-171">Tipo de datos de scripting: **fecha**</span><span class="sxs-lookup"><span data-stu-id="96783-171">Scripting data type: **DATE**</span></span>
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

<span data-ttu-id="96783-172">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="96783-172">**UntilTime**</span></span>
<span data-ttu-id="96783-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96783-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="96783-174">La hora a la que la cola debe dejar de procesar los trabajos.</span><span class="sxs-lookup"><span data-stu-id="96783-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="96783-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="96783-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="96783-176">Tipo de datos de scripting: **fecha**</span><span class="sxs-lookup"><span data-stu-id="96783-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="96783-177">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96783-177">Examples</span></span>

<span data-ttu-id="96783-178">En el ejemplo de código siguiente se muestra cómo determinar si una impresora especificada está en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="96783-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="96783-179">En el ejemplo de código siguiente se muestra cómo determinar si una impresora especificada está en línea o sin conexión.</span><span class="sxs-lookup"><span data-stu-id="96783-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="96783-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96783-180">Requirements</span></span>



| <span data-ttu-id="96783-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="96783-181">Requirement</span></span> | <span data-ttu-id="96783-182">Value</span><span class="sxs-lookup"><span data-stu-id="96783-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96783-183">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96783-183">Minimum supported client</span></span><br/> | <span data-ttu-id="96783-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96783-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96783-185">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96783-185">Minimum supported server</span></span><br/> | <span data-ttu-id="96783-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96783-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96783-187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96783-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="96783-188"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="96783-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="96783-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96783-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96783-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96783-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="96783-191">IID</span><span class="sxs-lookup"><span data-stu-id="96783-191">IID</span></span><br/>                      | <span data-ttu-id="96783-192">IID \_ IADsPrintQueue se define como B15160D0-1226-11cf-A985-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="96783-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="96783-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="96783-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96783-194">**IADsPrintQueue**</span><span class="sxs-lookup"><span data-stu-id="96783-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="96783-195">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="96783-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





