---
description: Muestra el cuadro de diálogo cerrar Windows. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar apagar.
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Método Shell. ShutdownWindows (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 804a1e211e191206d20f83d85dee2202492bfd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277404"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="b31f3-104">Shell. ShutdownWindows (método)</span><span class="sxs-lookup"><span data-stu-id="b31f3-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="b31f3-105">Muestra el cuadro de diálogo **cerrar Windows** .</span><span class="sxs-lookup"><span data-stu-id="b31f3-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="b31f3-106">Esto es lo mismo que hacer clic en el menú **Inicio** y seleccionar **apagar**.</span><span class="sxs-lookup"><span data-stu-id="b31f3-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b31f3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b31f3-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="b31f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b31f3-108">Parameters</span></span>

<span data-ttu-id="b31f3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b31f3-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="b31f3-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b31f3-110">Examples</span></span>

<span data-ttu-id="b31f3-111">En el ejemplo siguiente se muestra **ShutdownWindows** en uso.</span><span class="sxs-lookup"><span data-stu-id="b31f3-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="b31f3-112">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b31f3-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b31f3-113">JScript.net</span><span class="sxs-lookup"><span data-stu-id="b31f3-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="b31f3-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="b31f3-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="b31f3-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b31f3-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b31f3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b31f3-116">Requirements</span></span>



| <span data-ttu-id="b31f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b31f3-117">Requirement</span></span> | <span data-ttu-id="b31f3-118">Value</span><span class="sxs-lookup"><span data-stu-id="b31f3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b31f3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b31f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b31f3-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b31f3-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b31f3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b31f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b31f3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b31f3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b31f3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b31f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b31f3-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b31f3-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b31f3-125">IDL</span><span class="sxs-lookup"><span data-stu-id="b31f3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b31f3-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b31f3-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b31f3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b31f3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b31f3-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b31f3-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




