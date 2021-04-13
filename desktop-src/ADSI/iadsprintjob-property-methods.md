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
# <a name="iadsprintjob-property-methods"></a>Métodos de propiedad IADsPrintJob

Los métodos de propiedad de la interfaz [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Descripción**
</dt> <dd> <dl>

La descripción del trabajo de impresión.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**HostPrintQueue**
</dt> <dd> <dl>

Cadena ADsPath de la cola de impresión que procesa el trabajo de impresión.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

**Notificar**
</dt> <dd> <dl>

El usuario al que se va a notificar cuando se complete el trabajo.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**NotifyPath**
</dt> <dd> <dl>

Cadena ADsPath del objeto de usuario al que se va a notificar cuando se complete el trabajo de impresión.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
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

**Prioridad**
</dt> <dd> <dl>

Prioridad del trabajo de impresión.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

**Tamaño**
</dt> <dd> <dl>

Tamaño, en bytes, del trabajo de impresión.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

**StartTime**
</dt> <dd> <dl>

Hora más temprana en la que se debe iniciar el trabajo de impresión.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **fecha**
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

**TimeSubmitted**
</dt> <dd> <dl>

La hora a la que se envió el trabajo a la cola.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **fecha**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

**TotalPages**
</dt> <dd> <dl>

Número total de páginas en el trabajo de impresión.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **largo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

**UntilTime**
</dt> <dd> <dl>

La hora más reciente en la que se debe iniciar el trabajo de impresión.

<dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **fecha**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

**User**
</dt> <dd> <dl>

Nombre del usuario que envió el trabajo de impresión.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

**UserPath**
</dt> <dd> <dl>

Cadena ADsPath del objeto de usuario que envió este trabajo de impresión.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo trabajar con las propiedades de un objeto de trabajo de impresión.


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



En el ejemplo de código siguiente se muestra cómo trabajar con las propiedades de un objeto de trabajo de impresión.


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsPrintJob se define como 32FB6780-1ED0-11cf-A988-00AA006BC149<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





