---
description: Muestra una barra del explorador.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Método IShellDispatch2. ShowBrowserBar (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984667"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="11c47-103">IShellDispatch2. ShowBrowserBar, método</span><span class="sxs-lookup"><span data-stu-id="11c47-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="11c47-104">Muestra una barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="11c47-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11c47-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="11c47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11c47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c47-107">*sCLSID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11c47-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c47-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="11c47-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="11c47-109">**Cadena** que contiene la forma de cadena del CLSID de la barra del explorador que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="11c47-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="11c47-110">El objeto se debe registrar como un objeto de barra del explorador con una \_ categoría de componente CATID InfoBand.</span><span class="sxs-lookup"><span data-stu-id="11c47-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="11c47-111">Para obtener más información, vea [crear barras del explorador personalizadas, bandas de herramientas y bandas del escritorio](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="11c47-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="11c47-112">*vShow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11c47-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c47-113">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="11c47-113">Type: **Variant**</span></span>

<span data-ttu-id="11c47-114">Establézcalo en **true** para mostrar la barra del explorador o en **false** para ocultarla.</span><span class="sxs-lookup"><span data-stu-id="11c47-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c47-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11c47-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="11c47-116">JScript</span><span class="sxs-lookup"><span data-stu-id="11c47-116">JScript</span></span>

<span data-ttu-id="11c47-117">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="11c47-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="11c47-118">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="11c47-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="11c47-119">VB</span><span class="sxs-lookup"><span data-stu-id="11c47-119">VB</span></span>

<span data-ttu-id="11c47-120">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="11c47-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="11c47-121">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="11c47-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11c47-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11c47-122">Remarks</span></span>

<span data-ttu-id="11c47-123">Este método se implementa y se obtiene acceso a él a través del método [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .</span><span class="sxs-lookup"><span data-stu-id="11c47-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="11c47-124">Puede mostrar una de las barras del explorador estándar estableciendo el parámetro *sCLSID* en el CLSID de esa barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="11c47-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="11c47-125">Las barras del explorador estándar y sus cadenas CLSID son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="11c47-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="11c47-126">Barra del explorador</span><span class="sxs-lookup"><span data-stu-id="11c47-126">Explorer Bar</span></span> | <span data-ttu-id="11c47-127">Cadena CLSID</span><span class="sxs-lookup"><span data-stu-id="11c47-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="11c47-128">Favoritos</span><span class="sxs-lookup"><span data-stu-id="11c47-128">Favorites</span></span>    | <span data-ttu-id="11c47-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="11c47-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="11c47-130">Carpetas</span><span class="sxs-lookup"><span data-stu-id="11c47-130">Folders</span></span>      | <span data-ttu-id="11c47-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="11c47-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="11c47-132">Historial</span><span class="sxs-lookup"><span data-stu-id="11c47-132">History</span></span>      | <span data-ttu-id="11c47-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="11c47-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="11c47-134">Buscar</span><span class="sxs-lookup"><span data-stu-id="11c47-134">Search</span></span>       | <span data-ttu-id="11c47-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="11c47-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="11c47-136">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11c47-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="11c47-137">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="11c47-137">Examples</span></span>

<span data-ttu-id="11c47-138">En los siguientes ejemplos se muestra el uso de **ShowBrowserBar** para mostrar la barra del explorador **Favoritos** .</span><span class="sxs-lookup"><span data-stu-id="11c47-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="11c47-139">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="11c47-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="11c47-140">JScript.net</span><span class="sxs-lookup"><span data-stu-id="11c47-140">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="11c47-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="11c47-141">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="11c47-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11c47-142">Requirements</span></span>



| <span data-ttu-id="11c47-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="11c47-143">Requirement</span></span> | <span data-ttu-id="11c47-144">Value</span><span class="sxs-lookup"><span data-stu-id="11c47-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11c47-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11c47-145">Minimum supported client</span></span><br/> | <span data-ttu-id="11c47-146">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="11c47-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11c47-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11c47-147">Minimum supported server</span></span><br/> | <span data-ttu-id="11c47-148">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="11c47-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="11c47-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11c47-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="11c47-150"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11c47-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="11c47-151">IDL</span><span class="sxs-lookup"><span data-stu-id="11c47-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11c47-152"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11c47-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="11c47-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11c47-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11c47-154"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="11c47-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
