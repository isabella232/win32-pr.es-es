---
description: Obtenga información sobre el método Shell.RefreshMenu, que actualiza el contenido de la menú Inicio. Solo se usa con sistemas anteriores a Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Método Shell.RefreshMenu (Shldisp.h)
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
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404538"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="ab0ed-104">Método Shell.RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="ab0ed-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="ab0ed-105">Actualiza el contenido del **menú** Inicio.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="ab0ed-106">Solo se usa con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0ed-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab0ed-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="ab0ed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab0ed-108">Parameters</span></span>

<span data-ttu-id="ab0ed-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0ed-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab0ed-110">Remarks</span></span>

<span data-ttu-id="ab0ed-111">La funcionalidad **que proporciona RefreshMenu** se controla automáticamente en Windows XP o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="ab0ed-112">No llame a este método en ese sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="ab0ed-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ab0ed-113">Examples</span></span>

<span data-ttu-id="ab0ed-114">En el ejemplo siguiente se **muestra RefreshMenu** en uso.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="ab0ed-115">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ab0ed-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ab0ed-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ab0ed-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="ab0ed-117">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="ab0ed-117">VBScript:</span></span>


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



<span data-ttu-id="ab0ed-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ab0ed-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ab0ed-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab0ed-119">Requirements</span></span>



| <span data-ttu-id="ab0ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab0ed-120">Requirement</span></span> | <span data-ttu-id="ab0ed-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ab0ed-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0ed-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab0ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0ed-123">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="ab0ed-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab0ed-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab0ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0ed-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab0ed-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab0ed-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab0ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab0ed-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ab0ed-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ab0ed-128">Idl</span><span class="sxs-lookup"><span data-stu-id="ab0ed-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab0ed-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab0ed-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ab0ed-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab0ed-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab0ed-131"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ab0ed-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




