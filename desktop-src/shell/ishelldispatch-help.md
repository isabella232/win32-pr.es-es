---
description: Muestra la ventana de ayuda y soporte técnico de Windows. Este método tiene el mismo efecto que hacer clic en el menú Inicio y seleccionar ayuda y soporte técnico.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Método IShellDispatch. Help (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984710"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="b94d9-104">IShellDispatch. Help (método)</span><span class="sxs-lookup"><span data-stu-id="b94d9-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="b94d9-105">Muestra la ventana de ayuda y soporte técnico de Windows.</span><span class="sxs-lookup"><span data-stu-id="b94d9-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="b94d9-106">Este método tiene el mismo efecto que hacer clic en el menú **Inicio** y seleccionar **ayuda y soporte técnico**.</span><span class="sxs-lookup"><span data-stu-id="b94d9-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b94d9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b94d9-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="b94d9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b94d9-108">Parameters</span></span>

<span data-ttu-id="b94d9-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b94d9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b94d9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b94d9-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b94d9-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b94d9-111">JScript</span></span>

<span data-ttu-id="b94d9-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b94d9-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b94d9-113">VB</span><span class="sxs-lookup"><span data-stu-id="b94d9-113">VB</span></span>

<span data-ttu-id="b94d9-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b94d9-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b94d9-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b94d9-115">Remarks</span></span>

<span data-ttu-id="b94d9-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. Help**](shell-help.md) .</span><span class="sxs-lookup"><span data-stu-id="b94d9-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b94d9-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b94d9-117">Examples</span></span>

<span data-ttu-id="b94d9-118">En los siguientes ejemplos se muestra el uso de la **ayuda** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b94d9-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b94d9-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="b94d9-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="b94d9-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="b94d9-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b94d9-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b94d9-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b94d9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b94d9-122">Requirements</span></span>



| <span data-ttu-id="b94d9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b94d9-123">Requirement</span></span> | <span data-ttu-id="b94d9-124">Value</span><span class="sxs-lookup"><span data-stu-id="b94d9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b94d9-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b94d9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b94d9-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b94d9-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b94d9-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b94d9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b94d9-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b94d9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b94d9-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b94d9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b94d9-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b94d9-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b94d9-131">IDL</span><span class="sxs-lookup"><span data-stu-id="b94d9-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b94d9-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b94d9-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b94d9-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b94d9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b94d9-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b94d9-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




