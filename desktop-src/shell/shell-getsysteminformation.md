---
description: Recupera información del sistema.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Método Shell. GetSystemInformation (Shldisp. h)
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
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985974"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="cc96a-103">Shell. GetSystemInformation (método)</span><span class="sxs-lookup"><span data-stu-id="cc96a-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="cc96a-104">Recupera información del sistema.</span><span class="sxs-lookup"><span data-stu-id="cc96a-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc96a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc96a-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="cc96a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc96a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc96a-107">*sName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cc96a-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc96a-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cc96a-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cc96a-109">**Cadena** que especifica la información del sistema que se solicita.</span><span class="sxs-lookup"><span data-stu-id="cc96a-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc96a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc96a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cc96a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="cc96a-111">JScript</span></span>

<span data-ttu-id="cc96a-112">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="cc96a-112">Type: **Variant**</span></span>

<span data-ttu-id="cc96a-113">Devuelve el valor de la información del sistema solicitada.</span><span class="sxs-lookup"><span data-stu-id="cc96a-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="cc96a-114">El tipo de valor devuelto depende de la información del sistema que se solicite.</span><span class="sxs-lookup"><span data-stu-id="cc96a-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="cc96a-115">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cc96a-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="cc96a-116">VB</span><span class="sxs-lookup"><span data-stu-id="cc96a-116">VB</span></span>

<span data-ttu-id="cc96a-117">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="cc96a-117">Type: **Variant**</span></span>

<span data-ttu-id="cc96a-118">Devuelve el valor de la información del sistema solicitada.</span><span class="sxs-lookup"><span data-stu-id="cc96a-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="cc96a-119">El tipo de valor devuelto depende de la información del sistema que se solicite.</span><span class="sxs-lookup"><span data-stu-id="cc96a-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="cc96a-120">Para obtener información detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cc96a-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc96a-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc96a-121">Remarks</span></span>

<span data-ttu-id="cc96a-122">Este método se puede utilizar para solicitar muchos valores de información del sistema.</span><span class="sxs-lookup"><span data-stu-id="cc96a-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="cc96a-123">En la tabla siguiente se proporciona el valor de *sName* que se usa para solicitar la información y el tipo asociado del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="cc96a-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="cc96a-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="cc96a-124">*sName*</span></span>

<span data-ttu-id="cc96a-125">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc96a-125">Return type</span></span>

<span data-ttu-id="cc96a-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc96a-126">Description</span></span>

<span data-ttu-id="cc96a-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="cc96a-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="cc96a-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc96a-128">**Boolean**</span></span>

<span data-ttu-id="cc96a-129">Establézcalo en **true** si el servicio de directorio está disponible; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc96a-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="cc96a-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="cc96a-130">DoubleClickTime</span></span>

<span data-ttu-id="cc96a-131">**Entero**</span><span class="sxs-lookup"><span data-stu-id="cc96a-131">**Integer**</span></span>

<span data-ttu-id="cc96a-132">Tiempo de doble clic, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="cc96a-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="cc96a-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="cc96a-133">ProcessorLevel</span></span>

<span data-ttu-id="cc96a-134">**Entero**</span><span class="sxs-lookup"><span data-stu-id="cc96a-134">**Integer**</span></span>

<span data-ttu-id="cc96a-135">**Windows Vista y versiones posteriores**.</span><span class="sxs-lookup"><span data-stu-id="cc96a-135">**Windows Vista and later**.</span></span> <span data-ttu-id="cc96a-136">Nivel de procesador.</span><span class="sxs-lookup"><span data-stu-id="cc96a-136">The processor level.</span></span> <span data-ttu-id="cc96a-137">Devuelve 3, 4 o 5 para los procesadores x386, x486 y Pentium, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cc96a-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="cc96a-138">Velocidaddeprocesador</span><span class="sxs-lookup"><span data-stu-id="cc96a-138">ProcessorSpeed</span></span>

<span data-ttu-id="cc96a-139">**Entero**</span><span class="sxs-lookup"><span data-stu-id="cc96a-139">**Integer**</span></span>

<span data-ttu-id="cc96a-140">La velocidad del procesador, en megahercios (MHz).</span><span class="sxs-lookup"><span data-stu-id="cc96a-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="cc96a-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="cc96a-141">ProcessorArchitecture</span></span>

<span data-ttu-id="cc96a-142">**Entero**</span><span class="sxs-lookup"><span data-stu-id="cc96a-142">**Integer**</span></span>

<span data-ttu-id="cc96a-143">La arquitectura del procesador.</span><span class="sxs-lookup"><span data-stu-id="cc96a-143">The processor architecture.</span></span> <span data-ttu-id="cc96a-144">Para obtener más información, consulte la descripción del miembro **wProcessorArchitecture** de la estructura de [**\_ información del sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="cc96a-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="cc96a-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="cc96a-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="cc96a-146">**Entero**</span><span class="sxs-lookup"><span data-stu-id="cc96a-146">**Integer**</span></span>

<span data-ttu-id="cc96a-147">La cantidad de memoria física instalada, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cc96a-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="cc96a-148">Lo siguiente solo es válido en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cc96a-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="cc96a-149">Archivos ISO \_ Professional</span><span class="sxs-lookup"><span data-stu-id="cc96a-149">IsOS\_Professional</span></span>

<span data-ttu-id="cc96a-150">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc96a-150">**Boolean**</span></span>

<span data-ttu-id="cc96a-151">Establézcalo en **true** si el sistema operativo es Windows XP Professional Edition; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc96a-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="cc96a-152">Personal de archivos ISO \_</span><span class="sxs-lookup"><span data-stu-id="cc96a-152">IsOS\_Personal</span></span>

<span data-ttu-id="cc96a-153">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc96a-153">**Boolean**</span></span>

<span data-ttu-id="cc96a-154">Establézcalo en **true** si el sistema operativo es Windows XP Home Edition; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc96a-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="cc96a-155">Lo siguiente solo es válido en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="cc96a-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="cc96a-156">Archivos ISO \_ DomainMember</span><span class="sxs-lookup"><span data-stu-id="cc96a-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="cc96a-157">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cc96a-157">**Boolean**</span></span>

<span data-ttu-id="cc96a-158">Establézcalo en **true** si el equipo es miembro de un dominio; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="cc96a-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="cc96a-159">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cc96a-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="cc96a-160">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc96a-160">Examples</span></span>

<span data-ttu-id="cc96a-161">En los siguientes ejemplos se muestra el uso de **GetSystemInformation** para JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="cc96a-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="cc96a-162">JScript.net</span><span class="sxs-lookup"><span data-stu-id="cc96a-162">JScript:</span></span>


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



<span data-ttu-id="cc96a-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="cc96a-163">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cc96a-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc96a-164">Requirements</span></span>



| <span data-ttu-id="cc96a-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc96a-165">Requirement</span></span> | <span data-ttu-id="cc96a-166">Value</span><span class="sxs-lookup"><span data-stu-id="cc96a-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc96a-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc96a-167">Minimum supported client</span></span><br/> | <span data-ttu-id="cc96a-168">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cc96a-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc96a-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc96a-169">Minimum supported server</span></span><br/> | <span data-ttu-id="cc96a-170">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc96a-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cc96a-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc96a-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc96a-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc96a-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cc96a-173">IDL</span><span class="sxs-lookup"><span data-stu-id="cc96a-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cc96a-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc96a-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cc96a-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc96a-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc96a-176"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cc96a-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
