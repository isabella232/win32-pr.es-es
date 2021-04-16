---
description: Restaura todas las ventanas de escritorio al estado en que se encontraban antes del último comando MinimizeAll.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Método IShellDispatch. UndoMinimizeALL (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543134"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="c95f6-103">IShellDispatch. UndoMinimizeALL, método</span><span class="sxs-lookup"><span data-stu-id="c95f6-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="c95f6-104">Restaura todas las ventanas de escritorio al estado en que se encontraban antes del último comando [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="c95f6-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="c95f6-105">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Deshacer minimizar todas las ventanas** (en sistemas anteriores) o hacer clic en el icono **Mostrar escritorio** en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="c95f6-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="c95f6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c95f6-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="c95f6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c95f6-107">Parameters</span></span>

<span data-ttu-id="c95f6-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c95f6-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c95f6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c95f6-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c95f6-110">JScript</span><span class="sxs-lookup"><span data-stu-id="c95f6-110">JScript</span></span>

<span data-ttu-id="c95f6-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c95f6-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c95f6-112">VB</span><span class="sxs-lookup"><span data-stu-id="c95f6-112">VB</span></span>

<span data-ttu-id="c95f6-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c95f6-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c95f6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c95f6-114">Remarks</span></span>

<span data-ttu-id="c95f6-115">Este método se implementa y se obtiene acceso a él a través del método [**Shell. UndoMinimizeAll**](./shell-undominimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="c95f6-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c95f6-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c95f6-116">Examples</span></span>

<span data-ttu-id="c95f6-117">En los siguientes ejemplos se muestra el uso de **UndoMinimizeALL** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c95f6-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c95f6-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="c95f6-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="c95f6-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="c95f6-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c95f6-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c95f6-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c95f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c95f6-121">Requirements</span></span>



| <span data-ttu-id="c95f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c95f6-122">Requirement</span></span> | <span data-ttu-id="c95f6-123">Value</span><span class="sxs-lookup"><span data-stu-id="c95f6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c95f6-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c95f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c95f6-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c95f6-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c95f6-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c95f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c95f6-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c95f6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c95f6-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c95f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c95f6-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c95f6-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c95f6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="c95f6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c95f6-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c95f6-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c95f6-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c95f6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c95f6-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c95f6-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
