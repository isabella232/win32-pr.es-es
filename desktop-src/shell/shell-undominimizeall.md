---
description: Restaura todas las ventanas de escritorio al mismo estado en que se encontraban antes del último comando MinimizeAll.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Método Shell. UndoMinimizeALL (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277401"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="60c51-103">Shell. UndoMinimizeALL (método)</span><span class="sxs-lookup"><span data-stu-id="60c51-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="60c51-104">Restaura todas las ventanas de escritorio al mismo estado en que se encontraban antes del último comando [**MinimizeAll**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="60c51-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="60c51-105">Este método tiene el mismo efecto que hacer clic con el botón secundario en la barra de tareas y seleccionar **Deshacer minimizar todas las ventanas** en sistemas antiguos o hacer clic en el icono **Mostrar escritorio** del área Inicio rápido de la barra de tareas de Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="60c51-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c51-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60c51-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="60c51-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60c51-107">Parameters</span></span>

<span data-ttu-id="60c51-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="60c51-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="60c51-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="60c51-109">Examples</span></span>

<span data-ttu-id="60c51-110">En el ejemplo siguiente se muestra **UndoMinimizeALL** en uso.</span><span class="sxs-lookup"><span data-stu-id="60c51-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="60c51-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="60c51-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="60c51-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="60c51-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="60c51-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="60c51-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="60c51-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="60c51-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="60c51-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60c51-115">Requirements</span></span>



| <span data-ttu-id="60c51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="60c51-116">Requirement</span></span> | <span data-ttu-id="60c51-117">Value</span><span class="sxs-lookup"><span data-stu-id="60c51-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c51-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c51-118">Minimum supported client</span></span><br/> | <span data-ttu-id="60c51-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="60c51-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="60c51-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60c51-120">Minimum supported server</span></span><br/> | <span data-ttu-id="60c51-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="60c51-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="60c51-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60c51-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="60c51-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="60c51-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="60c51-124">IDL</span><span class="sxs-lookup"><span data-stu-id="60c51-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60c51-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60c51-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="60c51-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60c51-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c51-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="60c51-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




