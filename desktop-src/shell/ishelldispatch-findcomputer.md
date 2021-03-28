---
description: 'Muestra el cuadro de diálogo resultados de la búsqueda: equipos. En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Método IShellDispatch. FindComputer (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984715"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="1199d-104">IShellDispatch. FindComputer, método</span><span class="sxs-lookup"><span data-stu-id="1199d-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="1199d-105">Muestra el cuadro de diálogo resultados de la **búsqueda: equipos** .</span><span class="sxs-lookup"><span data-stu-id="1199d-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="1199d-106">En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="1199d-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1199d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1199d-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="1199d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1199d-108">Parameters</span></span>

<span data-ttu-id="1199d-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1199d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1199d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1199d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1199d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1199d-111">JScript</span></span>

<span data-ttu-id="1199d-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1199d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1199d-113">VB</span><span class="sxs-lookup"><span data-stu-id="1199d-113">VB</span></span>

<span data-ttu-id="1199d-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1199d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1199d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1199d-115">Remarks</span></span>

<span data-ttu-id="1199d-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. FindComputer**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="1199d-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1199d-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1199d-117">Examples</span></span>

<span data-ttu-id="1199d-118">En los siguientes ejemplos se muestra el uso de **FindComputer** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1199d-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1199d-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="1199d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="1199d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="1199d-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1199d-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1199d-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1199d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1199d-122">Requirements</span></span>



| <span data-ttu-id="1199d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1199d-123">Requirement</span></span> | <span data-ttu-id="1199d-124">Value</span><span class="sxs-lookup"><span data-stu-id="1199d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1199d-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1199d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1199d-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1199d-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1199d-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1199d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1199d-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1199d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1199d-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1199d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1199d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1199d-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1199d-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1199d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1199d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1199d-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1199d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1199d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1199d-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1199d-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




