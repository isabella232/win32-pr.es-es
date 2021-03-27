---
description: Obtiene el valor de una directiva especificada de Windows Internet Explorer.
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: Método IShellDispatch4. ExplorerPolicy (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 57247ad328c647cf9cdde32ac1a2951dd8e364ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908233"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="4e08f-103">IShellDispatch4. ExplorerPolicy, método</span><span class="sxs-lookup"><span data-stu-id="4e08f-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="4e08f-104">Obtiene el valor de una directiva especificada de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4e08f-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e08f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e08f-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="4e08f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e08f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e08f-107">*bstrPolicyName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e08f-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e08f-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4e08f-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4e08f-109">**Cadena** que especifica el nombre de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="4e08f-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e08f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e08f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4e08f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="4e08f-111">JScript</span></span>

<span data-ttu-id="4e08f-112">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="4e08f-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="4e08f-113">Valor asociado al nombre de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="4e08f-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="4e08f-114">VB</span><span class="sxs-lookup"><span data-stu-id="4e08f-114">VB</span></span>

<span data-ttu-id="4e08f-115">Tipo: _*variante \**_</span><span class="sxs-lookup"><span data-stu-id="4e08f-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="4e08f-116">Valor asociado al nombre de la Directiva especificada.</span><span class="sxs-lookup"><span data-stu-id="4e08f-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e08f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e08f-117">Remarks</span></span>

<span data-ttu-id="4e08f-118">Los administradores de red pueden controlar y administrar el entorno informático de sus usuarios mediante la configuración de directivas.</span><span class="sxs-lookup"><span data-stu-id="4e08f-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="4e08f-119">El nombre de valor especificado debe estar dentro de la subclave _ \*HKEY \_ Current \_ User **\\** software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer\*\*.</span><span class="sxs-lookup"><span data-stu-id="4e08f-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="4e08f-120">Si el nombre del valor no existe, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="4e08f-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="4e08f-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4e08f-121">Examples</span></span>

<span data-ttu-id="4e08f-122">En los siguientes ejemplos se muestra el uso correcto de **ExplorerPolicy** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4e08f-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4e08f-123">JScript.net</span><span class="sxs-lookup"><span data-stu-id="4e08f-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="4e08f-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="4e08f-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4e08f-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4e08f-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4e08f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e08f-126">Requirements</span></span>



| <span data-ttu-id="4e08f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e08f-127">Requirement</span></span> | <span data-ttu-id="4e08f-128">Value</span><span class="sxs-lookup"><span data-stu-id="4e08f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e08f-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e08f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4e08f-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4e08f-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="4e08f-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e08f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4e08f-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e08f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4e08f-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e08f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e08f-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e08f-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4e08f-135">IDL</span><span class="sxs-lookup"><span data-stu-id="4e08f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e08f-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e08f-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4e08f-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e08f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e08f-138"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4e08f-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
