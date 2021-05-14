---
description: Crea y devuelve un nuevo objeto ShellWindows que es una copia de este objeto ShellWindows.
title: ShellWindows._NewEnum método (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: 944da80196db12d0bfa5d64767c5e6c2e8ff733e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841256"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="4c704-103">ShellWindows. \_ Método NewEnum</span><span class="sxs-lookup"><span data-stu-id="4c704-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="4c704-104">Crea y devuelve un nuevo [**objeto ShellWindows**](shellwindows.md) que es una copia de **este objeto ShellWindows.**</span><span class="sxs-lookup"><span data-stu-id="4c704-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c704-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c704-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="4c704-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c704-106">Parameters</span></span>

<span data-ttu-id="4c704-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4c704-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c704-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c704-108">Return value</span></span>

<span data-ttu-id="4c704-109">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="4c704-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="4c704-110">Referencia de objeto a la [**copia del objeto ShellWindows.**](shellwindows.md)</span><span class="sxs-lookup"><span data-stu-id="4c704-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="4c704-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c704-111">Examples</span></span>

<span data-ttu-id="4c704-112">En el ejemplo siguiente se **\_ muestra NewEnum** en uso.</span><span class="sxs-lookup"><span data-stu-id="4c704-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="4c704-113">Se muestra un uso adecuado para VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4c704-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="4c704-114">Este método no se puede usar con JScript.</span><span class="sxs-lookup"><span data-stu-id="4c704-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="4c704-115">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="4c704-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4c704-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4c704-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4c704-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c704-117">Requirements</span></span>



| <span data-ttu-id="4c704-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c704-118">Requirement</span></span> | <span data-ttu-id="4c704-119">Value</span><span class="sxs-lookup"><span data-stu-id="4c704-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c704-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c704-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c704-121">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="4c704-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4c704-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c704-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c704-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c704-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4c704-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c704-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c704-125"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="4c704-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="4c704-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c704-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c704-127"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4c704-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
