---
title: Métodos de propiedad IADsServiceOperations (Iads.h)
description: Los métodos de propiedad de la interfaz IADsServiceOperations leen y escriben las propiedades descritas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea Métodos de propiedad de interfaz.
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
ms.openlocfilehash: c7f60b8fe1280e257ccd33f505b2b696a0d1a16228ebfaf8b0cabf7f1319964a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427611"
---
# <a name="iadsserviceoperations-property-methods"></a>Métodos de propiedad IADsServiceOperations

Los métodos de propiedad [**de la interfaz IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) leen y escriben las propiedades descritas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Estado**
</dt> <dd> <dl>

Estado del servicio.

A continuación se den los valores posibles.

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

**ADS \_ SERVICE \_ STOPPED** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

**ADS \_ INICIO \_ DEL \_ SERVICIO PENDIENTE** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

**ADS \_ SERVICE \_ STOP \_ PENDING** (0X00000003)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

**ADS \_ SERVICE \_ RUNNING** (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

**ADS \_ CONTINUAR \_ EL \_ SERVICIO PENDIENTE** (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

**ADS \_ PAUSA \_ DE \_ SERVICIO PENDIENTE** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

**ADS \_ SERVICIO \_ EN PAUSA** (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

**ADS \_ \_ERROR DE SERVICIO** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

**ADS \_ PROCESO \_ DE \_ SERVICE OWN** (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

**ADS \_ PROCESO \_ DE RECURSO COMPARTIDO \_ DE** SERVICIO (0x00000020)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

**ADS \_ CONTROLADOR \_ DE KERNEL \_ DE** SERVICIO (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

**ADS \_ CONTROLADOR \_ DEL SISTEMA DE ARCHIVOS \_ \_ DE** SERVICIO (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

**ADS \_ INICIO \_ DE ARRANQUE DEL \_ SERVICIO** (INICIO \_ DE ARRANQUE DEL \_ SERVICIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

**ADS \_ INICIO \_ DEL SISTEMA DE \_ SERVICIO** (INICIO \_ DEL SISTEMA DE \_ SERVICIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

**ADS \_ INICIO \_ AUTOMÁTICO \_ DEL SERVICIO** (INICIO AUTOMÁTICO DEL \_ \_ SERVICIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

**ADS \_ INICIO \_ DE LA DEMANDA DE \_ SERVICIO** (INICIO \_ DE LA DEMANDA DEL \_ SERVICIO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

**ADS \_ SERVICIO \_ DESHABILITADO** (SERVICIO \_ DESHABILITADO)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

**ADS \_ ERROR \_ DE \_ SERVICIO IGNORE** (0)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

**ADS \_ \_ERROR DE SERVICIO \_ NORMAL** (1)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

**ADS \_ \_ERROR GRAVE DEL \_ SERVICIO** (2)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

**ADS \_ \_ERROR CRÍTICO DEL \_ SERVICIO** (3)


</dt> <dd></dd> </dl> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo comprobar el estado de un servicio de fax de Microsoft que se ejecuta Windows 2000.


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



En el ejemplo de código siguiente se comprueba el estado de un servicio de fax de Microsoft que se ejecuta Windows 2000.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IADsServiceOperations se define como 5D7B33F0-31CA-11CF-A98A-00AA006BC149<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





