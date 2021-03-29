---
title: Métodos de la propiedad IADsSession (iAds. h)
description: Los métodos de propiedad de la interfaz IADsSession obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información y una explicación general sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
ms.assetid: b2366da7-c51c-4279-8931-2000d3110d72
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsSession ADSI
topic_type:
- apiref
api_name:
- IADsSession Property Methods
- IADsSession.Computer
- IADsSession.get_Computer
- IADsSession.ComputerPath
- IADsSession.get_ComputerPath
- IADsSession.ConnectTime
- IADsSession.get_ConnectTime
- IADsSession.IdleTime
- IADsSession.get_IdleTime
- IADsSession.User
- IADsSession.get_User
- IADsSession.UserPath
- IADsSession.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf7dd9abe25d731ba63385cd8d632c4212ea349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905178"
---
# <a name="iadssession-property-methods"></a><span data-ttu-id="d552a-105">Métodos de propiedad IADsSession</span><span class="sxs-lookup"><span data-stu-id="d552a-105">IADsSession Property Methods</span></span>

<span data-ttu-id="d552a-106">Los métodos de propiedad de la interfaz [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d552a-106">The property methods of the [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="d552a-107">Para obtener más información y una explicación general sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d552a-107">For more information and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="d552a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d552a-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="d552a-109">**Equipo**</span><span class="sxs-lookup"><span data-stu-id="d552a-109">**Computer**</span></span>
<span data-ttu-id="d552a-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d552a-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="d552a-111">Nombre de la estación de trabajo del cliente.</span><span class="sxs-lookup"><span data-stu-id="d552a-111">Name of the client workstation.</span></span>

<dt>

<span data-ttu-id="d552a-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d552a-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d552a-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d552a-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Computer(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d552a-114">**ComputerPath**</span><span class="sxs-lookup"><span data-stu-id="d552a-114">**ComputerPath**</span></span>
<span data-ttu-id="d552a-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d552a-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="d552a-116">ADsPath del objeto de equipo de la estación de trabajo cliente.</span><span class="sxs-lookup"><span data-stu-id="d552a-116">ADsPath of the computer object for the client workstation.</span></span>

<dt>

<span data-ttu-id="d552a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d552a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d552a-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d552a-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerPath(
  [out] BSTR* pbstrComputerPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d552a-119">**ConnectTime**</span><span class="sxs-lookup"><span data-stu-id="d552a-119">**ConnectTime**</span></span>
<span data-ttu-id="d552a-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d552a-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="d552a-121">Tiempo transcurrido, en segundos, desde que se inició la sesión.</span><span class="sxs-lookup"><span data-stu-id="d552a-121">Elapsed time, in seconds, since the session started.</span></span>

<dt>

<span data-ttu-id="d552a-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d552a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d552a-123">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d552a-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ConnectTime(
  [out] LONG* plConnectTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d552a-124">**Tiempo de inactividad**</span><span class="sxs-lookup"><span data-stu-id="d552a-124">**IdleTime**</span></span>
<span data-ttu-id="d552a-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d552a-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="d552a-126">Tiempo de inactividad, en segundos, de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d552a-126">Idle time, in seconds, of the session.</span></span>

<dt>

<span data-ttu-id="d552a-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d552a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d552a-128">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="d552a-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IdleTime(
  [out] LONG* plIdleTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d552a-129">**User**</span><span class="sxs-lookup"><span data-stu-id="d552a-129">**User**</span></span>
<span data-ttu-id="d552a-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d552a-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="d552a-131">Nombre del usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d552a-131">The name of the user of the session.</span></span>

<dt>

<span data-ttu-id="d552a-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d552a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d552a-133">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d552a-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="d552a-134">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="d552a-134">**UserPath**</span></span>
<span data-ttu-id="d552a-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="d552a-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="d552a-136">ADsPath del objeto de usuario para el usuario de esta sesión.</span><span class="sxs-lookup"><span data-stu-id="d552a-136">The ADsPath of the user object for the user of this session.</span></span>

<dt>

<span data-ttu-id="d552a-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d552a-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d552a-138">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d552a-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="d552a-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d552a-139">Examples</span></span>

<span data-ttu-id="d552a-140">En el ejemplo de código siguiente se muestra cómo examinar las sesiones de un servicio de archivos.</span><span class="sxs-lookup"><span data-stu-id="d552a-140">The following code example shows how to examine sessions for a file service.</span></span>


```VB
Dim fso As IADsFileServiceOperations
On Error GoTo Cleanup

' Bind to a file service operations object on "myComputer" in the local domain.
Set fso = GetObject("WinNT://myComputer/LanmanServer")

' Enumerate sessions.
If (IsEmpty(fso) = False) Then
    For Each session In fso.sessions
        MsgBox "Session Computer: " & session.Computer
        MsgBox "Session User: " & session.User
    Next Session
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fso = Nothing
```



<span data-ttu-id="d552a-141">En el ejemplo de código siguiente se enumera una colección de sesiones.</span><span class="sxs-lookup"><span data-stu-id="d552a-141">The following code example enumerates a collection of sessions.</span></span>


```C++
IADsFileServiceOperations *pFso = NULL;
IADsSession *pSes = NULL;
IADsCollection *pColl = NULL;
HRESULT hr = S_OK;
IUnknown *pUnk = NULL;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IEnumVARIANT *pEnum = NULL;

VariantInit(&var);

LPWSTR adsPath = L"WinNT://aMachine/LanmanServer";

hr = ADsGetObject(adsPath,IID_IADsFileServiceOperations,
                  (void**)&pFso);

if(FAILED(hr)) {goto Cleanup;}

hr = pFso->Sessions(&pColl);

// Enumerate sessions. 
hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)) {goto Cleanup;}

hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)) {goto Cleanup;}

// Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsSession, (void**)&pSes);
        pSes->get_Computer(&bstr);
        printf("Session host: %S\n",bstr);
        SysFreeString(bstr);

        pSes->get_User(&bstr);
        printf("Session user: %S\n",bstr);
        SysFreeString(bstr);

        pRes->Release();
    }

    VariantClear(&var);
    pDisp=NULL;
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pFso) pFso->Release();
    if(pColl) pColl->Release();
    if(pUnk) pUnk->Release();
    if(pEnum) pEnum->Release();
```



## <a name="requirements"></a><span data-ttu-id="d552a-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d552a-142">Requirements</span></span>



| <span data-ttu-id="d552a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d552a-143">Requirement</span></span> | <span data-ttu-id="d552a-144">Value</span><span class="sxs-lookup"><span data-stu-id="d552a-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d552a-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d552a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d552a-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d552a-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d552a-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d552a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d552a-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d552a-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d552a-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d552a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d552a-150"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="d552a-150"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="d552a-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d552a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d552a-152"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d552a-152"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="d552a-153">IID</span><span class="sxs-lookup"><span data-stu-id="d552a-153">IID</span></span><br/>                      | <span data-ttu-id="d552a-154">IID \_ IADsSession se define como 398B7DA0-4AAB-11cf-AE2C-00AA006EBFB9</span><span class="sxs-lookup"><span data-stu-id="d552a-154">IID\_IADsSession is defined as 398B7DA0-4AAB-11CF-AE2C-00AA006EBFB9</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d552a-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="d552a-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d552a-156">**IADsFileServiceOperations:: Sessions**</span><span class="sxs-lookup"><span data-stu-id="d552a-156">**IADsFileServiceOperations::Sessions**</span></span>](/windows/desktop/api/Iads/nf-iads-iadsfileserviceoperations-sessions)
</dt> <dt>

[<span data-ttu-id="d552a-157">**IADsSession**</span><span class="sxs-lookup"><span data-stu-id="d552a-157">**IADsSession**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssession)
</dt> </dl>

 

 





