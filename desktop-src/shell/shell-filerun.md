---
description: Muestra el cuadro de diálogo de ejecución al usuario. Este método tiene el mismo efecto que hacer clic en el menú Inicio y seleccionar ejecutar.
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: Método Shell. FileRun (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985987"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="f3f10-104">Shell. FileRun (método)</span><span class="sxs-lookup"><span data-stu-id="f3f10-104">Shell.FileRun method</span></span>

<span data-ttu-id="f3f10-105">Muestra el cuadro de diálogo de **ejecución** al usuario.</span><span class="sxs-lookup"><span data-stu-id="f3f10-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="f3f10-106">Este método tiene el mismo efecto que hacer clic en el menú **Inicio** y seleccionar **Ejecutar**.</span><span class="sxs-lookup"><span data-stu-id="f3f10-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f10-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3f10-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="f3f10-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3f10-108">Parameters</span></span>

<span data-ttu-id="f3f10-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f3f10-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3f10-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3f10-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f3f10-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f3f10-111">JScript</span></span>

<span data-ttu-id="f3f10-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f3f10-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f3f10-113">VB</span><span class="sxs-lookup"><span data-stu-id="f3f10-113">VB</span></span>

<span data-ttu-id="f3f10-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f3f10-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="f3f10-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f3f10-115">Examples</span></span>

<span data-ttu-id="f3f10-116">En el ejemplo siguiente se muestra **FileRun** en uso.</span><span class="sxs-lookup"><span data-stu-id="f3f10-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="f3f10-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f3f10-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f3f10-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="f3f10-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="f3f10-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="f3f10-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f3f10-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f3f10-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f3f10-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3f10-121">Requirements</span></span>



| <span data-ttu-id="f3f10-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f10-122">Requirement</span></span> | <span data-ttu-id="f3f10-123">Value</span><span class="sxs-lookup"><span data-stu-id="f3f10-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f10-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3f10-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f10-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f3f10-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3f10-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f3f10-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f10-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f3f10-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f3f10-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3f10-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f10-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f10-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f3f10-130">IDL</span><span class="sxs-lookup"><span data-stu-id="f3f10-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3f10-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3f10-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f3f10-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f3f10-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f10-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f3f10-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




