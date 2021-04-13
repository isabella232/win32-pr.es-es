---
description: Muestra el centro de ayuda y soporte técnico de Windows. Este método tiene el mismo efecto que hacer clic en el menú Inicio y seleccionar ayuda y soporte técnico.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Método Shell. Help (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276872"
---
# <a name="shellhelp-method"></a><span data-ttu-id="cbea3-104">Shell. Help (método)</span><span class="sxs-lookup"><span data-stu-id="cbea3-104">Shell.Help method</span></span>

<span data-ttu-id="cbea3-105">Muestra el centro de ayuda y soporte técnico de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbea3-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="cbea3-106">Este método tiene el mismo efecto que hacer clic en el menú **Inicio** y seleccionar **ayuda y soporte técnico**.</span><span class="sxs-lookup"><span data-stu-id="cbea3-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbea3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbea3-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="cbea3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbea3-108">Parameters</span></span>

<span data-ttu-id="cbea3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cbea3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cbea3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbea3-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cbea3-111">JScript</span><span class="sxs-lookup"><span data-stu-id="cbea3-111">JScript</span></span>

<span data-ttu-id="cbea3-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cbea3-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cbea3-113">VB</span><span class="sxs-lookup"><span data-stu-id="cbea3-113">VB</span></span>

<span data-ttu-id="cbea3-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cbea3-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="cbea3-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cbea3-115">Examples</span></span>

<span data-ttu-id="cbea3-116">En el ejemplo siguiente se muestra la **ayuda** en uso.</span><span class="sxs-lookup"><span data-stu-id="cbea3-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="cbea3-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cbea3-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cbea3-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="cbea3-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="cbea3-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="cbea3-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cbea3-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cbea3-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cbea3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbea3-121">Requirements</span></span>



| <span data-ttu-id="cbea3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbea3-122">Requirement</span></span> | <span data-ttu-id="cbea3-123">Value</span><span class="sxs-lookup"><span data-stu-id="cbea3-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbea3-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbea3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cbea3-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cbea3-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cbea3-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbea3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cbea3-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cbea3-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbea3-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cbea3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbea3-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbea3-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cbea3-130">IDL</span><span class="sxs-lookup"><span data-stu-id="cbea3-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbea3-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbea3-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cbea3-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbea3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbea3-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="cbea3-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




