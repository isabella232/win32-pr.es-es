---
description: 'Método IShellDispatch.Explore: abre una carpeta especificada en Explorador de Windows ventana.'
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: Método IShellDispatch.Explore (Shldisp.h)
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
ms.openlocfilehash: e693985cf7d8d83bd5a00595c42cd4427b0ebd5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100563"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="b4258-103">Método IShellDispatch.Explore</span><span class="sxs-lookup"><span data-stu-id="b4258-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="b4258-104">Abre una carpeta especificada en una Explorador de Windows ventana.</span><span class="sxs-lookup"><span data-stu-id="b4258-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4258-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4258-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b4258-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4258-107">*vDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b4258-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4258-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b4258-108">Type: **Variant**</span></span>

<span data-ttu-id="b4258-109">Carpeta que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="b4258-109">The folder to be displayed.</span></span> <span data-ttu-id="b4258-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="b4258-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="b4258-111">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="b4258-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="b4258-112">En esos casos, los valores numéricos deben usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b4258-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4258-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4258-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b4258-114">JScript</span><span class="sxs-lookup"><span data-stu-id="b4258-114">JScript</span></span>

<span data-ttu-id="b4258-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4258-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b4258-116">VB</span><span class="sxs-lookup"><span data-stu-id="b4258-116">VB</span></span>

<span data-ttu-id="b4258-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b4258-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4258-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b4258-118">Remarks</span></span>

<span data-ttu-id="b4258-119">Este método se implementa y se accede a través del [**método Shell.Explore.**](shell-explore.md)</span><span class="sxs-lookup"><span data-stu-id="b4258-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b4258-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b4258-120">Examples</span></span>

<span data-ttu-id="b4258-121">En los ejemplos siguientes se muestra el uso de **Explore** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b4258-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b4258-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="b4258-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="b4258-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="b4258-123">VBScript:</span></span>


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



<span data-ttu-id="b4258-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b4258-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b4258-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4258-125">Requirements</span></span>



| <span data-ttu-id="b4258-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4258-126">Requirement</span></span> | <span data-ttu-id="b4258-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b4258-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4258-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4258-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4258-129">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="b4258-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b4258-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4258-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4258-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4258-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4258-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4258-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4258-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b4258-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b4258-134">Idl</span><span class="sxs-lookup"><span data-stu-id="b4258-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4258-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4258-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b4258-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4258-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4258-137"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b4258-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




