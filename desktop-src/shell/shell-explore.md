---
description: 'Método Shell.Explore: abre una carpeta especificada en Explorador de Windows ventana.'
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Método Shell.Explore (Shldisp.h)
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
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104333"
---
# <a name="shellexplore-method"></a><span data-ttu-id="8bf56-103">Método Shell.Explore</span><span class="sxs-lookup"><span data-stu-id="8bf56-103">Shell.Explore method</span></span>

<span data-ttu-id="8bf56-104">Abre una carpeta especificada en una Explorador de Windows ventana.</span><span class="sxs-lookup"><span data-stu-id="8bf56-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf56-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bf56-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="8bf56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8bf56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bf56-107">*vDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8bf56-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bf56-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8bf56-108">Type: **Variant**</span></span>

<span data-ttu-id="8bf56-109">Carpeta que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="8bf56-109">The folder to be displayed.</span></span> <span data-ttu-id="8bf56-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="8bf56-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="8bf56-111">Tenga en cuenta que los nombres constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="8bf56-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="8bf56-112">En esos casos, los valores numéricos deben usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8bf56-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bf56-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8bf56-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8bf56-114">JScript</span><span class="sxs-lookup"><span data-stu-id="8bf56-114">JScript</span></span>

<span data-ttu-id="8bf56-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8bf56-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="8bf56-116">VB</span><span class="sxs-lookup"><span data-stu-id="8bf56-116">VB</span></span>

<span data-ttu-id="8bf56-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="8bf56-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8bf56-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8bf56-118">Examples</span></span>

<span data-ttu-id="8bf56-119">En el ejemplo siguiente se **muestra Explorar** en uso.</span><span class="sxs-lookup"><span data-stu-id="8bf56-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="8bf56-120">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8bf56-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8bf56-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="8bf56-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="8bf56-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="8bf56-122">VBScript:</span></span>


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



<span data-ttu-id="8bf56-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8bf56-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8bf56-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf56-124">Requirements</span></span>



| <span data-ttu-id="8bf56-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf56-125">Requirement</span></span> | <span data-ttu-id="8bf56-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8bf56-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf56-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bf56-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf56-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="8bf56-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8bf56-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bf56-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf56-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8bf56-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8bf56-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8bf56-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf56-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf56-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8bf56-133">Idl</span><span class="sxs-lookup"><span data-stu-id="8bf56-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bf56-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bf56-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8bf56-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bf56-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf56-136"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8bf56-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




