---
description: 'Método Shell.Windows: crea y devuelve un objeto ShellWindows. Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.'
title: Método Shell.Windows (Shldisp.h)
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
ms.openlocfilehash: bbe8ed55865322fc7436959fd80b478baa3c0b40
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842616"
---
# <a name="shellwindows-method"></a><span data-ttu-id="b8ca6-104">Método Shell.Windows</span><span class="sxs-lookup"><span data-stu-id="b8ca6-104">Shell.Windows method</span></span>

<span data-ttu-id="b8ca6-105">Crea y devuelve un [**objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="b8ca6-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="b8ca6-106">Este objeto representa una colección de todas las ventanas abiertas que pertenecen al Shell.</span><span class="sxs-lookup"><span data-stu-id="b8ca6-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ca6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8ca6-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="b8ca6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8ca6-108">Parameters</span></span>

<span data-ttu-id="b8ca6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b8ca6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8ca6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8ca6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b8ca6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b8ca6-111">JScript</span></span>

<span data-ttu-id="b8ca6-112">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8ca6-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="b8ca6-113">Referencia de objeto al [**objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="b8ca6-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="b8ca6-114">VB</span><span class="sxs-lookup"><span data-stu-id="b8ca6-114">VB</span></span>

<span data-ttu-id="b8ca6-115">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8ca6-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="b8ca6-116">Referencia de objeto al [**objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="b8ca6-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="b8ca6-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8ca6-117">Examples</span></span>

<span data-ttu-id="b8ca6-118">En el ejemplo siguiente se **usa Windows** para recuperar el objeto [**ShellWindows**](shellwindows.md) y mostrar un recuento del número de elementos que contiene.</span><span class="sxs-lookup"><span data-stu-id="b8ca6-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="b8ca6-119">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b8ca6-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b8ca6-120">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b8ca6-120">JScript:</span></span>


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



<span data-ttu-id="b8ca6-121">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b8ca6-121">VBScript:</span></span>


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



<span data-ttu-id="b8ca6-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b8ca6-122">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b8ca6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8ca6-123">Requirements</span></span>



| <span data-ttu-id="b8ca6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ca6-124">Requirement</span></span> | <span data-ttu-id="b8ca6-125">Value</span><span class="sxs-lookup"><span data-stu-id="b8ca6-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ca6-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ca6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ca6-127">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="b8ca6-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b8ca6-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8ca6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ca6-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8ca6-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8ca6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8ca6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ca6-131"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ca6-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b8ca6-132">Idl</span><span class="sxs-lookup"><span data-stu-id="b8ca6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8ca6-133"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8ca6-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b8ca6-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8ca6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8ca6-135"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ca6-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
