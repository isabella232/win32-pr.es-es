---
description: Actualiza el contenido del menú Inicio. Solo se usa con sistemas anteriores a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Método Shell. RefreshMenu (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985543"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="f10d6-104">Shell. RefreshMenu (método)</span><span class="sxs-lookup"><span data-stu-id="f10d6-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="f10d6-105">Actualiza el contenido del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="f10d6-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="f10d6-106">Solo se usa con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f10d6-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="f10d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f10d6-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="f10d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f10d6-108">Parameters</span></span>

<span data-ttu-id="f10d6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f10d6-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f10d6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f10d6-110">Remarks</span></span>

<span data-ttu-id="f10d6-111">La funcionalidad que proporciona **RefreshMenu** se administra automáticamente en Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="f10d6-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="f10d6-112">No llame a este método en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f10d6-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="f10d6-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f10d6-113">Examples</span></span>

<span data-ttu-id="f10d6-114">En el ejemplo siguiente se muestra **RefreshMenu** en uso.</span><span class="sxs-lookup"><span data-stu-id="f10d6-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="f10d6-115">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f10d6-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f10d6-116">JScript.net</span><span class="sxs-lookup"><span data-stu-id="f10d6-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="f10d6-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="f10d6-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f10d6-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f10d6-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f10d6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f10d6-119">Requirements</span></span>



| <span data-ttu-id="f10d6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f10d6-120">Requirement</span></span> | <span data-ttu-id="f10d6-121">Value</span><span class="sxs-lookup"><span data-stu-id="f10d6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f10d6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f10d6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f10d6-123">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f10d6-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f10d6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f10d6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f10d6-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f10d6-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f10d6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f10d6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f10d6-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f10d6-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f10d6-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f10d6-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f10d6-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f10d6-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f10d6-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f10d6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f10d6-131"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f10d6-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




