---
description: Crea y devuelve un objeto de carpeta para la carpeta especificada.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Método IShellDispatch. NameSpace (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543150"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="e76df-103">IShellDispatch. NameSpace (método)</span><span class="sxs-lookup"><span data-stu-id="e76df-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="e76df-104">Crea y devuelve un objeto de [**carpeta**](folder.md) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="e76df-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="e76df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e76df-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="e76df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e76df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e76df-107">*vDir* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e76df-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e76df-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="e76df-108">Type: **Variant**</span></span>

<span data-ttu-id="e76df-109">Carpeta para la que se va a crear el objeto de [**carpeta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="e76df-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="e76df-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="e76df-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="e76df-111">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="e76df-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="e76df-112">En estos casos, se deben usar los valores numéricos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="e76df-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e76df-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e76df-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e76df-114">JScript</span><span class="sxs-lookup"><span data-stu-id="e76df-114">JScript</span></span>

<span data-ttu-id="e76df-115">Tipo: **[ **carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e76df-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="e76df-116">Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="e76df-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="e76df-117">Si la carpeta no se ha creado correctamente, este valor devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="e76df-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="e76df-118">VB</span><span class="sxs-lookup"><span data-stu-id="e76df-118">VB</span></span>

<span data-ttu-id="e76df-119">Tipo: **[ **carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e76df-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="e76df-120">Referencia de objeto al objeto de [**carpeta**](folder.md) de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="e76df-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="e76df-121">Si la carpeta no se ha creado correctamente, este valor devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="e76df-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e76df-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e76df-122">Remarks</span></span>

<span data-ttu-id="e76df-123">Este método se implementa y se obtiene acceso a él a través del método [**Shell. Namespace**](shell-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="e76df-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="e76df-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e76df-124">Examples</span></span>

<span data-ttu-id="e76df-125">En los siguientes ejemplos se muestra el uso del [**espacio de nombres**](shell-namespace.md) en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e76df-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e76df-126">JScript.net</span><span class="sxs-lookup"><span data-stu-id="e76df-126">JScript:</span></span>


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



<span data-ttu-id="e76df-127">VBScript</span><span class="sxs-lookup"><span data-stu-id="e76df-127">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e76df-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e76df-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e76df-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e76df-129">Requirements</span></span>



| <span data-ttu-id="e76df-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e76df-130">Requirement</span></span> | <span data-ttu-id="e76df-131">Value</span><span class="sxs-lookup"><span data-stu-id="e76df-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e76df-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e76df-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e76df-133">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e76df-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e76df-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e76df-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e76df-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e76df-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e76df-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e76df-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e76df-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e76df-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e76df-138">IDL</span><span class="sxs-lookup"><span data-stu-id="e76df-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e76df-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e76df-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e76df-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e76df-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e76df-141"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e76df-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




