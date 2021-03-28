---
description: Expulsa el equipo de la estación de acoplamiento. Esto es lo mismo que hacer clic en el menú Inicio y seleccionar expulsar equipo si el equipo es compatible con este comando.
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Método IShellDispatch. EjectPC (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d85dd8c007338dca3d68183bc9ba3fbd333195ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275680"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="8bf03-104">IShellDispatch. EjectPC, método</span><span class="sxs-lookup"><span data-stu-id="8bf03-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="8bf03-105">Expulsa el equipo de la estación de acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="8bf03-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="8bf03-106">Esto es lo mismo que hacer clic en el menú **Inicio** y seleccionar **expulsar equipo** si el equipo es compatible con este comando.</span><span class="sxs-lookup"><span data-stu-id="8bf03-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf03-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bf03-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="8bf03-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bf03-108">Parameters</span></span>

<span data-ttu-id="8bf03-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8bf03-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8bf03-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bf03-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8bf03-111">JScript</span><span class="sxs-lookup"><span data-stu-id="8bf03-111">JScript</span></span>

<span data-ttu-id="8bf03-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8bf03-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="8bf03-113">VB</span><span class="sxs-lookup"><span data-stu-id="8bf03-113">VB</span></span>

<span data-ttu-id="8bf03-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8bf03-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bf03-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bf03-115">Remarks</span></span>

<span data-ttu-id="8bf03-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf03-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="8bf03-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8bf03-117">Examples</span></span>

<span data-ttu-id="8bf03-118">En los siguientes ejemplos se muestra el uso de **EjectPC** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8bf03-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8bf03-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="8bf03-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="8bf03-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="8bf03-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8bf03-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8bf03-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8bf03-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf03-122">Requirements</span></span>



| <span data-ttu-id="8bf03-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf03-123">Requirement</span></span> | <span data-ttu-id="8bf03-124">Value</span><span class="sxs-lookup"><span data-stu-id="8bf03-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf03-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bf03-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf03-126">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8bf03-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8bf03-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bf03-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf03-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8bf03-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8bf03-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bf03-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf03-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8bf03-131">IDL</span><span class="sxs-lookup"><span data-stu-id="8bf03-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bf03-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8bf03-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bf03-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf03-134"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf03-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




