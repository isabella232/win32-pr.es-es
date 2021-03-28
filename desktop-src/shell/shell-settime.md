---
description: Muestra el cuadro de diálogo Propiedades de fecha y hora. Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar ajustar fecha y hora.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Método Shell. SetTime (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985542"
---
# <a name="shellsettime-method"></a><span data-ttu-id="ee4a2-104">Shell. SetTime (método)</span><span class="sxs-lookup"><span data-stu-id="ee4a2-104">Shell.SetTime method</span></span>

<span data-ttu-id="ee4a2-105">Muestra el cuadro de diálogo **propiedades de fecha y hora** .</span><span class="sxs-lookup"><span data-stu-id="ee4a2-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="ee4a2-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en el reloj en el área de estado de la barra de tareas y seleccionar **Ajustar fecha y hora**.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee4a2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee4a2-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="ee4a2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee4a2-108">Parameters</span></span>

<span data-ttu-id="ee4a2-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="ee4a2-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ee4a2-110">Examples</span></span>

<span data-ttu-id="ee4a2-111">En el ejemplo siguiente se muestra **setTime** en uso.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="ee4a2-112">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ee4a2-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ee4a2-113">JScript.net</span><span class="sxs-lookup"><span data-stu-id="ee4a2-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="ee4a2-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="ee4a2-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ee4a2-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ee4a2-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ee4a2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee4a2-116">Requirements</span></span>



| <span data-ttu-id="ee4a2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee4a2-117">Requirement</span></span> | <span data-ttu-id="ee4a2-118">Value</span><span class="sxs-lookup"><span data-stu-id="ee4a2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee4a2-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee4a2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4a2-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ee4a2-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ee4a2-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee4a2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4a2-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ee4a2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ee4a2-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee4a2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee4a2-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee4a2-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ee4a2-125">IDL</span><span class="sxs-lookup"><span data-stu-id="ee4a2-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee4a2-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee4a2-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ee4a2-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee4a2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee4a2-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ee4a2-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




