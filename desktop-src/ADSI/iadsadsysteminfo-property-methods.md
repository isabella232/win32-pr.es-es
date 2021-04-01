---
title: Métodos de la propiedad IADsADSystemInfo (iAds. h)
description: Los métodos de propiedad de la interfaz IADsADSystemInfo obtienen o establecen las propiedades descritas en la tabla siguiente. Para obtener más información, vea métodos de propiedad de interfaz.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsADSystemInfo ADSI
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150781"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="6f610-105">Métodos de propiedad IADsADSystemInfo</span><span class="sxs-lookup"><span data-stu-id="6f610-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="6f610-106">Los métodos de propiedad de la interfaz [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) obtienen o establecen las propiedades descritas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6f610-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="6f610-107">Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="6f610-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="6f610-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f610-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="6f610-109">**nombreDeEquipo**</span><span class="sxs-lookup"><span data-stu-id="6f610-109">**ComputerName**</span></span>
<span data-ttu-id="6f610-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-111">Recupera el nombre distintivo del equipo local.</span><span class="sxs-lookup"><span data-stu-id="6f610-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="6f610-112">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-113">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-114">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="6f610-114">**DomainDNSName**</span></span>
<span data-ttu-id="6f610-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-116">Recupera el nombre DNS del dominio del equipo local, como "domainName.companyName.com".</span><span class="sxs-lookup"><span data-stu-id="6f610-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="6f610-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-118">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-119">**DomainShortName**</span><span class="sxs-lookup"><span data-stu-id="6f610-119">**DomainShortName**</span></span>
<span data-ttu-id="6f610-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-121">Recupera el nombre corto del dominio del equipo local, como "nombreDeDominio".</span><span class="sxs-lookup"><span data-stu-id="6f610-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="6f610-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-123">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-124">**ForestDNSName**</span><span class="sxs-lookup"><span data-stu-id="6f610-124">**ForestDNSName**</span></span>
<span data-ttu-id="6f610-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-126">Recupera el nombre DNS del bosque del equipo local.</span><span class="sxs-lookup"><span data-stu-id="6f610-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="6f610-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-128">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-129">**IsNativeMode**</span><span class="sxs-lookup"><span data-stu-id="6f610-129">**IsNativeMode**</span></span>
<span data-ttu-id="6f610-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-131">Determina si el dominio del equipo local está en modo nativo o mixto.</span><span class="sxs-lookup"><span data-stu-id="6f610-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="6f610-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-133">Tipo de datos de scripting: **bool**</span><span class="sxs-lookup"><span data-stu-id="6f610-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-134">**PDCRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="6f610-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="6f610-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-136">Recupera el nombre distintivo del objeto de agente de servicios de directorio (DSA) del DC que posee el rol de controlador de dominio principal en el dominio del equipo local.</span><span class="sxs-lookup"><span data-stu-id="6f610-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="6f610-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-138">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="6f610-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="6f610-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-141">Recupera el nombre distintivo del objeto de agente de servicios de directorio (DSA) del controlador de dominio al que pertenece el rol de maestro de esquema en el bosque del equipo local.</span><span class="sxs-lookup"><span data-stu-id="6f610-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="6f610-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-143">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-144">**Nombresitio**</span><span class="sxs-lookup"><span data-stu-id="6f610-144">**SiteName**</span></span>
<span data-ttu-id="6f610-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-146">Recupera el nombre del sitio del equipo local.</span><span class="sxs-lookup"><span data-stu-id="6f610-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="6f610-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-148">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f610-149">**UserName**</span><span class="sxs-lookup"><span data-stu-id="6f610-149">**UserName**</span></span>
<span data-ttu-id="6f610-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="6f610-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="6f610-151">Recupera el nombre distintivo Active Directory del usuario actual, que es el usuario que ha iniciado sesión o el usuario suplantado por el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="6f610-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="6f610-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6f610-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f610-153">Tipo de datos de scripting: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="6f610-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="6f610-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6f610-154">Examples</span></span>

<span data-ttu-id="6f610-155">En el siguiente ejemplo de código de C++ se recupera la información del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="6f610-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="6f610-156">Por motivos de brevedad, se omite la comprobación de errores.</span><span class="sxs-lookup"><span data-stu-id="6f610-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="6f610-157">En el siguiente ejemplo de código de Visual Basic se recupera la información del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="6f610-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="6f610-158">En el siguiente ejemplo de código de VBScript/ASP se recupera la información del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="6f610-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="6f610-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f610-159">Requirements</span></span>



| <span data-ttu-id="6f610-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f610-160">Requirement</span></span> | <span data-ttu-id="6f610-161">Value</span><span class="sxs-lookup"><span data-stu-id="6f610-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f610-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f610-162">Minimum supported client</span></span><br/> | <span data-ttu-id="6f610-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f610-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f610-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f610-164">Minimum supported server</span></span><br/> | <span data-ttu-id="6f610-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f610-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f610-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f610-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f610-167"><dt>IAds. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f610-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="6f610-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f610-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f610-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f610-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f610-170">IID</span><span class="sxs-lookup"><span data-stu-id="6f610-170">IID</span></span><br/>                      | <span data-ttu-id="6f610-171">IID \_ IADsADSystemInfo se define como 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="6f610-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="6f610-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f610-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f610-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="6f610-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="6f610-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="6f610-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

