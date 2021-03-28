---
description: Organiza en cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar ventanas en cascada.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Método Shell. CascadeWindows (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545915"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="a5d70-104">Shell. CascadeWindows (método)</span><span class="sxs-lookup"><span data-stu-id="a5d70-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="a5d70-105">Organiza en cascada todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="a5d70-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="a5d70-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **ventanas en cascada**.</span><span class="sxs-lookup"><span data-stu-id="a5d70-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d70-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5d70-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="a5d70-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5d70-108">Parameters</span></span>

<span data-ttu-id="a5d70-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a5d70-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5d70-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5d70-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a5d70-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a5d70-111">JScript</span></span>

<span data-ttu-id="a5d70-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a5d70-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a5d70-113">VB</span><span class="sxs-lookup"><span data-stu-id="a5d70-113">VB</span></span>

<span data-ttu-id="a5d70-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a5d70-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="a5d70-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a5d70-115">Examples</span></span>

<span data-ttu-id="a5d70-116">En el ejemplo siguiente se muestra **CascadeWindows** en uso.</span><span class="sxs-lookup"><span data-stu-id="a5d70-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="a5d70-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a5d70-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a5d70-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="a5d70-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="a5d70-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="a5d70-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a5d70-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a5d70-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a5d70-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d70-121">Requirements</span></span>



| <span data-ttu-id="a5d70-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d70-122">Requirement</span></span> | <span data-ttu-id="a5d70-123">Value</span><span class="sxs-lookup"><span data-stu-id="a5d70-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d70-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d70-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d70-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a5d70-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a5d70-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d70-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d70-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5d70-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5d70-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5d70-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d70-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d70-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a5d70-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a5d70-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5d70-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5d70-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a5d70-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5d70-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d70-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a5d70-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




