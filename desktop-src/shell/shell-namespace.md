---
description: 'Método Shell.NameSpace: crea y devuelve un objeto Folder para la carpeta especificada.'
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Método Shell.NameSpace (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fab501912c55aaaf6cab832bf76763672e830d33
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083715"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="a7b89-103">Shell.NameSpace (método)</span><span class="sxs-lookup"><span data-stu-id="a7b89-103">Shell.NameSpace method</span></span>

<span data-ttu-id="a7b89-104">Crea y devuelve un [**objeto Folder**](folder.md) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="a7b89-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7b89-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7b89-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="a7b89-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7b89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b89-107">*vDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a7b89-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7b89-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="a7b89-108">Type: **Variant**</span></span>

<span data-ttu-id="a7b89-109">Carpeta para la que se va a crear [**el objeto Folder.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="a7b89-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="a7b89-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="a7b89-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="a7b89-111">Tenga en cuenta que los nombres constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="a7b89-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="a7b89-112">En esos casos, los valores numéricos deben usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a7b89-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b89-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7b89-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a7b89-114">JScript</span><span class="sxs-lookup"><span data-stu-id="a7b89-114">JScript</span></span>

<span data-ttu-id="a7b89-115">Tipo: **[ **Carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a7b89-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="a7b89-116">Referencia de objeto al [**objeto Folder**](folder.md) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="a7b89-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="a7b89-117">Si la carpeta no se ha creado correctamente, este valor devuelve **null.**</span><span class="sxs-lookup"><span data-stu-id="a7b89-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="a7b89-118">VB</span><span class="sxs-lookup"><span data-stu-id="a7b89-118">VB</span></span>

<span data-ttu-id="a7b89-119">Tipo: **[ **Carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a7b89-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="a7b89-120">Referencia de objeto al [**objeto Folder**](folder.md) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="a7b89-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="a7b89-121">Si la carpeta no se ha creado correctamente, este valor devuelve **null.**</span><span class="sxs-lookup"><span data-stu-id="a7b89-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="a7b89-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a7b89-122">Examples</span></span>

<span data-ttu-id="a7b89-123">En el ejemplo siguiente se **muestra NameSpace** en uso.</span><span class="sxs-lookup"><span data-stu-id="a7b89-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="a7b89-124">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a7b89-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a7b89-125">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a7b89-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="a7b89-126">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a7b89-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a7b89-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a7b89-127">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a7b89-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7b89-128">Requirements</span></span>



| <span data-ttu-id="a7b89-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7b89-129">Requirement</span></span> | <span data-ttu-id="a7b89-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a7b89-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b89-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7b89-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b89-132">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="a7b89-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a7b89-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7b89-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b89-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a7b89-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7b89-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7b89-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b89-136"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b89-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a7b89-137">Idl</span><span class="sxs-lookup"><span data-stu-id="a7b89-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7b89-138"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7b89-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a7b89-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7b89-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7b89-140"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a7b89-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




