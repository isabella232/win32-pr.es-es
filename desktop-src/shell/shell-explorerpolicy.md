---
description: 'Método Shell.ExplorerPolicy: obtiene el valor de una directiva de Internet Explorer Windows especificada.'
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Método Shell.ExplorerPolicy (Shldisp.h)
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
ms.openlocfilehash: 765e1dc46edbe5a27292c5d8ff940e29b269f8dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083703"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="c1fae-103">Método Shell.ExplorerPolicy</span><span class="sxs-lookup"><span data-stu-id="c1fae-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="c1fae-104">Obtiene el valor de una directiva de windows Internet Explorer especificada.</span><span class="sxs-lookup"><span data-stu-id="c1fae-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1fae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1fae-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="c1fae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1fae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1fae-107">*bstrPolicyName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c1fae-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1fae-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c1fae-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c1fae-109">Cadena **que** especifica el nombre de la directiva.</span><span class="sxs-lookup"><span data-stu-id="c1fae-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1fae-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c1fae-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c1fae-111">JScript</span><span class="sxs-lookup"><span data-stu-id="c1fae-111">JScript</span></span>

<span data-ttu-id="c1fae-112">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="c1fae-112">Type: **Variant\***</span></span>

<span data-ttu-id="c1fae-113">Valor asociado al nombre de directiva especificado.</span><span class="sxs-lookup"><span data-stu-id="c1fae-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="c1fae-114">VB</span><span class="sxs-lookup"><span data-stu-id="c1fae-114">VB</span></span>

<span data-ttu-id="c1fae-115">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="c1fae-115">Type: **Variant\***</span></span>

<span data-ttu-id="c1fae-116">Valor asociado al nombre de directiva especificado.</span><span class="sxs-lookup"><span data-stu-id="c1fae-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1fae-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1fae-117">Remarks</span></span>

<span data-ttu-id="c1fae-118">Los administradores de red pueden controlar y administrar el entorno informático de sus usuarios estableciendo directivas.</span><span class="sxs-lookup"><span data-stu-id="c1fae-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="c1fae-119">El nombre de valor especificado debe estar dentro de la subclave **HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **Explorer.**</span><span class="sxs-lookup"><span data-stu-id="c1fae-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="c1fae-120">Si el nombre del valor no existe, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="c1fae-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="c1fae-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c1fae-121">Examples</span></span>

<span data-ttu-id="c1fae-122">En los ejemplos siguientes se muestra el uso adecuado de **ExplorerPolicy** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c1fae-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c1fae-123">Jscript:</span><span class="sxs-lookup"><span data-stu-id="c1fae-123">JScript:</span></span>


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



<span data-ttu-id="c1fae-124">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="c1fae-124">VBScript:</span></span>


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



<span data-ttu-id="c1fae-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c1fae-125">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c1fae-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1fae-126">Requirements</span></span>



| <span data-ttu-id="c1fae-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1fae-127">Requirement</span></span> | <span data-ttu-id="c1fae-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c1fae-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1fae-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1fae-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1fae-130">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c1fae-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c1fae-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1fae-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1fae-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1fae-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c1fae-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c1fae-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1fae-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c1fae-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c1fae-135">Idl</span><span class="sxs-lookup"><span data-stu-id="c1fae-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c1fae-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c1fae-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c1fae-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1fae-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1fae-138"><dt>Shell32.dll (versión 6.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c1fae-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
