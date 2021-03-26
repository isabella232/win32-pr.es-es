---
description: Abre una carpeta especificada en una ventana del explorador de Windows.
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Método Shell. Explore (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 00b597aea0121e5f87f51886e8019a1130a20584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002725"
---
# <a name="shellexplore-method"></a><span data-ttu-id="11a7e-103">Shell. Explore (método)</span><span class="sxs-lookup"><span data-stu-id="11a7e-103">Shell.Explore method</span></span>

<span data-ttu-id="11a7e-104">Abre una carpeta especificada en una ventana del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="11a7e-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11a7e-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="11a7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11a7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a7e-107">*vDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11a7e-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a7e-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="11a7e-108">Type: **Variant**</span></span>

<span data-ttu-id="11a7e-109">Carpeta que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="11a7e-109">The folder to be displayed.</span></span> <span data-ttu-id="11a7e-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="11a7e-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="11a7e-111">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="11a7e-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="11a7e-112">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="11a7e-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a7e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11a7e-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="11a7e-114">JScript</span><span class="sxs-lookup"><span data-stu-id="11a7e-114">JScript</span></span>

<span data-ttu-id="11a7e-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="11a7e-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="11a7e-116">VB</span><span class="sxs-lookup"><span data-stu-id="11a7e-116">VB</span></span>

<span data-ttu-id="11a7e-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="11a7e-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="11a7e-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="11a7e-118">Examples</span></span>

<span data-ttu-id="11a7e-119">En el ejemplo siguiente se muestra la **exploración** en uso.</span><span class="sxs-lookup"><span data-stu-id="11a7e-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="11a7e-120">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11a7e-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="11a7e-121">JScript.net</span><span class="sxs-lookup"><span data-stu-id="11a7e-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="11a7e-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="11a7e-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="11a7e-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="11a7e-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="11a7e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11a7e-124">Requirements</span></span>



| <span data-ttu-id="11a7e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="11a7e-125">Requirement</span></span> | <span data-ttu-id="11a7e-126">Value</span><span class="sxs-lookup"><span data-stu-id="11a7e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11a7e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11a7e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="11a7e-128">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="11a7e-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11a7e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11a7e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="11a7e-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="11a7e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11a7e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11a7e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="11a7e-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11a7e-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="11a7e-133">IDL</span><span class="sxs-lookup"><span data-stu-id="11a7e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11a7e-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11a7e-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="11a7e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11a7e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11a7e-136"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="11a7e-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




