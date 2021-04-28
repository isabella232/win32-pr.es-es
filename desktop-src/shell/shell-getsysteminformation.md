---
description: 'Método Shell.GetSystemInformation: recupera información del sistema.'
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Método Shell.GetSystemInformation (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104283"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="15efa-103">Método Shell.GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="15efa-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="15efa-104">Recupera información del sistema.</span><span class="sxs-lookup"><span data-stu-id="15efa-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="15efa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15efa-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="15efa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15efa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15efa-107">*sName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="15efa-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15efa-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="15efa-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="15efa-109">Cadena **que** especifica la información del sistema que se solicita.</span><span class="sxs-lookup"><span data-stu-id="15efa-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15efa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15efa-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="15efa-111">JScript</span><span class="sxs-lookup"><span data-stu-id="15efa-111">JScript</span></span>

<span data-ttu-id="15efa-112">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="15efa-112">Type: **Variant**</span></span>

<span data-ttu-id="15efa-113">Devuelve el valor de la información solicitada del sistema.</span><span class="sxs-lookup"><span data-stu-id="15efa-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="15efa-114">El tipo de valor devuelto depende de la información del sistema que se solicite.</span><span class="sxs-lookup"><span data-stu-id="15efa-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="15efa-115">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="15efa-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="15efa-116">VB</span><span class="sxs-lookup"><span data-stu-id="15efa-116">VB</span></span>

<span data-ttu-id="15efa-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="15efa-117">Type: **Variant**</span></span>

<span data-ttu-id="15efa-118">Devuelve el valor de la información solicitada del sistema.</span><span class="sxs-lookup"><span data-stu-id="15efa-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="15efa-119">El tipo de valor devuelto depende de la información del sistema que se solicite.</span><span class="sxs-lookup"><span data-stu-id="15efa-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="15efa-120">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="15efa-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="15efa-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15efa-121">Remarks</span></span>

<span data-ttu-id="15efa-122">Este método se puede usar para solicitar muchos valores de información del sistema.</span><span class="sxs-lookup"><span data-stu-id="15efa-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="15efa-123">En la tabla siguiente se proporciona *el valor sName* que se usa para solicitar la información y el tipo asociado del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="15efa-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="15efa-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="15efa-124">*sName*</span></span>

<span data-ttu-id="15efa-125">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15efa-125">Return type</span></span>

<span data-ttu-id="15efa-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="15efa-126">Description</span></span>

<span data-ttu-id="15efa-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="15efa-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="15efa-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="15efa-128">**Boolean**</span></span>

<span data-ttu-id="15efa-129">Establezca en **true** si el servicio de directorio está disponible; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15efa-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="15efa-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="15efa-130">DoubleClickTime</span></span>

<span data-ttu-id="15efa-131">**Entero**</span><span class="sxs-lookup"><span data-stu-id="15efa-131">**Integer**</span></span>

<span data-ttu-id="15efa-132">Tiempo de doble clic, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="15efa-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="15efa-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="15efa-133">ProcessorLevel</span></span>

<span data-ttu-id="15efa-134">**Entero**</span><span class="sxs-lookup"><span data-stu-id="15efa-134">**Integer**</span></span>

<span data-ttu-id="15efa-135">**Windows Vista y versiones posteriores.**</span><span class="sxs-lookup"><span data-stu-id="15efa-135">**Windows Vista and later**.</span></span> <span data-ttu-id="15efa-136">Nivel de procesador.</span><span class="sxs-lookup"><span data-stu-id="15efa-136">The processor level.</span></span> <span data-ttu-id="15efa-137">Devuelve 3, 4 o 5 para procesadores de nivel x386, x486 y Pentium, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="15efa-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="15efa-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="15efa-138">ProcessorSpeed</span></span>

<span data-ttu-id="15efa-139">**Entero**</span><span class="sxs-lookup"><span data-stu-id="15efa-139">**Integer**</span></span>

<span data-ttu-id="15efa-140">Velocidad del procesador, en megahercios (MHz).</span><span class="sxs-lookup"><span data-stu-id="15efa-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="15efa-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="15efa-141">ProcessorArchitecture</span></span>

<span data-ttu-id="15efa-142">**Entero**</span><span class="sxs-lookup"><span data-stu-id="15efa-142">**Integer**</span></span>

<span data-ttu-id="15efa-143">Arquitectura del procesador.</span><span class="sxs-lookup"><span data-stu-id="15efa-143">The processor architecture.</span></span> <span data-ttu-id="15efa-144">Para obtener más información, vea la explicación del **miembro wProcessorArchitecture** de la [**estructura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)</span><span class="sxs-lookup"><span data-stu-id="15efa-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="15efa-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="15efa-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="15efa-146">**Entero**</span><span class="sxs-lookup"><span data-stu-id="15efa-146">**Integer**</span></span>

<span data-ttu-id="15efa-147">Cantidad de memoria física instalada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="15efa-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="15efa-148">Los siguientes son válidos solo en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="15efa-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="15efa-149">IsOS \_ Professional</span><span class="sxs-lookup"><span data-stu-id="15efa-149">IsOS\_Professional</span></span>

<span data-ttu-id="15efa-150">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="15efa-150">**Boolean**</span></span>

<span data-ttu-id="15efa-151">Se establece **en true** si el sistema operativo es Windows XP Professional Edition; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15efa-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="15efa-152">IsOS \_ Personal</span><span class="sxs-lookup"><span data-stu-id="15efa-152">IsOS\_Personal</span></span>

<span data-ttu-id="15efa-153">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="15efa-153">**Boolean**</span></span>

<span data-ttu-id="15efa-154">Se establece **en true** si el sistema operativo es Windows XP Home Edition; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15efa-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="15efa-155">Lo siguiente solo es válido en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="15efa-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="15efa-156">DomainMember de IsOS \_</span><span class="sxs-lookup"><span data-stu-id="15efa-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="15efa-157">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="15efa-157">**Boolean**</span></span>

<span data-ttu-id="15efa-158">Se establece **en true** si el equipo es miembro de un dominio; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="15efa-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="15efa-159">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="15efa-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="15efa-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="15efa-160">Examples</span></span>

<span data-ttu-id="15efa-161">En los ejemplos siguientes se muestra el uso **de GetSystemInformation** para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="15efa-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="15efa-162">Jscript:</span><span class="sxs-lookup"><span data-stu-id="15efa-162">JScript:</span></span>


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



<span data-ttu-id="15efa-163">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="15efa-163">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="15efa-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15efa-164">Requirements</span></span>



| <span data-ttu-id="15efa-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="15efa-165">Requirement</span></span> | <span data-ttu-id="15efa-166">Valor</span><span class="sxs-lookup"><span data-stu-id="15efa-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15efa-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15efa-167">Minimum supported client</span></span><br/> | <span data-ttu-id="15efa-168">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="15efa-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="15efa-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15efa-169">Minimum supported server</span></span><br/> | <span data-ttu-id="15efa-170">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15efa-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="15efa-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15efa-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="15efa-172"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="15efa-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="15efa-173">Idl</span><span class="sxs-lookup"><span data-stu-id="15efa-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15efa-174"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="15efa-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="15efa-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15efa-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15efa-176"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="15efa-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
