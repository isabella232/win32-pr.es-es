---
description: Actualiza el contenido del menú Inicio. Solo se usa con sistemas anteriores a Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Método IShellDispatch. RefreshMenu (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 98728ef48ffb9ef4383cf9ba567606758b7a015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984707"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="a5d75-104">IShellDispatch. RefreshMenu, método</span><span class="sxs-lookup"><span data-stu-id="a5d75-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="a5d75-105">Actualiza el contenido del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="a5d75-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="a5d75-106">Solo se usa con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5d75-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d75-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5d75-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="a5d75-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5d75-108">Parameters</span></span>

<span data-ttu-id="a5d75-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a5d75-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5d75-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5d75-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a5d75-111">JScript</span><span class="sxs-lookup"><span data-stu-id="a5d75-111">JScript</span></span>

<span data-ttu-id="a5d75-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a5d75-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a5d75-113">VB</span><span class="sxs-lookup"><span data-stu-id="a5d75-113">VB</span></span>

<span data-ttu-id="a5d75-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a5d75-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d75-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a5d75-115">Remarks</span></span>

<span data-ttu-id="a5d75-116">Este método se implementa y se obtiene acceso a él a través del método [**Shell. TrayProperties**](shell-trayproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a5d75-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="a5d75-117">La funcionalidad que proporciona **RefreshMenu** se administra automáticamente en Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="a5d75-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="a5d75-118">No llame a este método en Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="a5d75-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="a5d75-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a5d75-119">Examples</span></span>

<span data-ttu-id="a5d75-120">En los siguientes ejemplos se muestra el uso de **RefreshMenu** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a5d75-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a5d75-121">JScript.net</span><span class="sxs-lookup"><span data-stu-id="a5d75-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="a5d75-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="a5d75-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a5d75-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a5d75-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a5d75-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5d75-124">Requirements</span></span>



| <span data-ttu-id="a5d75-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d75-125">Requirement</span></span> | <span data-ttu-id="a5d75-126">Value</span><span class="sxs-lookup"><span data-stu-id="a5d75-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d75-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d75-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d75-128">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a5d75-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a5d75-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5d75-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d75-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a5d75-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a5d75-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5d75-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d75-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d75-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a5d75-133">IDL</span><span class="sxs-lookup"><span data-stu-id="a5d75-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5d75-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5d75-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a5d75-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5d75-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5d75-136"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a5d75-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




