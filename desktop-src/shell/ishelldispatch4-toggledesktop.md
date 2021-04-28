---
description: 'Método IShellDispatch4.ToggleDesktop: muestra u oculta el escritorio.'
title: Método IShellDispatch4.ToggleDesktop (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: b635408ed8a44b8bb0d27e52c167470f80f61b18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116823"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="31709-103">Método IShellDispatch4.ToggleDesktop</span><span class="sxs-lookup"><span data-stu-id="31709-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="31709-104">Muestra u oculta el escritorio.</span><span class="sxs-lookup"><span data-stu-id="31709-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="31709-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31709-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="31709-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="31709-106">Parameters</span></span>

<span data-ttu-id="31709-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="31709-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31709-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="31709-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="31709-109">JScript</span><span class="sxs-lookup"><span data-stu-id="31709-109">JScript</span></span>

<span data-ttu-id="31709-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="31709-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="31709-111">VB</span><span class="sxs-lookup"><span data-stu-id="31709-111">VB</span></span>

<span data-ttu-id="31709-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="31709-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="31709-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31709-113">Remarks</span></span>

<span data-ttu-id="31709-114">Este método tiene el mismo efecto que el botón **Mostrar** escritorio de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="31709-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="31709-115">Oculta todas las ventanas abiertas para mostrar el escritorio o oculta el escritorio mostrando todas las ventanas abiertas.</span><span class="sxs-lookup"><span data-stu-id="31709-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="31709-116">El **método ToggleDesktop** no muestra una interfaz de usuario, simplemente invoca la acción de alternancia.</span><span class="sxs-lookup"><span data-stu-id="31709-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="31709-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="31709-117">Examples</span></span>

<span data-ttu-id="31709-118">En los ejemplos siguientes se muestra el uso correcto **de ToggleDesktop** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="31709-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="31709-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="31709-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="31709-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="31709-120">VBScript:</span></span>


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



<span data-ttu-id="31709-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="31709-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="31709-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31709-122">Requirements</span></span>



| <span data-ttu-id="31709-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="31709-123">Requirement</span></span> | <span data-ttu-id="31709-124">Valor</span><span class="sxs-lookup"><span data-stu-id="31709-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31709-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31709-125">Minimum supported client</span></span><br/> | <span data-ttu-id="31709-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="31709-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="31709-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31709-127">Minimum supported server</span></span><br/> | <span data-ttu-id="31709-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="31709-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="31709-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31709-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="31709-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="31709-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="31709-131">Idl</span><span class="sxs-lookup"><span data-stu-id="31709-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31709-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="31709-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="31709-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31709-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31709-134"><dt>Shell32.dll (versión 6.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="31709-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




