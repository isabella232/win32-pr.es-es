---
description: 'Método IShellDispatch.ShutdownWindows: muestra el cuadro de diálogo Apagar Windows. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar Apagar.'
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Método IShellDispatch.ShutdownWindows (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5146e17d17ba0f082ad2d80f91ae05c176cf44ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100473"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="6edfa-104">Método IShellDispatch.ShutdownWindows</span><span class="sxs-lookup"><span data-stu-id="6edfa-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="6edfa-105">Muestra el **cuadro de diálogo Apagar Windows.**</span><span class="sxs-lookup"><span data-stu-id="6edfa-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="6edfa-106">Esto es lo mismo que hacer clic en **el menú** Inicio y seleccionar **Apagar.**</span><span class="sxs-lookup"><span data-stu-id="6edfa-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6edfa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6edfa-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="6edfa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6edfa-108">Parameters</span></span>

<span data-ttu-id="6edfa-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6edfa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6edfa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6edfa-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6edfa-111">JScript</span><span class="sxs-lookup"><span data-stu-id="6edfa-111">JScript</span></span>

<span data-ttu-id="6edfa-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6edfa-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="6edfa-113">VB</span><span class="sxs-lookup"><span data-stu-id="6edfa-113">VB</span></span>

<span data-ttu-id="6edfa-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6edfa-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edfa-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6edfa-115">Remarks</span></span>

<span data-ttu-id="6edfa-116">Este método se implementa y se accede a través del [**método Shell.ShutdownWindows.**](shell-shutdownwindows.md)</span><span class="sxs-lookup"><span data-stu-id="6edfa-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6edfa-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6edfa-117">Examples</span></span>

<span data-ttu-id="6edfa-118">En el ejemplo siguiente se muestra el uso **de ShutdownWindows** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6edfa-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6edfa-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="6edfa-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="6edfa-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="6edfa-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6edfa-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6edfa-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6edfa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6edfa-122">Requirements</span></span>



| <span data-ttu-id="6edfa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6edfa-123">Requirement</span></span> | <span data-ttu-id="6edfa-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6edfa-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6edfa-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6edfa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6edfa-126">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="6edfa-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6edfa-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6edfa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6edfa-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6edfa-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6edfa-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6edfa-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6edfa-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="6edfa-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6edfa-131">Idl</span><span class="sxs-lookup"><span data-stu-id="6edfa-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6edfa-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="6edfa-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6edfa-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6edfa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6edfa-134"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6edfa-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




