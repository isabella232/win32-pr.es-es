---
description: Muestra el cuadro de diálogo fecha y hora. Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar ajustar fecha y hora.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: Método IShellDispatch. SetTime (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908237"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="f207a-104">IShellDispatch. SetTime, método</span><span class="sxs-lookup"><span data-stu-id="f207a-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="f207a-105">Muestra el cuadro de diálogo **fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="f207a-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="f207a-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar **Ajustar fecha y hora**.</span><span class="sxs-lookup"><span data-stu-id="f207a-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f207a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f207a-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="f207a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f207a-108">Parameters</span></span>

<span data-ttu-id="f207a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f207a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f207a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f207a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f207a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f207a-111">JScript</span></span>

<span data-ttu-id="f207a-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f207a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f207a-113">VB</span><span class="sxs-lookup"><span data-stu-id="f207a-113">VB</span></span>

<span data-ttu-id="f207a-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f207a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f207a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f207a-115">Remarks</span></span>

<span data-ttu-id="f207a-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. setTime**](shell-settime.md) .</span><span class="sxs-lookup"><span data-stu-id="f207a-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f207a-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f207a-117">Examples</span></span>

<span data-ttu-id="f207a-118">En los siguientes ejemplos se muestra el uso de **setTime** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f207a-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f207a-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="f207a-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="f207a-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="f207a-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="f207a-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f207a-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="f207a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f207a-122">Requirements</span></span>



| <span data-ttu-id="f207a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f207a-123">Requirement</span></span> | <span data-ttu-id="f207a-124">Value</span><span class="sxs-lookup"><span data-stu-id="f207a-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f207a-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f207a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f207a-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f207a-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f207a-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f207a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f207a-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f207a-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f207a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f207a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f207a-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f207a-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f207a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="f207a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f207a-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f207a-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f207a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f207a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f207a-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f207a-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




