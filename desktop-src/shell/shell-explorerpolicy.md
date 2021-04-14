---
description: Obtiene el valor de una directiva especificada de Windows Internet Explorer.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Método Shell. ExplorerPolicy (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986091"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="d15c6-103">Shell. ExplorerPolicy (método)</span><span class="sxs-lookup"><span data-stu-id="d15c6-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="d15c6-104">Obtiene el valor de una directiva especificada de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d15c6-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="d15c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d15c6-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="d15c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d15c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d15c6-107">*bstrPolicyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d15c6-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d15c6-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="d15c6-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="d15c6-109">**Cadena** que especifica el nombre de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="d15c6-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d15c6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d15c6-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d15c6-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d15c6-111">JScript</span></span>

<span data-ttu-id="d15c6-112">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="d15c6-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="d15c6-113">Valor asociado al nombre de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="d15c6-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="d15c6-114">VB</span><span class="sxs-lookup"><span data-stu-id="d15c6-114">VB</span></span>

<span data-ttu-id="d15c6-115">Tipo: _*variante \**_</span><span class="sxs-lookup"><span data-stu-id="d15c6-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="d15c6-116">Valor asociado al nombre de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="d15c6-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="d15c6-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d15c6-117">Remarks</span></span>

<span data-ttu-id="d15c6-118">Los administradores de red pueden controlar y administrar el entorno informático de sus usuarios mediante la configuración de directivas.</span><span class="sxs-lookup"><span data-stu-id="d15c6-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="d15c6-119">El nombre de valor especificado debe estar dentro de la subclave _ \*HKEY \_ Current \_ User **\\** software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer\*\*.</span><span class="sxs-lookup"><span data-stu-id="d15c6-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="d15c6-120">Si el nombre del valor no existe, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="d15c6-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="d15c6-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d15c6-121">Examples</span></span>

<span data-ttu-id="d15c6-122">En los siguientes ejemplos se muestra el uso correcto de **ExplorerPolicy** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d15c6-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d15c6-123">JScript.net</span><span class="sxs-lookup"><span data-stu-id="d15c6-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="d15c6-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="d15c6-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d15c6-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d15c6-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d15c6-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d15c6-126">Requirements</span></span>



| <span data-ttu-id="d15c6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d15c6-127">Requirement</span></span> | <span data-ttu-id="d15c6-128">Value</span><span class="sxs-lookup"><span data-stu-id="d15c6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d15c6-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d15c6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d15c6-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d15c6-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="d15c6-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d15c6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d15c6-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d15c6-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d15c6-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d15c6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d15c6-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d15c6-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d15c6-135">IDL</span><span class="sxs-lookup"><span data-stu-id="d15c6-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d15c6-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d15c6-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d15c6-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d15c6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d15c6-138"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d15c6-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
