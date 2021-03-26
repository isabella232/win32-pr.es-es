---
description: 'Muestra el cuadro de diálogo Buscar: todos los archivos. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar Buscar (o su equivalente en sistemas anteriores a Windows XP.'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Método Shell. FindFiles (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278505"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="fdf19-104">Shell. FindFiles (método)</span><span class="sxs-lookup"><span data-stu-id="fdf19-104">Shell.FindFiles method</span></span>

<span data-ttu-id="fdf19-105">Muestra el cuadro de diálogo **Buscar: todos los archivos** .</span><span class="sxs-lookup"><span data-stu-id="fdf19-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="fdf19-106">Esto es lo mismo que hacer clic en el menú **Inicio** y seleccionar **Buscar** (o su equivalente en sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fdf19-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf19-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fdf19-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="fdf19-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fdf19-108">Parameters</span></span>

<span data-ttu-id="fdf19-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fdf19-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fdf19-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fdf19-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fdf19-111">JScript</span><span class="sxs-lookup"><span data-stu-id="fdf19-111">JScript</span></span>

<span data-ttu-id="fdf19-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fdf19-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fdf19-113">VB</span><span class="sxs-lookup"><span data-stu-id="fdf19-113">VB</span></span>

<span data-ttu-id="fdf19-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fdf19-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="fdf19-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fdf19-115">Examples</span></span>

<span data-ttu-id="fdf19-116">En el ejemplo siguiente se muestra **FindFiles** en uso.</span><span class="sxs-lookup"><span data-stu-id="fdf19-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="fdf19-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fdf19-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fdf19-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="fdf19-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="fdf19-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="fdf19-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="fdf19-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fdf19-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fdf19-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdf19-121">Requirements</span></span>



| <span data-ttu-id="fdf19-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdf19-122">Requirement</span></span> | <span data-ttu-id="fdf19-123">Value</span><span class="sxs-lookup"><span data-stu-id="fdf19-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf19-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdf19-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf19-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fdf19-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fdf19-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fdf19-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf19-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fdf19-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fdf19-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdf19-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf19-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf19-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fdf19-130">IDL</span><span class="sxs-lookup"><span data-stu-id="fdf19-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fdf19-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fdf19-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fdf19-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fdf19-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdf19-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fdf19-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




