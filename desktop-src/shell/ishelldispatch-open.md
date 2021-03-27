---
description: Abre la carpeta especificada.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: Método IShellDispatch. Open (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810964"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="4673f-103">IShellDispatch. Open (método)</span><span class="sxs-lookup"><span data-stu-id="4673f-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="4673f-104">Abre la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="4673f-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="4673f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4673f-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="4673f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4673f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4673f-107">*vDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4673f-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4673f-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="4673f-108">Type: **Variant**</span></span>

<span data-ttu-id="4673f-109">Cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="4673f-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="4673f-110">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="4673f-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="4673f-111">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4673f-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="4673f-112">Si *vDir* está establecido en uno de los [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) y la carpeta Special no existe, esta función creará la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4673f-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4673f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4673f-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4673f-114">JScript</span><span class="sxs-lookup"><span data-stu-id="4673f-114">JScript</span></span>

<span data-ttu-id="4673f-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4673f-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="4673f-116">VB</span><span class="sxs-lookup"><span data-stu-id="4673f-116">VB</span></span>

<span data-ttu-id="4673f-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4673f-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4673f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4673f-118">Remarks</span></span>

<span data-ttu-id="4673f-119">Este método se implementa y se obtiene acceso a él a través del método [**Shell. Open**](shell-open.md) .</span><span class="sxs-lookup"><span data-stu-id="4673f-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="4673f-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4673f-120">Examples</span></span>

<span data-ttu-id="4673f-121">En los siguientes ejemplos se muestra el uso de **Open** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4673f-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4673f-122">JScript.net</span><span class="sxs-lookup"><span data-stu-id="4673f-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="4673f-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="4673f-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4673f-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4673f-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4673f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4673f-125">Requirements</span></span>



| <span data-ttu-id="4673f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4673f-126">Requirement</span></span> | <span data-ttu-id="4673f-127">Value</span><span class="sxs-lookup"><span data-stu-id="4673f-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4673f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4673f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4673f-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4673f-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4673f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4673f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4673f-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4673f-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4673f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4673f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4673f-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4673f-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4673f-134">IDL</span><span class="sxs-lookup"><span data-stu-id="4673f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4673f-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4673f-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4673f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4673f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4673f-137"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4673f-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4673f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="4673f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4673f-139">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="4673f-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="4673f-140">**Explorar**</span><span class="sxs-lookup"><span data-stu-id="4673f-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




