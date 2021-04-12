---
description: Crea y devuelve un objeto de carpeta para la carpeta especificada.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Método Shell. NameSpace (Shldisp. h)
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
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276871"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="712c2-103">Shell. NameSpace (método)</span><span class="sxs-lookup"><span data-stu-id="712c2-103">Shell.NameSpace method</span></span>

<span data-ttu-id="712c2-104">Crea y devuelve un objeto de [**carpeta**](folder.md) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="712c2-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="712c2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="712c2-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="712c2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="712c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="712c2-107">*vDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="712c2-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="712c2-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="712c2-108">Type: **Variant**</span></span>

<span data-ttu-id="712c2-109">Carpeta para la que se va a crear el objeto de [**carpeta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="712c2-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="712c2-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="712c2-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="712c2-111">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="712c2-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="712c2-112">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="712c2-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="712c2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="712c2-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="712c2-114">JScript</span><span class="sxs-lookup"><span data-stu-id="712c2-114">JScript</span></span>

<span data-ttu-id="712c2-115">Tipo: **[ **carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="712c2-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="712c2-116">Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="712c2-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="712c2-117">Si la carpeta no se ha creado correctamente, este valor devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="712c2-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="712c2-118">VB</span><span class="sxs-lookup"><span data-stu-id="712c2-118">VB</span></span>

<span data-ttu-id="712c2-119">Tipo: **[ **carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="712c2-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="712c2-120">Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="712c2-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="712c2-121">Si la carpeta no se ha creado correctamente, este valor devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="712c2-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="712c2-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="712c2-122">Examples</span></span>

<span data-ttu-id="712c2-123">En el ejemplo siguiente se muestra el **espacio de nombres** en uso.</span><span class="sxs-lookup"><span data-stu-id="712c2-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="712c2-124">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="712c2-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="712c2-125">JScript.net</span><span class="sxs-lookup"><span data-stu-id="712c2-125">JScript:</span></span>


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



<span data-ttu-id="712c2-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="712c2-126">VBScript:</span></span>


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



<span data-ttu-id="712c2-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="712c2-127">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="712c2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="712c2-128">Requirements</span></span>



| <span data-ttu-id="712c2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="712c2-129">Requirement</span></span> | <span data-ttu-id="712c2-130">Value</span><span class="sxs-lookup"><span data-stu-id="712c2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="712c2-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="712c2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="712c2-132">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="712c2-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="712c2-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="712c2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="712c2-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="712c2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="712c2-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="712c2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="712c2-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="712c2-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="712c2-137">IDL</span><span class="sxs-lookup"><span data-stu-id="712c2-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="712c2-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="712c2-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="712c2-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="712c2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="712c2-140"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="712c2-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




