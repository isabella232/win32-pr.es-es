---
description: Abre una carpeta especificada en una ventana del explorador de Windows.
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: Método IShellDispatch. Explore (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1ae29b4962dcac1be0b7ea23808e36ce005cb62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984718"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="164f4-103">IShellDispatch. Explore (método)</span><span class="sxs-lookup"><span data-stu-id="164f4-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="164f4-104">Abre una carpeta especificada en una ventana del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="164f4-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="164f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="164f4-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="164f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="164f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="164f4-107">*vDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="164f4-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="164f4-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="164f4-108">Type: **Variant**</span></span>

<span data-ttu-id="164f4-109">Carpeta que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="164f4-109">The folder to be displayed.</span></span> <span data-ttu-id="164f4-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="164f4-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="164f4-111">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="164f4-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="164f4-112">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="164f4-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="164f4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="164f4-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="164f4-114">JScript</span><span class="sxs-lookup"><span data-stu-id="164f4-114">JScript</span></span>

<span data-ttu-id="164f4-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="164f4-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="164f4-116">VB</span><span class="sxs-lookup"><span data-stu-id="164f4-116">VB</span></span>

<span data-ttu-id="164f4-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="164f4-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="164f4-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="164f4-118">Remarks</span></span>

<span data-ttu-id="164f4-119">Este método se implementa y se obtiene acceso a él a través del método [**Shell. Explore**](shell-explore.md) .</span><span class="sxs-lookup"><span data-stu-id="164f4-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="164f4-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="164f4-120">Examples</span></span>

<span data-ttu-id="164f4-121">En los siguientes ejemplos se muestra el uso de **explorar** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="164f4-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="164f4-122">JScript.net</span><span class="sxs-lookup"><span data-stu-id="164f4-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="164f4-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="164f4-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="164f4-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="164f4-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="164f4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="164f4-125">Requirements</span></span>



| <span data-ttu-id="164f4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="164f4-126">Requirement</span></span> | <span data-ttu-id="164f4-127">Value</span><span class="sxs-lookup"><span data-stu-id="164f4-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="164f4-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="164f4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="164f4-129">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="164f4-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="164f4-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="164f4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="164f4-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="164f4-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="164f4-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="164f4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="164f4-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="164f4-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="164f4-134">IDL</span><span class="sxs-lookup"><span data-stu-id="164f4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="164f4-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="164f4-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="164f4-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="164f4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="164f4-137"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="164f4-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




