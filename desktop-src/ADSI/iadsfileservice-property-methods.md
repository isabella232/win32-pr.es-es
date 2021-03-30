---
title: Métodos de la propiedad IADsFileService (iAds. h)
description: Los métodos de propiedad de la interfaz IADsFileService obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 1455df61-9218-450b-b956-1cf127364f24
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsFileService ADSI
topic_type:
- apiref
api_name:
- IADsFileService Property Methods
- IADsFileService.Description
- IADsFileService.get_Description
- IADsFileService.put_Description
- IADsFileService.MaxUserCount
- IADsFileService.get_MaxUserCount
- IADsFileService.put_MaxUserCount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a46b37522bbdce6e99b969811e2909c8ecc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534846"
---
# <a name="iadsfileservice-property-methods"></a><span data-ttu-id="6fbcb-105">Métodos de propiedad IADsFileService</span><span class="sxs-lookup"><span data-stu-id="6fbcb-105">IADsFileService Property Methods</span></span>

<span data-ttu-id="6fbcb-106">Los métodos de propiedad de la interfaz [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-106">The property methods of the [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="6fbcb-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6fbcb-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6fbcb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6fbcb-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6fbcb-109">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-109">**Description**</span></span>
<span data-ttu-id="6fbcb-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6fbcb-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6fbcb-111">La descripción del servicio de archivos.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-111">The description of the file service.</span></span>

<dt>

<span data-ttu-id="6fbcb-112">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6fbcb-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6fbcb-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-113">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="6fbcb-114">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-114">**MaxUserCount**</span></span>
<span data-ttu-id="6fbcb-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6fbcb-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6fbcb-116">Número máximo de usuarios permitidos en el servicio en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-116">The maximum number of users allowed on the service at any time.</span></span>

<dt>

<span data-ttu-id="6fbcb-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6fbcb-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6fbcb-118">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
HRESULT put_MaxUserCount(
  [in] LONG lMaxUserCount
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="6fbcb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fbcb-119">Remarks</span></span>

<span data-ttu-id="6fbcb-120">Debe pasar por el servicio archivo para tener acceso a recursos compartidos de archivos, sesiones y recursos de un equipo.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-120">You must go through the file service to access file shares, sessions, and resources on a computer.</span></span>

## <a name="examples"></a><span data-ttu-id="6fbcb-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6fbcb-121">Examples</span></span>

<span data-ttu-id="6fbcb-122">En el ejemplo de código siguiente se escribe una descripción de y se comprueba el límite de usuario del servicio archivo.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-122">The following code example writes a description for and check the user limit of the file service.</span></span>


```VB
Dim fs As IADsFileService
On Error GoTo Cleanup

' Bind to a file service object on "myComputer" in the local domain.
Set fs = GetObject("WinNT://myComputer/LanmanServer")

fs.Description = "WinNT file service."
n = fs.MaxUserCount
If n = -1 Then
   MsgBox "No limit has been imposed on number of users allowed."
Else
   MsgBox n & " users are allowed."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
```



<span data-ttu-id="6fbcb-123">En el ejemplo de código siguiente se escribe una descripción de y se comprueba el límite de usuario en un objeto de servicio de archivos.</span><span class="sxs-lookup"><span data-stu-id="6fbcb-123">The following code example writes a description for and check the user limit on a file service object.</span></span>


```C++
HRESULT CheckFileService()
{
    IADsFileService *pFs = NULL;
    LPWSTR adsPath = L"WinNT://myComputer/LanmanServer";
    HRESULT hr = S_OK;
    long count = 0;

    hr = ADsGetObject(adsPath, IID_IADsFileService, (void**)&pFs)
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->put_Description(CComBSTR("WinNT File Service"));
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->SetInfo();
    if(FAILED(hr)) {goto Cleanup;}

    hr = pFs->get_MaxUserCount(&count);
    if(FAILED(hr)) {goto Cleanup;}

    if(count == -1) {
        printf("No limit has been imposed on the number of users.\n");
    } 
    else {
        printf("Number of allowed users are %d\n",count);
    }

Cleanup:
    if(pFs) pFs->Release();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="6fbcb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fbcb-124">Requirements</span></span>



| <span data-ttu-id="6fbcb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fbcb-125">Requirement</span></span> | <span data-ttu-id="6fbcb-126">Value</span><span class="sxs-lookup"><span data-stu-id="6fbcb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbcb-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fbcb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6fbcb-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fbcb-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6fbcb-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6fbcb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6fbcb-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fbcb-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6fbcb-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fbcb-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fbcb-132"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fbcb-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6fbcb-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6fbcb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fbcb-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fbcb-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6fbcb-135">IID</span><span class="sxs-lookup"><span data-stu-id="6fbcb-135">IID</span></span><br/>                      | <span data-ttu-id="6fbcb-136">IID \_ IADsFileService se define como A89D1900-31CA-11cf-A98A-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="6fbcb-136">IID\_IADsFileService is defined as A89D1900-31CA-11CF-A98A-00AA006BC149</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="6fbcb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fbcb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbcb-138">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-138">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="6fbcb-139">**IADsFileService**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-139">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="6fbcb-140">**IADsFileServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-140">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="6fbcb-141">**IADsServiceOperations**</span><span class="sxs-lookup"><span data-stu-id="6fbcb-141">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> <dt>

[<span data-ttu-id="6fbcb-142">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="6fbcb-142">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





