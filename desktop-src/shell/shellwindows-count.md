---
description: 'Propiedad ShellWindows.Count: contiene el número de elementos de la colección.'
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Propiedad ShellWindows.Count (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b2b33dc11e6bf909043ac5391965e1ebd225d376
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103943"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="ceed9-103">Propiedad ShellWindows.Count</span><span class="sxs-lookup"><span data-stu-id="ceed9-103">ShellWindows.Count property</span></span>

<span data-ttu-id="ceed9-104">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="ceed9-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="ceed9-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceed9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceed9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ceed9-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="ceed9-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ceed9-107">Property value</span></span>

<span data-ttu-id="ceed9-108">Entero **que** contiene un valor para la **propiedad Count.**</span><span class="sxs-lookup"><span data-stu-id="ceed9-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="ceed9-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ceed9-109">Examples</span></span>

<span data-ttu-id="ceed9-110">En el ejemplo siguiente se **muestra Count** en uso.</span><span class="sxs-lookup"><span data-stu-id="ceed9-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="ceed9-111">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ceed9-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ceed9-112">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ceed9-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="ceed9-113">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="ceed9-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ceed9-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ceed9-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ceed9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceed9-115">Requirements</span></span>



| <span data-ttu-id="ceed9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceed9-116">Requirement</span></span> | <span data-ttu-id="ceed9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ceed9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceed9-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ceed9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ceed9-119">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="ceed9-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ceed9-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ceed9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ceed9-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ceed9-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ceed9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ceed9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceed9-123"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ceed9-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="ceed9-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ceed9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ceed9-125"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ceed9-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




