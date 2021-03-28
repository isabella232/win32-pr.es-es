---
description: Recupera un objeto que representa el elemento primario del objeto actual.
ms.assetid: 2FDEF8D3-3F5B-43ae-9812-83B4249D9CBB
title: Propiedad IShellDispatch. Parent (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 051e6f323b9663b692410d81d85e55a404e99d56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154940"
---
# <a name="ishelldispatchparent-property"></a><span data-ttu-id="56307-103">IShellDispatch. Parent (propiedad)</span><span class="sxs-lookup"><span data-stu-id="56307-103">IShellDispatch.Parent property</span></span>

<span data-ttu-id="56307-104">Recupera un objeto que representa el elemento primario del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="56307-104">Retrieves an object that represents the parent of the current object.</span></span>

<span data-ttu-id="56307-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="56307-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56307-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56307-106">Syntax</span></span>


```JScript
objParent = IShellDispatch.Parent
```


```VB

Property Parent As Object
```





## <a name="property-value"></a><span data-ttu-id="56307-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56307-107">Property value</span></span>

<span data-ttu-id="56307-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto primario.</span><span class="sxs-lookup"><span data-stu-id="56307-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="remarks"></a><span data-ttu-id="56307-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56307-109">Remarks</span></span>

<span data-ttu-id="56307-110">Esta propiedad se implementa y se obtiene acceso a ella a través de la propiedad [**Shell. Parent**](shell-parent.md) .</span><span class="sxs-lookup"><span data-stu-id="56307-110">This property is implemented and accessed through the [**Shell.Parent**](shell-parent.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="56307-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56307-111">Examples</span></span>

<span data-ttu-id="56307-112">En los siguientes ejemplos se muestra el uso de los **elementos primarios** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="56307-112">The following examples show the use of **Parent** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="56307-113">JScript.net</span><span class="sxs-lookup"><span data-stu-id="56307-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellParentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objParent;

        objParent = objshell.Shell_Parent;
        if (objParent != null)
        {
            alert("Got parent property");
        }
    }
</script>
```



<span data-ttu-id="56307-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="56307-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellParentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            if (not objShell is nothing) then
                dim objParent

                set objParent = objshell.Parent
                    if (not objParent is nothing) then
                        alert("Got parent property")
                    end if
                set objParent = nothing
            end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="56307-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="56307-115">Visual Basic:</span></span>


```VB
Private Sub fnShellParentVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        If (Not objShell Is Nothing) Then
            Dim objParent As Object
            
            Set objParent = objshell.Parent
                If (Not objParent Is Nothing) Then
                    Debug.Print "Got parent object"
                End If
            Set objParent = Nothing
        End If
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="56307-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56307-116">Requirements</span></span>



| <span data-ttu-id="56307-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="56307-117">Requirement</span></span> | <span data-ttu-id="56307-118">Value</span><span class="sxs-lookup"><span data-stu-id="56307-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56307-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56307-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56307-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="56307-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="56307-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56307-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56307-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56307-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56307-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56307-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56307-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56307-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="56307-125">IDL</span><span class="sxs-lookup"><span data-stu-id="56307-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56307-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56307-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="56307-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56307-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56307-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="56307-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
