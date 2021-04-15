---
description: Organiza en mosaico todas las ventanas del escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar ventanas de mosaico verticalmente.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Método Shell. TileVertically (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985963"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="4026c-104">Shell. TileVertically (método)</span><span class="sxs-lookup"><span data-stu-id="4026c-104">Shell.TileVertically method</span></span>

<span data-ttu-id="4026c-105">Organiza en mosaico todas las ventanas del escritorio verticalmente.</span><span class="sxs-lookup"><span data-stu-id="4026c-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="4026c-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **ventanas de mosaico verticalmente**.</span><span class="sxs-lookup"><span data-stu-id="4026c-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4026c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4026c-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="4026c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4026c-108">Parameters</span></span>

<span data-ttu-id="4026c-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4026c-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="4026c-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4026c-110">Examples</span></span>

<span data-ttu-id="4026c-111">En el ejemplo siguiente se muestra **TileVertically** en uso.</span><span class="sxs-lookup"><span data-stu-id="4026c-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="4026c-112">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4026c-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4026c-113">JScript.net</span><span class="sxs-lookup"><span data-stu-id="4026c-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="4026c-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="4026c-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4026c-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4026c-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4026c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4026c-116">Requirements</span></span>



| <span data-ttu-id="4026c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4026c-117">Requirement</span></span> | <span data-ttu-id="4026c-118">Value</span><span class="sxs-lookup"><span data-stu-id="4026c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4026c-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4026c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4026c-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4026c-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4026c-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4026c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4026c-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4026c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4026c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4026c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4026c-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4026c-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4026c-125">IDL</span><span class="sxs-lookup"><span data-stu-id="4026c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4026c-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4026c-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4026c-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4026c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4026c-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4026c-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




