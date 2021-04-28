---
description: 'Método IShellDispatch.Windows: crea y devuelve un objeto ShellWindows. Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.'
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Método IShellDispatch.Windows (Shldisp.h)
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
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117173"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="400d6-104">Método IShellDispatch.Windows</span><span class="sxs-lookup"><span data-stu-id="400d6-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="400d6-105">Crea y devuelve un [**objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="400d6-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="400d6-106">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.</span><span class="sxs-lookup"><span data-stu-id="400d6-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="400d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="400d6-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="400d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="400d6-108">Parameters</span></span>

<span data-ttu-id="400d6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="400d6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="400d6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="400d6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="400d6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="400d6-111">JScript</span></span>

<span data-ttu-id="400d6-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="400d6-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="400d6-113">Referencia de objeto al [**objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="400d6-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="400d6-114">VB</span><span class="sxs-lookup"><span data-stu-id="400d6-114">VB</span></span>

<span data-ttu-id="400d6-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="400d6-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="400d6-116">Referencia de objeto al [**objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="400d6-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="400d6-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="400d6-117">Remarks</span></span>

<span data-ttu-id="400d6-118">Este método se implementa y se accede a través del [**método Shell.Windows.**](shell-windows.md)</span><span class="sxs-lookup"><span data-stu-id="400d6-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="400d6-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="400d6-119">Examples</span></span>

<span data-ttu-id="400d6-120">En los ejemplos siguientes se **usa Windows** para recuperar el objeto [**ShellWindows**](shellwindows.md) y mostrar un recuento del número de elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="400d6-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="400d6-121">El uso se muestra para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="400d6-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="400d6-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="400d6-122">JScript:</span></span>


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



<span data-ttu-id="400d6-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="400d6-123">VBScript:</span></span>


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



<span data-ttu-id="400d6-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="400d6-124">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="400d6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="400d6-125">Requirements</span></span>



| <span data-ttu-id="400d6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="400d6-126">Requirement</span></span> | <span data-ttu-id="400d6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="400d6-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="400d6-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="400d6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="400d6-129">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="400d6-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="400d6-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="400d6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="400d6-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="400d6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="400d6-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="400d6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="400d6-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="400d6-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="400d6-134">Idl</span><span class="sxs-lookup"><span data-stu-id="400d6-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="400d6-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="400d6-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="400d6-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="400d6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="400d6-137"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="400d6-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
