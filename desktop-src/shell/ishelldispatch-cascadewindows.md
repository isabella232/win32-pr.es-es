---
description: Organiza en cascada todas las ventanas del escritorio. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar ventanas en cascada.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Método IShellDispatch. CascadeWindows (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154945"
---
# <a name="ishelldispatchcascadewindows-method"></a><span data-ttu-id="3d2e7-104">IShellDispatch. CascadeWindows, método</span><span class="sxs-lookup"><span data-stu-id="3d2e7-104">IShellDispatch.CascadeWindows method</span></span>

<span data-ttu-id="3d2e7-105">Organiza en cascada todas las ventanas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="3d2e7-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="3d2e7-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **ventanas en cascada**.</span><span class="sxs-lookup"><span data-stu-id="3d2e7-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2e7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d2e7-107">Syntax</span></span>


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="3d2e7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d2e7-108">Parameters</span></span>

<span data-ttu-id="3d2e7-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3d2e7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d2e7-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d2e7-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3d2e7-111">JScript</span><span class="sxs-lookup"><span data-stu-id="3d2e7-111">JScript</span></span>

<span data-ttu-id="3d2e7-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d2e7-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="3d2e7-113">VB</span><span class="sxs-lookup"><span data-stu-id="3d2e7-113">VB</span></span>

<span data-ttu-id="3d2e7-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d2e7-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2e7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d2e7-115">Remarks</span></span>

<span data-ttu-id="3d2e7-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. CascadeWindows**](shell-cascadewindows.md) .</span><span class="sxs-lookup"><span data-stu-id="3d2e7-116">This method is implemented and accessed through the [**Shell.CascadeWindows**](shell-cascadewindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="3d2e7-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3d2e7-117">Examples</span></span>

<span data-ttu-id="3d2e7-118">En los siguientes ejemplos se muestra el uso de **CascadeWindows** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3d2e7-118">The following examples show the use of **CascadeWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3d2e7-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="3d2e7-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="3d2e7-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="3d2e7-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3d2e7-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3d2e7-121">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3d2e7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d2e7-122">Requirements</span></span>



| <span data-ttu-id="3d2e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d2e7-123">Requirement</span></span> | <span data-ttu-id="3d2e7-124">Value</span><span class="sxs-lookup"><span data-stu-id="3d2e7-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2e7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d2e7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2e7-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3d2e7-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d2e7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d2e7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2e7-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d2e7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3d2e7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d2e7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d2e7-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d2e7-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3d2e7-131">IDL</span><span class="sxs-lookup"><span data-stu-id="3d2e7-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d2e7-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d2e7-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3d2e7-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d2e7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d2e7-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="3d2e7-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




