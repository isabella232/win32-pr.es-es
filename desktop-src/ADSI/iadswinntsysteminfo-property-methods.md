---
title: Métodos de la propiedad IADsWinNTSystemInfo (iAds. h)
description: Los métodos de propiedad de la interfaz IADsWinNTSystemInfo obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsWinNTSystemInfo ADSI
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656477"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="96c76-105">Métodos de propiedad IADsWinNTSystemInfo</span><span class="sxs-lookup"><span data-stu-id="96c76-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="96c76-106">Los métodos de propiedad de la interfaz [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="96c76-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="96c76-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="96c76-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="96c76-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96c76-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="96c76-109">**nombreDeEquipo**</span><span class="sxs-lookup"><span data-stu-id="96c76-109">**ComputerName**</span></span>
<span data-ttu-id="96c76-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96c76-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="96c76-111">Nombre del equipo host en el que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="96c76-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="96c76-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96c76-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c76-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96c76-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96c76-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="96c76-114">**DomainName**</span></span>
<span data-ttu-id="96c76-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96c76-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="96c76-116">Nombre del dominio al que pertenece el usuario.</span><span class="sxs-lookup"><span data-stu-id="96c76-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="96c76-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96c76-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c76-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96c76-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96c76-119">**ÉL**</span><span class="sxs-lookup"><span data-stu-id="96c76-119">**PDC**</span></span>
<span data-ttu-id="96c76-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96c76-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="96c76-121">Nombre del controlador de dominio principal al que pertenece el equipo host.</span><span class="sxs-lookup"><span data-stu-id="96c76-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="96c76-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96c76-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c76-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96c76-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="96c76-124">**UserName**</span><span class="sxs-lookup"><span data-stu-id="96c76-124">**UserName**</span></span>
<span data-ttu-id="96c76-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="96c76-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="96c76-126">Nombre de la cuenta de usuario en la que se crea el objeto **WinNTSystemInfo** .</span><span class="sxs-lookup"><span data-stu-id="96c76-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="96c76-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96c76-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96c76-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="96c76-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="96c76-129">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="96c76-129">Examples</span></span>

<span data-ttu-id="96c76-130">En el siguiente ejemplo de código de C/C++ se recupera la información del sistema Winnt.</span><span class="sxs-lookup"><span data-stu-id="96c76-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="96c76-131">Por motivos de brevedad, se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="96c76-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="96c76-132">En el siguiente ejemplo de código de Visual Basic se recupera la información del sistema Winnt.</span><span class="sxs-lookup"><span data-stu-id="96c76-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="96c76-133">En el siguiente ejemplo de código de páginas de Visual Basic Scripting Edition/Active Server se recupera la información del sistema Winnt.</span><span class="sxs-lookup"><span data-stu-id="96c76-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="96c76-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96c76-134">Requirements</span></span>



| <span data-ttu-id="96c76-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c76-135">Requirement</span></span> | <span data-ttu-id="96c76-136">Value</span><span class="sxs-lookup"><span data-stu-id="96c76-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96c76-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96c76-137">Minimum supported client</span></span><br/> | <span data-ttu-id="96c76-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96c76-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96c76-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96c76-139">Minimum supported server</span></span><br/> | <span data-ttu-id="96c76-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96c76-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96c76-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="96c76-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="96c76-142"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c76-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="96c76-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="96c76-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96c76-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96c76-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="96c76-145">IID</span><span class="sxs-lookup"><span data-stu-id="96c76-145">IID</span></span><br/>                      | <span data-ttu-id="96c76-146">IID \_ IADsWinNTSystemInfo se define como 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="96c76-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="96c76-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="96c76-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c76-148">**IADsWinNTSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="96c76-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





