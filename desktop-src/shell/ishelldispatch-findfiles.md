---
description: 'Muestra el cuadro de diálogo Buscar: todos los archivos. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar Buscar.'
ms.assetid: 6F588D5E-5B6E-4000-BAD5-B557FB975FCA
title: Método IShellDispatch. FindFiles (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9a9ea407d0ceccfe7706ed481aa80bcda9405ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908239"
---
# <a name="ishelldispatchfindfiles-method"></a><span data-ttu-id="b04c7-104">IShellDispatch. FindFiles, método</span><span class="sxs-lookup"><span data-stu-id="b04c7-104">IShellDispatch.FindFiles method</span></span>

<span data-ttu-id="b04c7-105">Muestra el cuadro de diálogo **Buscar: todos los archivos** .</span><span class="sxs-lookup"><span data-stu-id="b04c7-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="b04c7-106">Esto es lo mismo que hacer clic en el menú **Inicio** y seleccionar **Buscar**.</span><span class="sxs-lookup"><span data-stu-id="b04c7-106">This is the same as clicking the **Start** menu and then selecting **Search**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b04c7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b04c7-107">Syntax</span></span>


```JScript
IShellDispatch.FindFiles()
```


```VB

IShellDispatch.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="b04c7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b04c7-108">Parameters</span></span>

<span data-ttu-id="b04c7-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b04c7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b04c7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b04c7-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b04c7-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b04c7-111">JScript</span></span>

<span data-ttu-id="b04c7-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b04c7-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b04c7-113">VB</span><span class="sxs-lookup"><span data-stu-id="b04c7-113">VB</span></span>

<span data-ttu-id="b04c7-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b04c7-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b04c7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b04c7-115">Remarks</span></span>

<span data-ttu-id="b04c7-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. FindFiles**](shell-findfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="b04c7-116">This method is implemented and accessed through the [**Shell.FindFiles**](shell-findfiles.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b04c7-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b04c7-117">Examples</span></span>

<span data-ttu-id="b04c7-118">En los siguientes ejemplos se muestra el uso de **FindFiles** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b04c7-118">The following examples show the use of **FindFiles** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b04c7-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="b04c7-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindFiles();
    }
</script>
```



<span data-ttu-id="b04c7-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="b04c7-120">VBScript:</span></span>


```VB
<script language="VBScript">
   function fnShellFindFilesVB()
       dim objShell
       
       set objShell = CreateObject("shell.application")
       objshell.FindFiles

       set objShell = nothing
   end function
</script>
```



<span data-ttu-id="b04c7-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b04c7-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b04c7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b04c7-122">Requirements</span></span>



| <span data-ttu-id="b04c7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b04c7-123">Requirement</span></span> | <span data-ttu-id="b04c7-124">Value</span><span class="sxs-lookup"><span data-stu-id="b04c7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04c7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b04c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b04c7-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b04c7-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b04c7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b04c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b04c7-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b04c7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b04c7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b04c7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b04c7-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04c7-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b04c7-131">IDL</span><span class="sxs-lookup"><span data-stu-id="b04c7-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b04c7-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b04c7-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b04c7-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b04c7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b04c7-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b04c7-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




