---
title: Método GenerateReport de la clase Win32_TSLicenseReport (GPMgmt. h)
description: GenerateReport ya no está disponible para su uso a partir de Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Método GenerateReport Servicios de Escritorio remoto
- Método GenerateReport Servicios de Escritorio remoto, clase Win32_TSLicenseReport
- Win32_TSLicenseReport de clase Servicios de Escritorio remoto, método GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422480"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="2af6e-106">Método GenerateReport de la \_ clase TSLicenseReport de Win32</span><span class="sxs-lookup"><span data-stu-id="2af6e-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="2af6e-107">\[**GenerateReport** ya no está disponible para su uso a partir de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="2af6e-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="2af6e-108">En su lugar, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span><span class="sxs-lookup"><span data-stu-id="2af6e-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="2af6e-109">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2af6e-109">This method is not supported.</span></span>

<span data-ttu-id="2af6e-110">**Windows server 2008 R2 y Windows server 2008:** Genera un informe de uso de licencias por usuario actual en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2af6e-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2af6e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2af6e-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="2af6e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2af6e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2af6e-113">*ScopeType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2af6e-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af6e-114">Ámbito del informe de uso de licencias.</span><span class="sxs-lookup"><span data-stu-id="2af6e-114">Scope of the license usage report.</span></span> <span data-ttu-id="2af6e-115">Puede tener los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2af6e-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="2af6e-116">1</span><span class="sxs-lookup"><span data-stu-id="2af6e-116">1</span></span>
</dt> <dd>

<span data-ttu-id="2af6e-117">El informe se generará para todo el dominio.</span><span class="sxs-lookup"><span data-stu-id="2af6e-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="2af6e-118">2</span><span class="sxs-lookup"><span data-stu-id="2af6e-118">2</span></span>
</dt> <dd>

<span data-ttu-id="2af6e-119">El informe se generará para la unidad organizativa (OU) que se especifica en el parámetro *ScopeValue* .</span><span class="sxs-lookup"><span data-stu-id="2af6e-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2af6e-120">3</span><span class="sxs-lookup"><span data-stu-id="2af6e-120">3</span></span>
</dt> <dd>

<span data-ttu-id="2af6e-121">El informe se generará para todos los dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="2af6e-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="2af6e-122">*ScopeValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2af6e-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2af6e-123">Si el parámetro *ScopeType* es 2, *ScopeType* especifica la unidad organizativa para la que se generará el informe.</span><span class="sxs-lookup"><span data-stu-id="2af6e-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="2af6e-124">Debe especificar *ScopeValue* con el formato **ou =**_OUName1_*_, ou =_*_OUName2_*_.._*..</span><span class="sxs-lookup"><span data-stu-id="2af6e-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="2af6e-125">*Nombre de archivo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2af6e-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2af6e-126">Nombre de archivo del informe generado.</span><span class="sxs-lookup"><span data-stu-id="2af6e-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2af6e-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2af6e-127">Return value</span></span>

<span data-ttu-id="2af6e-128">Devuelve **WBEM \_ E \_ no \_ compatible**.</span><span class="sxs-lookup"><span data-stu-id="2af6e-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="2af6e-129">**Windows server 2008 R2 y Windows server 2008:** Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2af6e-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2af6e-130">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2af6e-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2af6e-131">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2af6e-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2af6e-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2af6e-132">Remarks</span></span>

<span data-ttu-id="2af6e-133">Se trata de un método estático.</span><span class="sxs-lookup"><span data-stu-id="2af6e-133">This is a static method.</span></span>

<span data-ttu-id="2af6e-134">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2af6e-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2af6e-135">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2af6e-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2af6e-136">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2af6e-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2af6e-137">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2af6e-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2af6e-138">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2af6e-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2af6e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2af6e-139">Requirements</span></span>



| <span data-ttu-id="2af6e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="2af6e-140">Requirement</span></span> | <span data-ttu-id="2af6e-141">Value</span><span class="sxs-lookup"><span data-stu-id="2af6e-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2af6e-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2af6e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2af6e-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2af6e-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2af6e-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2af6e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2af6e-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2af6e-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2af6e-146">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="2af6e-146">End of client support</span></span><br/>    | <span data-ttu-id="2af6e-147">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2af6e-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2af6e-148">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="2af6e-148">End of server support</span></span><br/>    | <span data-ttu-id="2af6e-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2af6e-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="2af6e-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2af6e-150">Namespace</span></span><br/>                | <span data-ttu-id="2af6e-151">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2af6e-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2af6e-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2af6e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="2af6e-153"><dt>GPMgmt. h</dt></span><span class="sxs-lookup"><span data-stu-id="2af6e-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="2af6e-154">MOF</span><span class="sxs-lookup"><span data-stu-id="2af6e-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2af6e-155"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2af6e-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2af6e-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2af6e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2af6e-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2af6e-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2af6e-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="2af6e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2af6e-159">**Win32 \_ TSLicenseReport**</span><span class="sxs-lookup"><span data-stu-id="2af6e-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

