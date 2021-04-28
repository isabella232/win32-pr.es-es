---
description: 'Método IShellDispatch2.GetSystemInformation: recupera información del sistema.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Método IShellDispatch2.GetSystemInformation (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117113"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="82420-103">Método IShellDispatch2.GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="82420-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="82420-104">Recupera información del sistema.</span><span class="sxs-lookup"><span data-stu-id="82420-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="82420-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82420-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="82420-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82420-107">*sName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="82420-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82420-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="82420-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="82420-109">Cadena **que** especifica la información del sistema que se solicita.</span><span class="sxs-lookup"><span data-stu-id="82420-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82420-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82420-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="82420-111">JScript</span><span class="sxs-lookup"><span data-stu-id="82420-111">JScript</span></span>

<span data-ttu-id="82420-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="82420-112">Type: **Variant**</span></span>

<span data-ttu-id="82420-113">Devuelve el valor de la información solicitada del sistema.</span><span class="sxs-lookup"><span data-stu-id="82420-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="82420-114">El tipo de valor devuelto depende de la información del sistema que se solicite.</span><span class="sxs-lookup"><span data-stu-id="82420-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="82420-115">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="82420-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="82420-116">VB</span><span class="sxs-lookup"><span data-stu-id="82420-116">VB</span></span>

<span data-ttu-id="82420-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="82420-117">Type: **Variant**</span></span>

<span data-ttu-id="82420-118">Devuelve el valor de la información solicitada del sistema.</span><span class="sxs-lookup"><span data-stu-id="82420-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="82420-119">El tipo de valor devuelto depende de la información del sistema que se solicite.</span><span class="sxs-lookup"><span data-stu-id="82420-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="82420-120">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="82420-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="82420-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="82420-121">Remarks</span></span>

<span data-ttu-id="82420-122">Este método se implementa y se accede a través del [**método Shell.GetSystemInformation.**](./shell-getsysteminformation.md)</span><span class="sxs-lookup"><span data-stu-id="82420-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="82420-123">Este método se puede usar para solicitar muchos valores de información del sistema.</span><span class="sxs-lookup"><span data-stu-id="82420-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="82420-124">En la tabla siguiente se proporciona *el valor sName* que se usa para solicitar la información y el tipo asociado del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="82420-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="82420-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="82420-125">*sName*</span></span>

<span data-ttu-id="82420-126">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82420-126">Return type</span></span>

<span data-ttu-id="82420-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="82420-127">Description</span></span>

<span data-ttu-id="82420-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="82420-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="82420-129">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="82420-129">**Boolean**</span></span>

<span data-ttu-id="82420-130">Establezca en **true** si el servicio de directorio está disponible; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="82420-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="82420-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="82420-131">DoubleClickTime</span></span>

<span data-ttu-id="82420-132">**Entero**</span><span class="sxs-lookup"><span data-stu-id="82420-132">**Integer**</span></span>

<span data-ttu-id="82420-133">Tiempo de doble clic, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="82420-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="82420-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="82420-134">ProcessorLevel</span></span>

<span data-ttu-id="82420-135">**Entero**</span><span class="sxs-lookup"><span data-stu-id="82420-135">**Integer**</span></span>

<span data-ttu-id="82420-136">**Windows Vista y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="82420-136">**Windows Vista and later**.</span></span> <span data-ttu-id="82420-137">Nivel de procesador.</span><span class="sxs-lookup"><span data-stu-id="82420-137">The processor level.</span></span> <span data-ttu-id="82420-138">Devuelve 3, 4 o 5 para procesadores de nivel x386, x486 y Pentium, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="82420-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="82420-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="82420-139">ProcessorSpeed</span></span>

<span data-ttu-id="82420-140">**Entero**</span><span class="sxs-lookup"><span data-stu-id="82420-140">**Integer**</span></span>

<span data-ttu-id="82420-141">Velocidad del procesador, en megahercios (MHz).</span><span class="sxs-lookup"><span data-stu-id="82420-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="82420-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="82420-142">ProcessorArchitecture</span></span>

<span data-ttu-id="82420-143">**Entero**</span><span class="sxs-lookup"><span data-stu-id="82420-143">**Integer**</span></span>

<span data-ttu-id="82420-144">Arquitectura del procesador.</span><span class="sxs-lookup"><span data-stu-id="82420-144">The processor architecture.</span></span> <span data-ttu-id="82420-145">Para obtener más información, vea la explicación del **miembro wProcessorArchitecture** de la [**estructura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)</span><span class="sxs-lookup"><span data-stu-id="82420-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="82420-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="82420-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="82420-147">**Entero**</span><span class="sxs-lookup"><span data-stu-id="82420-147">**Integer**</span></span>

<span data-ttu-id="82420-148">Cantidad de memoria física instalada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="82420-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="82420-149">Los siguientes son válidos solo en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="82420-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="82420-150">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="82420-150">IsOS\_Professional</span></span>

<span data-ttu-id="82420-151">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="82420-151">**Boolean**</span></span>

<span data-ttu-id="82420-152">Establezca en **true** si el sistema operativo es Windows XP Professional Edition; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="82420-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="82420-153">IsOS \_ Personal</span><span class="sxs-lookup"><span data-stu-id="82420-153">IsOS\_Personal</span></span>

<span data-ttu-id="82420-154">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="82420-154">**Boolean**</span></span>

<span data-ttu-id="82420-155">Establezca en **true** si el sistema operativo es Windows XP Home Edition; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="82420-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="82420-156">Lo siguiente solo es válido en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="82420-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="82420-157">DomainMember de IsOS \_</span><span class="sxs-lookup"><span data-stu-id="82420-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="82420-158">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="82420-158">**Boolean**</span></span>

<span data-ttu-id="82420-159">Establezca en **true** si el equipo es miembro de un dominio; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="82420-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="82420-160">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="82420-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="82420-161">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="82420-161">Examples</span></span>

<span data-ttu-id="82420-162">En los ejemplos siguientes se muestra el uso **de GetSystemInformation** para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="82420-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="82420-163">Jscript:</span><span class="sxs-lookup"><span data-stu-id="82420-163">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="82420-164">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="82420-164">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="82420-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82420-165">Requirements</span></span>



| <span data-ttu-id="82420-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="82420-166">Requirement</span></span> | <span data-ttu-id="82420-167">Valor</span><span class="sxs-lookup"><span data-stu-id="82420-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82420-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82420-168">Minimum supported client</span></span><br/> | <span data-ttu-id="82420-169">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="82420-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="82420-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82420-170">Minimum supported server</span></span><br/> | <span data-ttu-id="82420-171">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="82420-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="82420-172">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82420-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="82420-173"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="82420-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="82420-174">Idl</span><span class="sxs-lookup"><span data-stu-id="82420-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="82420-175"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="82420-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="82420-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82420-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82420-177"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="82420-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
