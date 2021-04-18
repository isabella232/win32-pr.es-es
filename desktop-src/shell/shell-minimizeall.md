---
description: Minimiza todas las ventanas del escritorio.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Método Shell. MinimizeAll (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985971"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="2cea4-103">Shell. MinimizeAll (método)</span><span class="sxs-lookup"><span data-stu-id="2cea4-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="2cea4-104">Minimiza todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="2cea4-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="2cea4-105">Este método tiene el mismo efecto que hacer clic con el botón secundario en la barra de tareas y seleccionar **minimizar todas las ventanas** en sistemas antiguos o hacer clic en el icono **Mostrar escritorio** del área Inicio rápido de la barra de tareas de Windows 2000 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2cea4-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cea4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cea4-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="2cea4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cea4-107">Parameters</span></span>

<span data-ttu-id="2cea4-108">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2cea4-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="2cea4-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2cea4-109">Examples</span></span>

<span data-ttu-id="2cea4-110">En el ejemplo siguiente se muestra **MinimizeAll** en uso.</span><span class="sxs-lookup"><span data-stu-id="2cea4-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="2cea4-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2cea4-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2cea4-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="2cea4-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="2cea4-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="2cea4-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2cea4-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2cea4-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2cea4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cea4-115">Requirements</span></span>



| <span data-ttu-id="2cea4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cea4-116">Requirement</span></span> | <span data-ttu-id="2cea4-117">Value</span><span class="sxs-lookup"><span data-stu-id="2cea4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cea4-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cea4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2cea4-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2cea4-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2cea4-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cea4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2cea4-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2cea4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cea4-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cea4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cea4-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cea4-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2cea4-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2cea4-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2cea4-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2cea4-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2cea4-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cea4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cea4-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2cea4-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cea4-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cea4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cea4-129">**Shell**</span><span class="sxs-lookup"><span data-stu-id="2cea4-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="2cea4-130">**UndoMinimizeALL**</span><span class="sxs-lookup"><span data-stu-id="2cea4-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




