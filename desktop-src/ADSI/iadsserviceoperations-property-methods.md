---
title: Métodos de la propiedad IADsServiceOperations (iAds. h)
description: Los métodos de propiedad de la interfaz IADsServiceOperations leen y escriben las propiedades descritas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsServiceOperations ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905179"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="fbeb9-105">Métodos de propiedad IADsServiceOperations</span><span class="sxs-lookup"><span data-stu-id="fbeb9-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="fbeb9-106">Los métodos de propiedad de la interfaz [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) leen y escriben las propiedades descritas en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="fbeb9-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="fbeb9-107">Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fbeb9-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="fbeb9-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbeb9-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="fbeb9-109">**Estado**</span><span class="sxs-lookup"><span data-stu-id="fbeb9-109">**Status**</span></span>
<span data-ttu-id="fbeb9-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="fbeb9-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="fbeb9-111">Estado del servicio.</span><span class="sxs-lookup"><span data-stu-id="fbeb9-111">Status of service.</span></span>

<span data-ttu-id="fbeb9-112">Los valores posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fbeb9-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="fbeb9-113">**Anuncios \_ de SERVICIO \_ detenido** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="fbeb9-114">**Anuncios \_ de Inicio de servicio \_ \_ pendiente** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="fbeb9-115">**Anuncios \_ de Detención de servicio \_ \_ pendiente** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="fbeb9-116">**Anuncios \_ de SERVICIO en \_ ejecución** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="fbeb9-117">**Anuncios \_ de El servicio \_ continúa \_ pendiente** (0x00000005)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="fbeb9-118">**Anuncios \_ de La \_ pausa \_ del servicio está pendiente** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="fbeb9-119">**Anuncios \_ de SERVICIO en \_ pausa** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="fbeb9-120">**Anuncios \_ de \_Error de servicio** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="fbeb9-121">**Anuncios \_ de \_ \_ Proceso propio del servicio** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="fbeb9-122">**Anuncios \_ de \_ \_ Proceso de recurso compartido de servicio** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="fbeb9-123">**Anuncios \_ de \_ \_ Controlador de kernel de servicio** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="fbeb9-124">**Anuncios \_ de \_ \_ \_ Controlador del sistema de archivos de servicio** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="fbeb9-125">**Anuncios \_ de \_ \_ Inicio de arranque del servicio** (inicio de \_ arranque del servicio \_ )</span><span class="sxs-lookup"><span data-stu-id="fbeb9-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="fbeb9-126">**Anuncios \_ de \_ \_ Inicio de sistema de servicio** (inicio de sistema de servicio \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="fbeb9-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="fbeb9-127">**Anuncios \_ de \_ \_ Inicio automático del servicio** ( \_ Inicio automático del servicio \_ )</span><span class="sxs-lookup"><span data-stu-id="fbeb9-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="fbeb9-128">**Anuncios \_ de \_ \_ Inicio** de la demanda de servicio (inicio de la demanda de servicio \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="fbeb9-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="fbeb9-129">**Anuncios \_ de SERVICIO \_ deshabilitado** (servicio \_ deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="fbeb9-130">**Anuncios \_ de \_ \_ Omitir error de servicio** (0)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="fbeb9-131">**Anuncios \_ de ERROR de servicio \_ \_ normal** (1)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="fbeb9-132">**Anuncios \_ de \_Error \_ grave del servicio** (2)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="fbeb9-133">**Anuncios \_ de ERROR de servicio \_ \_ crítico** (3)</span><span class="sxs-lookup"><span data-stu-id="fbeb9-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="fbeb9-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbeb9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbeb9-135">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="fbeb9-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="fbeb9-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fbeb9-136">Examples</span></span>

<span data-ttu-id="fbeb9-137">En el ejemplo de código siguiente se muestra cómo comprobar el estado de un servicio de fax de Microsoft que se ejecuta en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fbeb9-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="fbeb9-138">En el ejemplo de código siguiente se comprueba el estado de un servicio de fax de Microsoft que se ejecuta en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fbeb9-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="fbeb9-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbeb9-139">Requirements</span></span>



| <span data-ttu-id="fbeb9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbeb9-140">Requirement</span></span> | <span data-ttu-id="fbeb9-141">Value</span><span class="sxs-lookup"><span data-stu-id="fbeb9-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbeb9-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbeb9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fbeb9-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbeb9-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fbeb9-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbeb9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fbeb9-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbeb9-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fbeb9-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbeb9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbeb9-147"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbeb9-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="fbeb9-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbeb9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbeb9-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbeb9-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="fbeb9-150">IID</span><span class="sxs-lookup"><span data-stu-id="fbeb9-150">IID</span></span><br/>                      | <span data-ttu-id="fbeb9-151">IID \_ IADsServiceOperations se define como 5D7B33F0-31CA-11cf-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="fbeb9-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbeb9-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbeb9-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbeb9-153">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="fbeb9-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="fbeb9-154">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="fbeb9-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="fbeb9-155">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="fbeb9-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="fbeb9-156">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="fbeb9-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





