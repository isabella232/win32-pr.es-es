---
description: 'Muestra el cuadro de diálogo resultados de la búsqueda: equipos. En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Método Shell. FindComputer (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985982"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="ec863-104">Shell. FindComputer (método)</span><span class="sxs-lookup"><span data-stu-id="ec863-104">Shell.FindComputer method</span></span>

<span data-ttu-id="ec863-105">Muestra el cuadro de diálogo resultados de la **búsqueda: equipos** .</span><span class="sxs-lookup"><span data-stu-id="ec863-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="ec863-106">En el cuadro de diálogo se muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="ec863-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec863-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec863-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="ec863-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec863-108">Parameters</span></span>

<span data-ttu-id="ec863-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ec863-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec863-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec863-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ec863-111">JScript</span><span class="sxs-lookup"><span data-stu-id="ec863-111">JScript</span></span>

<span data-ttu-id="ec863-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec863-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="ec863-113">VB</span><span class="sxs-lookup"><span data-stu-id="ec863-113">VB</span></span>

<span data-ttu-id="ec863-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ec863-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="ec863-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ec863-115">Examples</span></span>

<span data-ttu-id="ec863-116">En el ejemplo siguiente se muestra **FindComputer** en uso.</span><span class="sxs-lookup"><span data-stu-id="ec863-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="ec863-117">El resultado de este código es el mismo que cuando se presiona el botón **Inicio** , se hace clic en **Buscar**, se hace clic en la opción **impresoras, equipos o personas** y, a continuación, se hace clic **en un equipo de la red**.</span><span class="sxs-lookup"><span data-stu-id="ec863-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="ec863-118">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ec863-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ec863-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="ec863-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="ec863-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="ec863-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ec863-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ec863-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ec863-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec863-122">Requirements</span></span>



| <span data-ttu-id="ec863-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec863-123">Requirement</span></span> | <span data-ttu-id="ec863-124">Value</span><span class="sxs-lookup"><span data-stu-id="ec863-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec863-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec863-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ec863-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ec863-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ec863-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec863-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ec863-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ec863-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec863-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec863-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec863-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec863-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ec863-131">IDL</span><span class="sxs-lookup"><span data-stu-id="ec863-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec863-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec863-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ec863-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec863-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec863-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ec863-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




