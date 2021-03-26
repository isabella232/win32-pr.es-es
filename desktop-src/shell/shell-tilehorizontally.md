---
description: Organiza en mosaico todas las ventanas del escritorio de forma horizontal. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar mosaico de ventanas horizontalmente.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Método Shell. TileHorizontally (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277402"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="d229b-104">Shell. TileHorizontally (método)</span><span class="sxs-lookup"><span data-stu-id="d229b-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="d229b-105">Organiza en mosaico todas las ventanas del escritorio de forma horizontal.</span><span class="sxs-lookup"><span data-stu-id="d229b-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="d229b-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **mosaico de ventanas horizontalmente**.</span><span class="sxs-lookup"><span data-stu-id="d229b-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d229b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d229b-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="d229b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d229b-108">Parameters</span></span>

<span data-ttu-id="d229b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d229b-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="d229b-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d229b-110">Examples</span></span>

<span data-ttu-id="d229b-111">En el ejemplo siguiente se muestra **TileHorizontally** en uso.</span><span class="sxs-lookup"><span data-stu-id="d229b-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="d229b-112">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d229b-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d229b-113">JScript.net</span><span class="sxs-lookup"><span data-stu-id="d229b-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="d229b-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="d229b-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d229b-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d229b-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d229b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d229b-116">Requirements</span></span>



| <span data-ttu-id="d229b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d229b-117">Requirement</span></span> | <span data-ttu-id="d229b-118">Value</span><span class="sxs-lookup"><span data-stu-id="d229b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d229b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d229b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d229b-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d229b-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d229b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d229b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d229b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d229b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d229b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d229b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d229b-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d229b-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d229b-125">IDL</span><span class="sxs-lookup"><span data-stu-id="d229b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d229b-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d229b-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d229b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d229b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d229b-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d229b-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




