---
description: Ejecuta la aplicación Panel de control especificada.
title: Método IShellDispatch.ControlPanelItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ControlPanelItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9A9B6B3F-FBBC-4e76-8018-8858B6392276
ms.openlocfilehash: 1a1c024b316472be00f119485326b704a4fe8dd0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842846"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="2ac18-103">Método IShellDispatch.ControlPanelItem</span><span class="sxs-lookup"><span data-stu-id="2ac18-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="2ac18-104">Ejecuta la aplicación Panel de control especificada.</span><span class="sxs-lookup"><span data-stu-id="2ac18-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="2ac18-105">Si la aplicación ya está abierta, activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="2ac18-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="2ac18-106">Desde Windows Vista, la mayoría Panel de control aplicaciones son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="2ac18-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="2ac18-107">Para abrir esas Panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="2ac18-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="2ac18-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2ac18-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="2ac18-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ac18-109">Syntax</span></span>


```JScript
IShellDispatch.ControlPanelItem(
  bstrDir
)
```


```VB

IShellDispatch.ControlPanelItem( _
  ByVal bstrDir As BSTR _
)
```





## <a name="parameters"></a><span data-ttu-id="2ac18-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ac18-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac18-111">*bstrDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="2ac18-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac18-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2ac18-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2ac18-113">El Panel de control de archivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2ac18-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac18-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ac18-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2ac18-115">JScript</span><span class="sxs-lookup"><span data-stu-id="2ac18-115">JScript</span></span>

<span data-ttu-id="2ac18-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2ac18-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="2ac18-117">VB</span><span class="sxs-lookup"><span data-stu-id="2ac18-117">VB</span></span>

<span data-ttu-id="2ac18-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2ac18-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac18-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ac18-119">Remarks</span></span>

<span data-ttu-id="2ac18-120">Este método se implementa y se accede a través del [**método Shell.ControlPanelItem.**](shell-controlpanelitem.md)</span><span class="sxs-lookup"><span data-stu-id="2ac18-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="2ac18-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2ac18-121">Examples</span></span>

<span data-ttu-id="2ac18-122">En los ejemplos siguientes se [**usa ControlPanelItem**](shell-controlpanelitem.md) para ejecutar el Panel de control **de** Propiedades de pantalla elemento.</span><span class="sxs-lookup"><span data-stu-id="2ac18-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="2ac18-123">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2ac18-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2ac18-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="2ac18-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="2ac18-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="2ac18-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellControlPanelItemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Shell_ControlPanelItem("desk.cpl")
       
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2ac18-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2ac18-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2ac18-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ac18-127">Requirements</span></span>



| <span data-ttu-id="2ac18-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ac18-128">Requirement</span></span> | <span data-ttu-id="2ac18-129">Value</span><span class="sxs-lookup"><span data-stu-id="2ac18-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac18-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ac18-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac18-131">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="2ac18-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2ac18-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ac18-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac18-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2ac18-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2ac18-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ac18-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac18-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac18-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2ac18-136">Idl</span><span class="sxs-lookup"><span data-stu-id="2ac18-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2ac18-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2ac18-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2ac18-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ac18-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ac18-139"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2ac18-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
