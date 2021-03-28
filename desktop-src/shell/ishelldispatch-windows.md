---
description: Crea y devuelve un objeto ShellWindows. Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Método IShellDispatch. Windows (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cb5f84caebf38deb27c7fb60565167793fead561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810958"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="c4691-104">Método IShellDispatch. Windows</span><span class="sxs-lookup"><span data-stu-id="c4691-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="c4691-105">Crea y devuelve un objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="c4691-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="c4691-106">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.</span><span class="sxs-lookup"><span data-stu-id="c4691-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4691-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4691-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="c4691-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4691-108">Parameters</span></span>

<span data-ttu-id="c4691-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c4691-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4691-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4691-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c4691-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c4691-111">JScript</span></span>

<span data-ttu-id="c4691-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4691-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="c4691-113">Una referencia de objeto al objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="c4691-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="c4691-114">VB</span><span class="sxs-lookup"><span data-stu-id="c4691-114">VB</span></span>

<span data-ttu-id="c4691-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="c4691-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="c4691-116">Una referencia de objeto al objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="c4691-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4691-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4691-117">Remarks</span></span>

<span data-ttu-id="c4691-118">Este método se implementa y se obtiene acceso a él a través del método [**Shell. Windows**](shell-windows.md) .</span><span class="sxs-lookup"><span data-stu-id="c4691-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="c4691-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c4691-119">Examples</span></span>

<span data-ttu-id="c4691-120">En los ejemplos siguientes se usa **Windows** para recuperar el objeto [**ShellWindows**](shellwindows.md) y mostrar un recuento del número de elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="c4691-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="c4691-121">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c4691-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c4691-122">JScript.net</span><span class="sxs-lookup"><span data-stu-id="c4691-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="c4691-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="c4691-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c4691-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c4691-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c4691-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4691-125">Requirements</span></span>



| <span data-ttu-id="c4691-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4691-126">Requirement</span></span> | <span data-ttu-id="c4691-127">Value</span><span class="sxs-lookup"><span data-stu-id="c4691-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4691-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4691-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c4691-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c4691-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c4691-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4691-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c4691-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c4691-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c4691-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4691-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4691-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4691-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c4691-134">IDL</span><span class="sxs-lookup"><span data-stu-id="c4691-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4691-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4691-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c4691-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4691-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4691-137"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c4691-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
