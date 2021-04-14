---
description: Expulsa el equipo de la estación de acoplamiento. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar expulsar equipo si el equipo es compatible con este comando.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Método Shell. EjectPC (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 355d75b2ffaca9c9f90e66fbc535333a84bfa45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985614"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="7bbfa-104">Shell. EjectPC (método)</span><span class="sxs-lookup"><span data-stu-id="7bbfa-104">Shell.EjectPC method</span></span>

<span data-ttu-id="7bbfa-105">Expulsa el equipo de la estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="7bbfa-106">Esto es lo mismo que hacer clic en el menú **Inicio** y seleccionar **expulsar equipo** si el equipo es compatible con este comando.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbfa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bbfa-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="7bbfa-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bbfa-108">Parameters</span></span>

<span data-ttu-id="7bbfa-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bbfa-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bbfa-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7bbfa-111">JScript</span><span class="sxs-lookup"><span data-stu-id="7bbfa-111">JScript</span></span>

<span data-ttu-id="7bbfa-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7bbfa-113">VB</span><span class="sxs-lookup"><span data-stu-id="7bbfa-113">VB</span></span>

<span data-ttu-id="7bbfa-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7bbfa-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7bbfa-115">Examples</span></span>

<span data-ttu-id="7bbfa-116">En el ejemplo siguiente se muestra **EjectPC** en uso.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="7bbfa-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7bbfa-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7bbfa-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="7bbfa-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="7bbfa-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="7bbfa-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7bbfa-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7bbfa-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7bbfa-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bbfa-121">Requirements</span></span>



| <span data-ttu-id="7bbfa-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bbfa-122">Requirement</span></span> | <span data-ttu-id="7bbfa-123">Value</span><span class="sxs-lookup"><span data-stu-id="7bbfa-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbfa-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bbfa-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbfa-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7bbfa-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7bbfa-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bbfa-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbfa-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7bbfa-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7bbfa-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7bbfa-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bbfa-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfa-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7bbfa-130">IDL</span><span class="sxs-lookup"><span data-stu-id="7bbfa-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7bbfa-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfa-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7bbfa-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7bbfa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bbfa-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfa-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




