---
description: 'Método Shell.ToggleDesktop: muestra u oculta el escritorio.'
title: Método Shell.ToggleDesktop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: c0d6c1e03db960c6abc8abc28ba8e79755fce639
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083683"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="9f110-103">Método Shell.ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="9f110-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="9f110-104">Muestra u oculta el escritorio.</span><span class="sxs-lookup"><span data-stu-id="9f110-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f110-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f110-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="9f110-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f110-106">Parameters</span></span>

<span data-ttu-id="9f110-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9f110-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f110-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f110-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9f110-109">JScript</span><span class="sxs-lookup"><span data-stu-id="9f110-109">JScript</span></span>

<span data-ttu-id="9f110-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9f110-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9f110-111">VB</span><span class="sxs-lookup"><span data-stu-id="9f110-111">VB</span></span>

<span data-ttu-id="9f110-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9f110-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f110-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9f110-113">Remarks</span></span>

<span data-ttu-id="9f110-114">Este método tiene el mismo efecto que el botón **Mostrar** escritorio de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="9f110-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="9f110-115">Oculta todas las ventanas abiertas para mostrar el escritorio o oculta el escritorio mostrando todas las ventanas abiertas.</span><span class="sxs-lookup"><span data-stu-id="9f110-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="9f110-116">El **método ToggleDesktop** no muestra una interfaz de usuario, simplemente invoca la acción de alternancia.</span><span class="sxs-lookup"><span data-stu-id="9f110-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="9f110-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f110-117">Examples</span></span>

<span data-ttu-id="9f110-118">En los ejemplos siguientes se muestra el uso adecuado **de ToggleDesktop** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9f110-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9f110-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="9f110-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="9f110-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="9f110-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9f110-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9f110-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9f110-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f110-122">Requirements</span></span>



| <span data-ttu-id="9f110-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f110-123">Requirement</span></span> | <span data-ttu-id="9f110-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9f110-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f110-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f110-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9f110-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9f110-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9f110-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f110-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9f110-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f110-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9f110-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f110-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f110-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9f110-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9f110-131">Idl</span><span class="sxs-lookup"><span data-stu-id="9f110-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f110-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f110-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9f110-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f110-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f110-134"><dt>Shell32.dll (versión 6.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9f110-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




