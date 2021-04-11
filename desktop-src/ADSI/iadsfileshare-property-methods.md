---
title: Métodos de la propiedad IADsFileShare (iAds. h)
description: Los métodos de propiedad de la interfaz IADsFileshare obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: c5a81c42-507f-4a68-b6f4-83097bd0fa01
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsFileShare ADSI
topic_type:
- apiref
api_name:
- IADsFileShare Property Methods
- IADsFileShare.CurrentUserCount
- IADsFileShare.get_CurrentUserCount
- IADsFileShare.Description
- IADsFileShare.get_Description
- IADsFileShare.put_Description
- IADsFileShare.HostComputer
- IADsFileShare.get_HostComputer
- IADsFileShare.put_HostComputer
- IADsFileShare.MaxUserCount
- IADsFileShare.get_MaxUserCount
- IADsFileShare.Path
- IADsFileShare.get_Path
- IADsFileShare.put_Path
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38369a4054f1848d5e35ff8bdb2dda9e9423a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150772"
---
# <a name="iadsfileshare-property-methods"></a><span data-ttu-id="52500-105">Métodos de propiedad IADsFileShare</span><span class="sxs-lookup"><span data-stu-id="52500-105">IADsFileShare Property Methods</span></span>

<span data-ttu-id="52500-106">Los métodos de propiedad de la interfaz [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="52500-106">The property methods of the [**IADsFileshare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="52500-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="52500-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="52500-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52500-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="52500-109">**CurrentUserCount**</span><span class="sxs-lookup"><span data-stu-id="52500-109">**CurrentUserCount**</span></span>
<span data-ttu-id="52500-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="52500-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="52500-111">Número de usuarios conectados al recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="52500-111">The number of users connected to the share.</span></span>

<dt>

<span data-ttu-id="52500-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52500-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52500-113">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="52500-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CurrentUserCount(
  [out] LONG* plCurrentUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="52500-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52500-114">**Description**</span></span>
<span data-ttu-id="52500-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="52500-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="52500-116">La descripción del recurso compartido de archivos.</span><span class="sxs-lookup"><span data-stu-id="52500-116">The description of the file share.</span></span>

<dt>

<span data-ttu-id="52500-117">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="52500-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="52500-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="52500-118">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="52500-119">**HostComputer**</span><span class="sxs-lookup"><span data-stu-id="52500-119">**HostComputer**</span></span>
<span data-ttu-id="52500-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="52500-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="52500-121">Una referencia ADsPath al equipo host.</span><span class="sxs-lookup"><span data-stu-id="52500-121">An ADsPath reference to the host computer.</span></span>

<dt>

<span data-ttu-id="52500-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="52500-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="52500-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="52500-123">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="52500-124">**MaxUserCount**</span><span class="sxs-lookup"><span data-stu-id="52500-124">**MaxUserCount**</span></span>
<span data-ttu-id="52500-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="52500-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="52500-126">Número máximo de usuarios con permiso para obtener acceso al recurso compartido al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="52500-126">The maximum number of users allowed to access the share at one time.</span></span>

<dt>

<span data-ttu-id="52500-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="52500-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52500-128">Tipo de datos de scripting: **largo**</span><span class="sxs-lookup"><span data-stu-id="52500-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxUserCount(
  [out] LONG* plMaxUserCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="52500-129">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="52500-129">**Path**</span></span>
<span data-ttu-id="52500-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="52500-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="52500-131">Ruta de acceso del sistema de archivos al directorio compartido.</span><span class="sxs-lookup"><span data-stu-id="52500-131">The file system path to the shared directory.</span></span>

<dt>

<span data-ttu-id="52500-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="52500-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="52500-133">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="52500-133">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="52500-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="52500-134">Examples</span></span>

<span data-ttu-id="52500-135">Para tener acceso a las propiedades de los recursos compartidos de archivos de un equipo, primero debe enlazar a "LanmanServer" en el equipo.</span><span class="sxs-lookup"><span data-stu-id="52500-135">To access the properties of file shares on a computer, you must first bind to the "LanmanServer" on the machine.</span></span> <span data-ttu-id="52500-136">En el ejemplo de código siguiente se muestra cómo configurar la descripción y el número máximo de usuarios permitidos para todos los recursos compartidos de archivos públicos del equipo, denominados "MiEquipo", en el dominio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="52500-136">The following code example shows how to set up the description and the maximum number of allowed users for all the public file shares on the computer, named as "myMachine", in the default domain.</span></span>


```VB
Dim fs As IADsFileService
Dim share As IADsFileShare
On Error GoTo Cleanup

Set fs = GetObject("WinNT://myMachine/LanmanServer")
If (fs.class = "FileService") Then
    For Each share In fs
        share.description = share.name & " is my working folder."
        share.MaxUserCount =  10
        share.SetInfo
    Next share
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set fs = Nothing
    Set share = Nothing
```



<span data-ttu-id="52500-137">En el ejemplo de código siguiente se muestra cómo convertir el directorio C: carpetas existente en \\ un recurso compartido de archivos público.</span><span class="sxs-lookup"><span data-stu-id="52500-137">The following code example shows how to make the existing C:\\MyFolder directory a public file share.</span></span>


```VB
Dim fs As IADsFileShare
Dim cont As IADsContainer
On Error GoTo Cleanup
 
Set cont = GetObject("WinNT://yourDomain/yourMachineName/LanmanServer")
 
Set fs = cont.Create("FileShare", "Public")
Debug.Print fs.Class
fs.Path = "C:\MyFolder"
fs.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set fs = Nothing
```



<span data-ttu-id="52500-138">En el ejemplo de código siguiente se hace que el directorio C: \\ carpeta de carpetas existente sea un recurso compartido de archivos público.</span><span class="sxs-lookup"><span data-stu-id="52500-138">The following code example makes the existing C:\\MyFolder directory a public file share.</span></span>


```C++
IADsFileShare *pShare = NULL;
IADsContainer *pCont = NULL;
LPWSTR adsPath = L"WinNT://yourMachineName/LanmanServer";
HRESULT hr = S_OK;

hr = ADsGetObject(adsPath, IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->Create(CComBSTR("FileShare"), CComBSTR("Public"), (IDispatch**)&pShare);

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->put_Path(CComBSTR("c:\\public"));

if(FAILED(hr)) {goto Cleanup;}

hr = pShare->SetInfo();

Cleanup:
    if(pCont) pCont->Release();
    if(pShare) pShare->Release();
```



## <a name="requirements"></a><span data-ttu-id="52500-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52500-139">Requirements</span></span>



| <span data-ttu-id="52500-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="52500-140">Requirement</span></span> | <span data-ttu-id="52500-141">Value</span><span class="sxs-lookup"><span data-stu-id="52500-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52500-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52500-142">Minimum supported client</span></span><br/> | <span data-ttu-id="52500-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52500-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="52500-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52500-144">Minimum supported server</span></span><br/> | <span data-ttu-id="52500-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52500-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="52500-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52500-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="52500-147"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="52500-147"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="52500-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52500-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52500-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52500-149"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="52500-150">IID</span><span class="sxs-lookup"><span data-stu-id="52500-150">IID</span></span><br/>                      | <span data-ttu-id="52500-151">IID \_ IADsFileShare se define como EB6DCAF0-4B83-11cf-A995-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="52500-151">IID\_IADsFileShare is defined as EB6DCAF0-4B83-11CF-A995-00AA006BC149</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="52500-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="52500-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52500-153">**IADsService**</span><span class="sxs-lookup"><span data-stu-id="52500-153">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="52500-154">**IADsFileShare**</span><span class="sxs-lookup"><span data-stu-id="52500-154">**IADsFileShare**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileshare)
</dt> <dt>

[<span data-ttu-id="52500-155">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="52500-155">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





