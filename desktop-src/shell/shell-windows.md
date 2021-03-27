---
description: Crea y devuelve un objeto ShellWindows. Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.
title: Método Shell. Windows (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: a865109f926253215e5ad39227cfe3d480e9ccc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002800"
---
# <a name="shellwindows-method"></a><span data-ttu-id="afecc-104">Shell. Windows (método)</span><span class="sxs-lookup"><span data-stu-id="afecc-104">Shell.Windows method</span></span>

<span data-ttu-id="afecc-105">Crea y devuelve un objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="afecc-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="afecc-106">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al shell.</span><span class="sxs-lookup"><span data-stu-id="afecc-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="afecc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afecc-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="afecc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afecc-108">Parameters</span></span>

<span data-ttu-id="afecc-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="afecc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="afecc-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afecc-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="afecc-111">JScript</span><span class="sxs-lookup"><span data-stu-id="afecc-111">JScript</span></span>

<span data-ttu-id="afecc-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="afecc-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="afecc-113">Una referencia de objeto al objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="afecc-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="afecc-114">VB</span><span class="sxs-lookup"><span data-stu-id="afecc-114">VB</span></span>

<span data-ttu-id="afecc-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="afecc-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="afecc-116">Una referencia de objeto al objeto [**ShellWindows**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="afecc-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="afecc-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="afecc-117">Examples</span></span>

<span data-ttu-id="afecc-118">En el ejemplo siguiente se usa **Windows** para recuperar el objeto [**ShellWindows**](shellwindows.md) y mostrar un recuento del número de elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="afecc-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="afecc-119">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="afecc-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="afecc-120">JScript.net</span><span class="sxs-lookup"><span data-stu-id="afecc-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="afecc-121">VBScript</span><span class="sxs-lookup"><span data-stu-id="afecc-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="afecc-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="afecc-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="afecc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afecc-123">Requirements</span></span>



| <span data-ttu-id="afecc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="afecc-124">Requirement</span></span> | <span data-ttu-id="afecc-125">Value</span><span class="sxs-lookup"><span data-stu-id="afecc-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afecc-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afecc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="afecc-127">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="afecc-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="afecc-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afecc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="afecc-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="afecc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="afecc-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afecc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="afecc-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="afecc-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="afecc-132">IDL</span><span class="sxs-lookup"><span data-stu-id="afecc-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afecc-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afecc-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="afecc-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="afecc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afecc-135"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="afecc-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
