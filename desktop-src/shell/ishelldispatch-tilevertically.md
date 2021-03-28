---
description: Organiza en mosaico todas las ventanas del escritorio verticalmente. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar mostrar ventanas en paralelo.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Método IShellDispatch. TileVertically (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984699"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="50020-104">IShellDispatch. TileVertically, método</span><span class="sxs-lookup"><span data-stu-id="50020-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="50020-105">Organiza en mosaico todas las ventanas del escritorio verticalmente.</span><span class="sxs-lookup"><span data-stu-id="50020-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="50020-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Mostrar ventanas en paralelo**.</span><span class="sxs-lookup"><span data-stu-id="50020-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="50020-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50020-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="50020-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50020-108">Parameters</span></span>

<span data-ttu-id="50020-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="50020-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50020-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50020-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="50020-111">JScript</span><span class="sxs-lookup"><span data-stu-id="50020-111">JScript</span></span>

<span data-ttu-id="50020-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="50020-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="50020-113">VB</span><span class="sxs-lookup"><span data-stu-id="50020-113">VB</span></span>

<span data-ttu-id="50020-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="50020-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50020-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50020-115">Remarks</span></span>

<span data-ttu-id="50020-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. TileVertically**](shell-tilevertically.md) .</span><span class="sxs-lookup"><span data-stu-id="50020-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="50020-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50020-117">Examples</span></span>

<span data-ttu-id="50020-118">En los siguientes ejemplos se muestra el uso de **TileVertically** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="50020-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="50020-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="50020-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="50020-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="50020-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="50020-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="50020-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="50020-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50020-122">Requirements</span></span>



| <span data-ttu-id="50020-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="50020-123">Requirement</span></span> | <span data-ttu-id="50020-124">Value</span><span class="sxs-lookup"><span data-stu-id="50020-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50020-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50020-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50020-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="50020-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="50020-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50020-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50020-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="50020-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50020-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50020-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="50020-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50020-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="50020-131">IDL</span><span class="sxs-lookup"><span data-stu-id="50020-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50020-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50020-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="50020-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50020-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50020-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="50020-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




