---
description: Organiza en mosaico todas las ventanas del escritorio de forma horizontal. Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar mostrar ventanas apiladas.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Método IShellDispatch. TileHorizontally (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154937"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="61a04-104">IShellDispatch. TileHorizontally, método</span><span class="sxs-lookup"><span data-stu-id="61a04-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="61a04-105">Organiza en mosaico todas las ventanas del escritorio de forma horizontal.</span><span class="sxs-lookup"><span data-stu-id="61a04-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="61a04-106">Este método tiene el mismo efecto que hacer clic con el botón derecho en la barra de tareas y seleccionar **Mostrar ventanas apiladas**.</span><span class="sxs-lookup"><span data-stu-id="61a04-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61a04-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="61a04-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="61a04-108">Parameters</span></span>

<span data-ttu-id="61a04-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="61a04-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="61a04-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61a04-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="61a04-111">JScript</span><span class="sxs-lookup"><span data-stu-id="61a04-111">JScript</span></span>

<span data-ttu-id="61a04-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="61a04-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="61a04-113">VB</span><span class="sxs-lookup"><span data-stu-id="61a04-113">VB</span></span>

<span data-ttu-id="61a04-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="61a04-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a04-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61a04-115">Remarks</span></span>

<span data-ttu-id="61a04-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. TileHorizontally**](shell-tilehorizontally.md) .</span><span class="sxs-lookup"><span data-stu-id="61a04-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="61a04-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61a04-117">Examples</span></span>

<span data-ttu-id="61a04-118">En el ejemplo siguiente se muestra el uso de **TileHorizontally** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="61a04-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="61a04-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="61a04-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="61a04-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="61a04-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="61a04-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="61a04-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="61a04-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61a04-122">Requirements</span></span>



| <span data-ttu-id="61a04-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a04-123">Requirement</span></span> | <span data-ttu-id="61a04-124">Value</span><span class="sxs-lookup"><span data-stu-id="61a04-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a04-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61a04-125">Minimum supported client</span></span><br/> | <span data-ttu-id="61a04-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="61a04-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="61a04-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61a04-127">Minimum supported server</span></span><br/> | <span data-ttu-id="61a04-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="61a04-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="61a04-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61a04-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a04-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="61a04-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="61a04-131">IDL</span><span class="sxs-lookup"><span data-stu-id="61a04-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61a04-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61a04-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="61a04-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="61a04-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a04-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="61a04-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




