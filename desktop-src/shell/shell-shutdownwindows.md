---
description: 'Método Shell.ShutdownWindows: muestra el cuadro de diálogo Apagar Windows. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar Apagar.'
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Método Shell.ShutdownWindows (Shldisp.h)
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
ms.openlocfilehash: 2a3c0746caccb360f6f7f0156b72a57ed0a2d2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083673"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="499ae-104">Método Shell.ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="499ae-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="499ae-105">Muestra el **cuadro de diálogo Apagar Windows.**</span><span class="sxs-lookup"><span data-stu-id="499ae-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="499ae-106">Esto es lo mismo que hacer clic en **el menú** Inicio y seleccionar **Apagar.**</span><span class="sxs-lookup"><span data-stu-id="499ae-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="499ae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="499ae-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="499ae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="499ae-108">Parameters</span></span>

<span data-ttu-id="499ae-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="499ae-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="499ae-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="499ae-110">Examples</span></span>

<span data-ttu-id="499ae-111">En el ejemplo siguiente se **muestra ShutdownWindows** en uso.</span><span class="sxs-lookup"><span data-stu-id="499ae-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="499ae-112">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="499ae-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="499ae-113">Jscript:</span><span class="sxs-lookup"><span data-stu-id="499ae-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="499ae-114">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="499ae-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="499ae-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="499ae-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="499ae-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="499ae-116">Requirements</span></span>



| <span data-ttu-id="499ae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="499ae-117">Requirement</span></span> | <span data-ttu-id="499ae-118">Valor</span><span class="sxs-lookup"><span data-stu-id="499ae-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="499ae-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="499ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="499ae-120">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="499ae-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="499ae-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="499ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="499ae-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="499ae-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="499ae-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="499ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="499ae-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="499ae-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="499ae-125">Idl</span><span class="sxs-lookup"><span data-stu-id="499ae-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="499ae-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="499ae-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="499ae-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="499ae-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="499ae-128"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="499ae-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




