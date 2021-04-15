---
description: Contiene el número de elementos de la colección.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: ShellWindows. Count (propiedad) (exdisp. h)
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
ms.openlocfilehash: a8d5b9e605650ba7d3cb6036e8abfac58c0b8597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986018"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="e9863-103">ShellWindows. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e9863-103">ShellWindows.Count property</span></span>

<span data-ttu-id="e9863-104">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="e9863-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="e9863-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e9863-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9863-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9863-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="e9863-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e9863-107">Property value</span></span>

<span data-ttu-id="e9863-108">Un **entero** que contiene un valor para la propiedad **Count** .</span><span class="sxs-lookup"><span data-stu-id="e9863-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="e9863-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e9863-109">Examples</span></span>

<span data-ttu-id="e9863-110">En el ejemplo siguiente se muestra el **recuento** en uso.</span><span class="sxs-lookup"><span data-stu-id="e9863-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="e9863-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e9863-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e9863-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="e9863-112">JScript:</span></span>


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



<span data-ttu-id="e9863-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="e9863-113">VBScript:</span></span>


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



<span data-ttu-id="e9863-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e9863-114">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e9863-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9863-115">Requirements</span></span>



| <span data-ttu-id="e9863-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9863-116">Requirement</span></span> | <span data-ttu-id="e9863-117">Value</span><span class="sxs-lookup"><span data-stu-id="e9863-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9863-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9863-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e9863-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e9863-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e9863-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9863-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e9863-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e9863-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e9863-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9863-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9863-123"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9863-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="e9863-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9863-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9863-125"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e9863-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




