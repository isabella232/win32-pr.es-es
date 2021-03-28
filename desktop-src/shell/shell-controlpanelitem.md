---
description: Ejecuta la aplicación del panel de control ( \* . cpl) especificada.
title: Método Shell. ControlPanelItem (Shldisp. h)
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
ms.openlocfilehash: dec27dab8bd37cc9c15e603c24a54d528cea331a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985618"
---
# <a name="shellcontrolpanelitem-method"></a><span data-ttu-id="27fc9-103">Shell. ControlPanelItem (método)</span><span class="sxs-lookup"><span data-stu-id="27fc9-103">Shell.ControlPanelItem method</span></span>

<span data-ttu-id="27fc9-104">Ejecuta la aplicación del panel de control ( \* . cpl) especificada.</span><span class="sxs-lookup"><span data-stu-id="27fc9-104">Runs the specified Control Panel (\*.cpl) application.</span></span> <span data-ttu-id="27fc9-105">Si la aplicación ya está abierta, se activará la instancia en ejecución.</span><span class="sxs-lookup"><span data-stu-id="27fc9-105">If the application is already open, it will activate the running instance.</span></span>

> [!Note]  
> <span data-ttu-id="27fc9-106">A partir de Windows Vista, la mayoría de las aplicaciones del panel de control son elementos de Shell y no se pueden abrir con esta función.</span><span class="sxs-lookup"><span data-stu-id="27fc9-106">As of Windows Vista, most Control Panel applications are Shell items and cannot be opened with this function.</span></span> <span data-ttu-id="27fc9-107">Para abrir esas aplicaciones del panel de control, pase el nombre canónico a control.exe.</span><span class="sxs-lookup"><span data-stu-id="27fc9-107">To open those Control Panel applications, pass the canonical name to control.exe.</span></span> <span data-ttu-id="27fc9-108">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="27fc9-108">For example:</span></span>
>
> ``` syntax
> control.exe /name Microsoft.Personalization
> ```

 

## <a name="syntax"></a><span data-ttu-id="27fc9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27fc9-109">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="27fc9-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="27fc9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27fc9-111">*bstrDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="27fc9-111">*bstrDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fc9-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="27fc9-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="27fc9-113">Nombre de archivo de la aplicación del panel de control.</span><span class="sxs-lookup"><span data-stu-id="27fc9-113">The Control Panel application's file name.</span></span> <span data-ttu-id="27fc9-114">Todas las aplicaciones del panel de control tienen la extensión. cpl.</span><span class="sxs-lookup"><span data-stu-id="27fc9-114">All Control Panel applications have the .cpl extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27fc9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27fc9-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="27fc9-116">JScript</span><span class="sxs-lookup"><span data-stu-id="27fc9-116">JScript</span></span>

<span data-ttu-id="27fc9-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="27fc9-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="27fc9-118">VB</span><span class="sxs-lookup"><span data-stu-id="27fc9-118">VB</span></span>

<span data-ttu-id="27fc9-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="27fc9-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="27fc9-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="27fc9-120">Examples</span></span>

<span data-ttu-id="27fc9-121">En el ejemplo siguiente se usa **ControlPanelItem** para ejecutar el elemento de **propiedades de presentación** del panel de control.</span><span class="sxs-lookup"><span data-stu-id="27fc9-121">The following example uses **ControlPanelItem** to run the Control Panel's **Display Properties** item.</span></span> <span data-ttu-id="27fc9-122">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="27fc9-122">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="27fc9-123">JScript.net</span><span class="sxs-lookup"><span data-stu-id="27fc9-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellControlPanelItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ControlPanelItem("desk.cpl");
    }
</script>
```



<span data-ttu-id="27fc9-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="27fc9-124">VBScript:</span></span>


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



<span data-ttu-id="27fc9-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="27fc9-125">Visual Basic:</span></span>


```VB
Private Sub fnShellControlPanelItemVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ControlPanelItem ("desk.cpl")
    
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="27fc9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27fc9-126">Requirements</span></span>



| <span data-ttu-id="27fc9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fc9-127">Requirement</span></span> | <span data-ttu-id="27fc9-128">Value</span><span class="sxs-lookup"><span data-stu-id="27fc9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27fc9-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27fc9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="27fc9-130">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="27fc9-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="27fc9-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27fc9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="27fc9-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="27fc9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="27fc9-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27fc9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="27fc9-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="27fc9-134"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="27fc9-135">IDL</span><span class="sxs-lookup"><span data-stu-id="27fc9-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27fc9-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27fc9-136"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="27fc9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="27fc9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27fc9-138"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="27fc9-138"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
