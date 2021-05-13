---
description: Ejecuta la aplicación Panel de control especificada \* (.cpl).
title: Método Shell.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 54979bbd-b36b-4b5b-a8a0-5f63e9526fa5
ms.openlocfilehash: 04d2493f5d0ec5b86d19689cb8e7c2a02a82e536
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841806"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="12630-103">Método Shell.ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="12630-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="12630-104">Ejecuta la aplicación Panel de control especificada \* (.cpl).</span><span class="sxs-lookup"><span data-stu-id="12630-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="12630-105">Si la aplicación ya está abierta, activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="12630-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="12630-106">Desde Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="12630-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="12630-107">Para abrir esas Panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="12630-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="12630-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="12630-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="12630-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12630-109">Syntax</span></span>


```JScript
Shell.ControlPanelItem(
  bstrDir
)
```


```VB

Shell.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="12630-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12630-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12630-111">*bstrDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="12630-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12630-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="12630-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="12630-113">El Panel de control de archivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="12630-113">The Control Panel application's file name.</span></span> <span data-ttu-id="12630-114">Todas Panel de control aplicaciones tienen la extensión .cpl.</span><span class="sxs-lookup"><span data-stu-id="12630-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12630-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="12630-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="12630-116">JScript</span><span class="sxs-lookup"><span data-stu-id="12630-116">JScript</span></span>

<span data-ttu-id="12630-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="12630-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="12630-118">VB</span><span class="sxs-lookup"><span data-stu-id="12630-118">VB</span></span>

<span data-ttu-id="12630-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="12630-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="12630-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="12630-120">Examples</span></span>

<span data-ttu-id="12630-121">En el ejemplo siguiente se **usa ControlPanelItem** para ejecutar el Panel de control **de** Propiedades de pantalla elemento.</span><span class="sxs-lookup"><span data-stu-id="12630-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="12630-122">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="12630-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="12630-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="12630-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="12630-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="12630-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="12630-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="12630-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="12630-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12630-126">Requirements</span></span>



| <span data-ttu-id="12630-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="12630-127">Requirement</span></span> | <span data-ttu-id="12630-128">Value</span><span class="sxs-lookup"><span data-stu-id="12630-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12630-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12630-129">Minimum supported client</span></span><br/> | <span data-ttu-id="12630-130">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="12630-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="12630-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12630-131">Minimum supported server</span></span><br/> | <span data-ttu-id="12630-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12630-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12630-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12630-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="12630-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="12630-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="12630-135">Idl</span><span class="sxs-lookup"><span data-stu-id="12630-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12630-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="12630-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="12630-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12630-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12630-138"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="12630-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
