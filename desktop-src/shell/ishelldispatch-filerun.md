---
description: Muestra el cuadro de diálogo de ejecución al usuario.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Método IShellDispatch. FileRun (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810970"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="3c738-103">IShellDispatch. FileRun, método</span><span class="sxs-lookup"><span data-stu-id="3c738-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="3c738-104">Muestra el cuadro de diálogo de **ejecución** al usuario.</span><span class="sxs-lookup"><span data-stu-id="3c738-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c738-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c738-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="3c738-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c738-106">Parameters</span></span>

<span data-ttu-id="3c738-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3c738-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c738-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c738-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3c738-109">JScript</span><span class="sxs-lookup"><span data-stu-id="3c738-109">JScript</span></span>

<span data-ttu-id="3c738-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3c738-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="3c738-111">VB</span><span class="sxs-lookup"><span data-stu-id="3c738-111">VB</span></span>

<span data-ttu-id="3c738-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3c738-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c738-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3c738-113">Remarks</span></span>

<span data-ttu-id="3c738-114">Este método se implementa y se obtiene acceso a él a través del método [**Shell. FileRun**](shell-filerun.md) .</span><span class="sxs-lookup"><span data-stu-id="3c738-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="3c738-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c738-115">Examples</span></span>

<span data-ttu-id="3c738-116">En los siguientes ejemplos se muestra el uso de **FileRun** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3c738-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3c738-117">JScript.net</span><span class="sxs-lookup"><span data-stu-id="3c738-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="3c738-118">VBScript</span><span class="sxs-lookup"><span data-stu-id="3c738-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3c738-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3c738-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3c738-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c738-120">Requirements</span></span>



| <span data-ttu-id="3c738-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c738-121">Requirement</span></span> | <span data-ttu-id="3c738-122">Value</span><span class="sxs-lookup"><span data-stu-id="3c738-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c738-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c738-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3c738-124">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3c738-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3c738-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c738-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3c738-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3c738-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3c738-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c738-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c738-128"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c738-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3c738-129">IDL</span><span class="sxs-lookup"><span data-stu-id="3c738-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c738-130"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c738-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3c738-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c738-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c738-132"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3c738-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




