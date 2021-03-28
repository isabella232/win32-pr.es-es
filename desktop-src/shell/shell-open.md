---
description: Abre la carpeta especificada.
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Método Shell. Open (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3572f48a7b129500c38c3c0227ba479ecb775067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910762"
---
# <a name="shellopen-method"></a><span data-ttu-id="f6bde-103">Shell. Open (método)</span><span class="sxs-lookup"><span data-stu-id="f6bde-103">Shell.Open method</span></span>

<span data-ttu-id="f6bde-104">Abre la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="f6bde-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6bde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6bde-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="f6bde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6bde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6bde-107">*vDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6bde-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6bde-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="f6bde-108">Type: **Variant**</span></span>

<span data-ttu-id="f6bde-109">Cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="f6bde-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="f6bde-110">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="f6bde-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="f6bde-111">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f6bde-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="f6bde-112">Si *vDir* está establecido en uno de los [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) y la carpeta Special no existe, esta función creará la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f6bde-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f6bde-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6bde-113">Examples</span></span>

<span data-ttu-id="f6bde-114">En el ejemplo siguiente se muestra **abierto** en uso.</span><span class="sxs-lookup"><span data-stu-id="f6bde-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="f6bde-115">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6bde-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f6bde-116">JScript.net</span><span class="sxs-lookup"><span data-stu-id="f6bde-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="f6bde-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="f6bde-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f6bde-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f6bde-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f6bde-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6bde-119">Requirements</span></span>



| <span data-ttu-id="f6bde-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6bde-120">Requirement</span></span> | <span data-ttu-id="f6bde-121">Value</span><span class="sxs-lookup"><span data-stu-id="f6bde-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6bde-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6bde-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6bde-123">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f6bde-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6bde-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6bde-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6bde-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6bde-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6bde-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6bde-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6bde-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6bde-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f6bde-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f6bde-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6bde-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6bde-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f6bde-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6bde-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6bde-131"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f6bde-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6bde-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6bde-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6bde-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="f6bde-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="f6bde-134">**Explorar**</span><span class="sxs-lookup"><span data-stu-id="f6bde-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




