---
description: Minimiza todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar minimizar todas las ventanas en sistemas antiguos o hacer clic en el icono Mostrar escritorio en la barra de tareas.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Método IShellDispatch. MinimizeAll (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543147"
---
# <a name="ishelldispatchminimizeall-method"></a><span data-ttu-id="cf3c3-104">IShellDispatch. MinimizeAll, método</span><span class="sxs-lookup"><span data-stu-id="cf3c3-104">IShellDispatch.MinimizeAll method</span></span>

<span data-ttu-id="cf3c3-105">Minimiza todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="cf3c3-105">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="cf3c3-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **minimizar todas las ventanas** en sistemas antiguos o hacer clic en el icono **Mostrar escritorio** en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="cf3c3-106">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon on the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf3c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf3c3-107">Syntax</span></span>


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a><span data-ttu-id="cf3c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf3c3-108">Parameters</span></span>

<span data-ttu-id="cf3c3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf3c3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf3c3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf3c3-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cf3c3-111">JScript</span><span class="sxs-lookup"><span data-stu-id="cf3c3-111">JScript</span></span>

<span data-ttu-id="cf3c3-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cf3c3-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cf3c3-113">VB</span><span class="sxs-lookup"><span data-stu-id="cf3c3-113">VB</span></span>

<span data-ttu-id="cf3c3-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cf3c3-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf3c3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf3c3-115">Remarks</span></span>

<span data-ttu-id="cf3c3-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="cf3c3-116">This method is implemented and accessed through the [**Shell.MinimizeAll**](shell-minimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cf3c3-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cf3c3-117">Examples</span></span>

<span data-ttu-id="cf3c3-118">En los siguientes ejemplos se muestra el uso de **MinimizeAll** en uso para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cf3c3-118">The following examples show the use of **MinimizeAll** in use for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cf3c3-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="cf3c3-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="cf3c3-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="cf3c3-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cf3c3-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cf3c3-121">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cf3c3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf3c3-122">Requirements</span></span>



| <span data-ttu-id="cf3c3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf3c3-123">Requirement</span></span> | <span data-ttu-id="cf3c3-124">Value</span><span class="sxs-lookup"><span data-stu-id="cf3c3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf3c3-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf3c3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cf3c3-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cf3c3-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cf3c3-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf3c3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cf3c3-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cf3c3-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cf3c3-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf3c3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf3c3-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf3c3-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cf3c3-131">IDL</span><span class="sxs-lookup"><span data-stu-id="cf3c3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cf3c3-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cf3c3-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cf3c3-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf3c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf3c3-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cf3c3-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf3c3-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf3c3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf3c3-136">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="cf3c3-136">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="cf3c3-137">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="cf3c3-137">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




