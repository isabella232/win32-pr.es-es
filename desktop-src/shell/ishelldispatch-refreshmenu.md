---
description: Obtenga información sobre el método IShellDispatch.RefreshMenu, que actualiza el contenido de la menú Inicio. Solo se usa con sistemas anteriores a Windows XP.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Método IShellDispatch.RefreshMenu (Shldisp.h)
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
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404678"
---
# <a name="ishelldispatchrefreshmenu-method"></a><span data-ttu-id="5b876-104">Método IShellDispatch.RefreshMenu</span><span class="sxs-lookup"><span data-stu-id="5b876-104">IShellDispatch.RefreshMenu method</span></span>

<span data-ttu-id="5b876-105">Actualiza el contenido del **menú** Inicio.</span><span class="sxs-lookup"><span data-stu-id="5b876-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="5b876-106">Solo se usa con sistemas anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b876-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b876-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b876-107">Syntax</span></span>


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a><span data-ttu-id="5b876-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b876-108">Parameters</span></span>

<span data-ttu-id="5b876-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5b876-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b876-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b876-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5b876-111">JScript</span><span class="sxs-lookup"><span data-stu-id="5b876-111">JScript</span></span>

<span data-ttu-id="5b876-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5b876-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="5b876-113">VB</span><span class="sxs-lookup"><span data-stu-id="5b876-113">VB</span></span>

<span data-ttu-id="5b876-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="5b876-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b876-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b876-115">Remarks</span></span>

<span data-ttu-id="5b876-116">Este método se implementa y se accede a través del [**método Shell.TrayProperties.**](shell-trayproperties.md)</span><span class="sxs-lookup"><span data-stu-id="5b876-116">This method is implemented and accessed through the [**Shell.TrayProperties**](shell-trayproperties.md) method.</span></span>

<span data-ttu-id="5b876-117">La funcionalidad **que proporciona RefreshMenu** se controla automáticamente en Windows XP o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5b876-117">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="5b876-118">No llame a este método en Windows XP o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="5b876-118">Do not call this method on Windows XP or later.</span></span>

## <a name="examples"></a><span data-ttu-id="5b876-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5b876-119">Examples</span></span>

<span data-ttu-id="5b876-120">En los ejemplos siguientes se muestra el uso **de RefreshMenu** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b876-120">The following examples show the use of **RefreshMenu** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5b876-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="5b876-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="5b876-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="5b876-122">VBScript:</span></span>


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



<span data-ttu-id="5b876-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5b876-123">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5b876-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b876-124">Requirements</span></span>



| <span data-ttu-id="5b876-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b876-125">Requirement</span></span> | <span data-ttu-id="5b876-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5b876-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b876-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b876-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5b876-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="5b876-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5b876-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b876-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5b876-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5b876-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5b876-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b876-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b876-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5b876-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5b876-133">Idl</span><span class="sxs-lookup"><span data-stu-id="5b876-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b876-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b876-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5b876-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b876-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b876-136"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5b876-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




