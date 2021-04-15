---
description: Muestra una barra del explorador.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Método Shell. ShowBrowserBar (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d112399e62825714b4c060aeddcb8618ff73d478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985539"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="0ed15-103">Shell. ShowBrowserBar (método)</span><span class="sxs-lookup"><span data-stu-id="0ed15-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="0ed15-104">Muestra una barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="0ed15-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed15-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ed15-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="0ed15-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ed15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed15-107">*sCLSID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ed15-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed15-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="0ed15-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="0ed15-109">**Cadena** que contiene la forma de cadena del CLSID de la barra del explorador que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="0ed15-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="0ed15-110">El objeto se debe registrar como un objeto de barra del explorador con una \_ categoría de componente CATID InfoBand.</span><span class="sxs-lookup"><span data-stu-id="0ed15-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="0ed15-111">Para obtener más información, vea [crear barras del explorador personalizadas, bandas de herramientas y bandas del escritorio](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="0ed15-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ed15-112">*vShow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0ed15-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ed15-113">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="0ed15-113">Type: **Variant**</span></span>

<span data-ttu-id="0ed15-114">Establézcalo en **true** para mostrar la barra del explorador o en **false** para ocultarla.</span><span class="sxs-lookup"><span data-stu-id="0ed15-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ed15-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ed15-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0ed15-116">JScript</span><span class="sxs-lookup"><span data-stu-id="0ed15-116">JScript</span></span>

<span data-ttu-id="0ed15-117">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="0ed15-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="0ed15-118">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0ed15-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="0ed15-119">VB</span><span class="sxs-lookup"><span data-stu-id="0ed15-119">VB</span></span>

<span data-ttu-id="0ed15-120">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="0ed15-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="0ed15-121">Devuelve _ *true*\* si es correcto; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="0ed15-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ed15-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ed15-122">Remarks</span></span>

<span data-ttu-id="0ed15-123">Puede mostrar una de las barras del explorador estándar estableciendo el parámetro *sCLSID* en el CLSID de esa barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="0ed15-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="0ed15-124">Las barras del explorador estándar y sus cadenas CLSID son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="0ed15-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="0ed15-125">Barra del explorador</span><span class="sxs-lookup"><span data-stu-id="0ed15-125">Explorer Bar</span></span> | <span data-ttu-id="0ed15-126">Cadena CLSID</span><span class="sxs-lookup"><span data-stu-id="0ed15-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="0ed15-127">Favoritos</span><span class="sxs-lookup"><span data-stu-id="0ed15-127">Favorites</span></span>    | <span data-ttu-id="0ed15-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="0ed15-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="0ed15-129">Carpetas</span><span class="sxs-lookup"><span data-stu-id="0ed15-129">Folders</span></span>      | <span data-ttu-id="0ed15-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="0ed15-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="0ed15-131">Historial</span><span class="sxs-lookup"><span data-stu-id="0ed15-131">History</span></span>      | <span data-ttu-id="0ed15-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="0ed15-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="0ed15-133">Buscar</span><span class="sxs-lookup"><span data-stu-id="0ed15-133">Search</span></span>       | <span data-ttu-id="0ed15-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="0ed15-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="0ed15-135">Este método no está disponible actualmente en Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0ed15-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="0ed15-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0ed15-136">Examples</span></span>

<span data-ttu-id="0ed15-137">En los siguientes ejemplos se muestra el uso de **Shell. ShowBrowserBar** para mostrar la barra de explorador **Favoritos** .</span><span class="sxs-lookup"><span data-stu-id="0ed15-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="0ed15-138">Se muestra el uso de JScript y VBScript.</span><span class="sxs-lookup"><span data-stu-id="0ed15-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="0ed15-139">JScript.net</span><span class="sxs-lookup"><span data-stu-id="0ed15-139">JScript:</span></span>


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



<span data-ttu-id="0ed15-140">VBScript</span><span class="sxs-lookup"><span data-stu-id="0ed15-140">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0ed15-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed15-141">Requirements</span></span>



| <span data-ttu-id="0ed15-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed15-142">Requirement</span></span> | <span data-ttu-id="0ed15-143">Value</span><span class="sxs-lookup"><span data-stu-id="0ed15-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed15-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ed15-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed15-145">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0ed15-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ed15-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0ed15-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed15-147">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ed15-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0ed15-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ed15-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ed15-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed15-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0ed15-150">IDL</span><span class="sxs-lookup"><span data-stu-id="0ed15-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ed15-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ed15-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0ed15-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0ed15-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ed15-153"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed15-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
