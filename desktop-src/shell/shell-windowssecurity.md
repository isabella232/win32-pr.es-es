---
description: Muestra el cuadro de diálogo seguridad de Windows.
title: Método Shell. WindowsSecurity (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.WindowsSecurity
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 94916E29-5960-4010-B2C6-0FAA1E4BF72D
ms.openlocfilehash: bbefa4c772adde64b8142b7e3563315fe4833b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545907"
---
# <a name="shellwindowssecurity-method"></a><span data-ttu-id="9a2f2-103">Shell. WindowsSecurity (método)</span><span class="sxs-lookup"><span data-stu-id="9a2f2-103">Shell.WindowsSecurity method</span></span>

<span data-ttu-id="9a2f2-104">Muestra el cuadro de diálogo **seguridad de Windows** .</span><span class="sxs-lookup"><span data-stu-id="9a2f2-104">Displays the **Windows Security** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a2f2-105">Syntax</span></span>


```JScript
Shell.WindowsSecurity()
```


```VB

Shell.WindowsSecurity()
```





## <a name="parameters"></a><span data-ttu-id="9a2f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9a2f2-106">Parameters</span></span>

<span data-ttu-id="9a2f2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9a2f2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a2f2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9a2f2-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9a2f2-109">JScript</span><span class="sxs-lookup"><span data-stu-id="9a2f2-109">JScript</span></span>

<span data-ttu-id="9a2f2-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9a2f2-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9a2f2-111">VB</span><span class="sxs-lookup"><span data-stu-id="9a2f2-111">VB</span></span>

<span data-ttu-id="9a2f2-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9a2f2-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a2f2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9a2f2-113">Remarks</span></span>

<span data-ttu-id="9a2f2-114">Este método muestra el cuadro de diálogo que se muestra después de presionar CTRL + ALT + SUPR o el uso de la opción seguridad en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="9a2f2-114">This method displays the dialog box shown after pressing CTRL+ALT+DELETE or using the security option on the **Start** menu.</span></span>

> [!Note]  
> <span data-ttu-id="9a2f2-115">Este método solo se puede usar cuando está conectado mediante una sesión de terminal a Microsoft Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="9a2f2-115">This method can be used only when connected by a terminal session to Microsoft Terminal Server.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9a2f2-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9a2f2-116">Examples</span></span>

<span data-ttu-id="9a2f2-117">En los siguientes ejemplos se muestra el uso de **WindowsSecurity** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9a2f2-117">The following examples show the use of **WindowsSecurity** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9a2f2-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="9a2f2-118">JScript:</span></span>


```JScript
<script language="JScript">
     function fnIShellDispatch4WindowsSecurityJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.WindowsSecurity();
    }
</script>
```



<span data-ttu-id="9a2f2-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="9a2f2-119">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4WindowsSecurityVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.WindowsSecurity
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9a2f2-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9a2f2-120">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4WindowsSecurityVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
        objShell.WindowsSecurity
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9a2f2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a2f2-121">Requirements</span></span>



| <span data-ttu-id="9a2f2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a2f2-122">Requirement</span></span> | <span data-ttu-id="9a2f2-123">Value</span><span class="sxs-lookup"><span data-stu-id="9a2f2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2f2-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a2f2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2f2-125">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9a2f2-125">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="9a2f2-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9a2f2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2f2-127">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a2f2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="9a2f2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a2f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a2f2-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f2-129"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="9a2f2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="9a2f2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a2f2-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f2-131"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="9a2f2-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9a2f2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a2f2-133"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9a2f2-133"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




