---
description: Ejecuta la aplicación del panel de control especificada.
title: Método IShellDispatch. ControlPanelItem (Shldisp. h)
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
ms.openlocfilehash: 72164ff76cbcf15703bc91160e6211b38015f989
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543163"
---
# <a name="ishelldispatchcontrolpanelitem-method"></a><span data-ttu-id="940a2-103">IShellDispatch. ControlPanelItem, método</span><span class="sxs-lookup"><span data-stu-id="940a2-103">IShellDispatch.ControlPanelItem method</span></span>

<span data-ttu-id="940a2-104">Ejecuta la aplicación del panel de control especificada.</span><span class="sxs-lookup"><span data-stu-id="940a2-104">Runs the specified Control Panel application.</span></span> <span data-ttu-id="940a2-105">Si la aplicación ya está abierta, se activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="940a2-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="940a2-106">A partir de Windows Vista, la mayoría de las aplicaciones del panel de control son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="940a2-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="940a2-107">Para abrir esas aplicaciones del panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="940a2-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="940a2-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="940a2-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="940a2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="940a2-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="940a2-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="940a2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="940a2-111">*bstrDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="940a2-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="940a2-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="940a2-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="940a2-113">Nombre de archivo de la aplicación del panel de control.</span><span class="sxs-lookup"><span data-stu-id="940a2-113">The Control Panel application's file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="940a2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="940a2-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="940a2-115">JScript</span><span class="sxs-lookup"><span data-stu-id="940a2-115">JScript</span></span>

<span data-ttu-id="940a2-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="940a2-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="940a2-117">VB</span><span class="sxs-lookup"><span data-stu-id="940a2-117">VB</span></span>

<span data-ttu-id="940a2-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="940a2-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="940a2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="940a2-119">Remarks</span></span>

<span data-ttu-id="940a2-120">Este método se implementa y se obtiene acceso a él a través del método [**Shell. ControlPanelItem**](shell-controlpanelitem.md) .</span><span class="sxs-lookup"><span data-stu-id="940a2-120">This method is implemented and accessed through the [**Shell.ControlPanelItem**](shell-controlpanelitem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="940a2-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="940a2-121">Examples</span></span>

<span data-ttu-id="940a2-122">En los ejemplos siguientes se usa [**ControlPanelItem**](shell-controlpanelitem.md) para ejecutar el elemento **propiedades de presentación** del panel de control.</span><span class="sxs-lookup"><span data-stu-id="940a2-122">The following examples use [**ControlPanelItem**](shell-controlpanelitem.md) to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="940a2-123">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="940a2-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="940a2-124">JScript.net</span><span class="sxs-lookup"><span data-stu-id="940a2-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Shell_ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="940a2-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="940a2-125">VBScript:</span></span>


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



<span data-ttu-id="940a2-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="940a2-126">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Shell_ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="940a2-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="940a2-127">Requirements</span></span>



| <span data-ttu-id="940a2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="940a2-128">Requirement</span></span> | <span data-ttu-id="940a2-129">Value</span><span class="sxs-lookup"><span data-stu-id="940a2-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="940a2-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="940a2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="940a2-131">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="940a2-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="940a2-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="940a2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="940a2-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="940a2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="940a2-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="940a2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="940a2-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="940a2-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="940a2-136">IDL</span><span class="sxs-lookup"><span data-stu-id="940a2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="940a2-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="940a2-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="940a2-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="940a2-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="940a2-139"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="940a2-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
