---
description: Obtiene un objeto que representa el elemento primario del objeto actual.
ms.assetid: 76c2f72c-5ef6-4f2c-bdfc-62ced6dbc504
title: Propiedad Shell. Parent (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a121e4f87be1163429156f22dfe7bd55f1345f43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985546"
---
# <a name="shellparent-property"></a><span data-ttu-id="fb2de-103">Shell. Parent (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fb2de-103">Shell.Parent property</span></span>

<span data-ttu-id="fb2de-104">Obtiene un objeto que representa el elemento primario del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="fb2de-104">Gets an object that represents the parent of the current object.</span></span>

<span data-ttu-id="fb2de-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fb2de-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2de-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb2de-106">Syntax</span></span>


```JScript
objParent = Shell.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="fb2de-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fb2de-107">Property value</span></span>

<span data-ttu-id="fb2de-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto primario.</span><span class="sxs-lookup"><span data-stu-id="fb2de-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="fb2de-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fb2de-109">Examples</span></span>

<span data-ttu-id="fb2de-110">En el ejemplo siguiente se muestra el uso correcto de los **elementos primarios** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fb2de-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fb2de-111">JScript.net</span><span class="sxs-lookup"><span data-stu-id="fb2de-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objShell.Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="fb2de-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="fb2de-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objShell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="fb2de-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fb2de-113">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objShell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fb2de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb2de-114">Requirements</span></span>



| <span data-ttu-id="fb2de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb2de-115">Requirement</span></span> | <span data-ttu-id="fb2de-116">Value</span><span class="sxs-lookup"><span data-stu-id="fb2de-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2de-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb2de-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2de-118">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fb2de-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fb2de-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb2de-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2de-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fb2de-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb2de-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb2de-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb2de-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2de-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fb2de-123">IDL</span><span class="sxs-lookup"><span data-stu-id="fb2de-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb2de-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb2de-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fb2de-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb2de-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb2de-126"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fb2de-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
