---
description: Muestra el cuadro de diálogo seguridad de Windows.
title: Método IShellDispatch4. WindowsSecurity (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 665c4644-7749-446e-8212-3ecc9901a035
ms.openlocfilehash: 066321c0ea4e4d5ade35a6571c59128a5137cba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984647"
---
# <a name="ishelldispatch4windowssecurity-method"></a><span data-ttu-id="e88e1-103">IShellDispatch4. WindowsSecurity, método</span><span class="sxs-lookup"><span data-stu-id="e88e1-103">IShellDispatch4.WindowsSecurity method</span></span>

<span data-ttu-id="e88e1-104">Muestra el cuadro de diálogo **seguridad de Windows** .</span><span class="sxs-lookup"><span data-stu-id="e88e1-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e88e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e88e1-105">Syntax</span></span>


```JScript
IShellDispatch4.WindowsSecurity()
```


```VB

IShellDispatch4.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="e88e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e88e1-106">Parameters</span></span>

<span data-ttu-id="e88e1-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e88e1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e88e1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e88e1-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e88e1-109">JScript</span><span class="sxs-lookup"><span data-stu-id="e88e1-109">JScript</span></span>

<span data-ttu-id="e88e1-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e88e1-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="e88e1-111">VB</span><span class="sxs-lookup"><span data-stu-id="e88e1-111">VB</span></span>

<span data-ttu-id="e88e1-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e88e1-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e88e1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e88e1-113">Remarks</span></span>

<span data-ttu-id="e88e1-114">Este método muestra el cuadro de diálogo que se muestra después de presionar CTRL + ALT + SUPR o el uso de la opción seguridad en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="e88e1-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="e88e1-115">Este método solo se puede usar cuando está conectado mediante una sesión de terminal a Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="e88e1-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="e88e1-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e88e1-116">Examples</span></span>

<span data-ttu-id="e88e1-117">En los siguientes ejemplos se muestra el uso de **WindowsSecurity** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e88e1-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e88e1-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="e88e1-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="e88e1-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="e88e1-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objshell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e88e1-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e88e1-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objshell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="e88e1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e88e1-121">Requirements</span></span>



| <span data-ttu-id="e88e1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e88e1-122">Requirement</span></span> | <span data-ttu-id="e88e1-123">Value</span><span class="sxs-lookup"><span data-stu-id="e88e1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e88e1-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e88e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e88e1-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e88e1-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="e88e1-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e88e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e88e1-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e88e1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e88e1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e88e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e88e1-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e88e1-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e88e1-130">IDL</span><span class="sxs-lookup"><span data-stu-id="e88e1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e88e1-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e88e1-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e88e1-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e88e1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e88e1-133"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e88e1-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




