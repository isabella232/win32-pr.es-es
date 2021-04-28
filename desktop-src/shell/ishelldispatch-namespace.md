---
description: 'Método IShellDispatch.NameSpace: crea y devuelve un objeto Folder para la carpeta especificada.'
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Método IShellDispatch.NameSpace (Shldisp.h)
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
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100523"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="caf3a-103">Método IShellDispatch.NameSpace</span><span class="sxs-lookup"><span data-stu-id="caf3a-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="caf3a-104">Crea y devuelve un [**objeto Folder**](folder.md) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="caf3a-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf3a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="caf3a-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="caf3a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="caf3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caf3a-107">*vDir* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="caf3a-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="caf3a-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="caf3a-108">Type: **Variant**</span></span>

<span data-ttu-id="caf3a-109">Carpeta para la que se va a crear el [**objeto Folder.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="caf3a-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="caf3a-110">Puede ser una cadena que especifica la ruta de acceso de la carpeta o uno de los valores [**de ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="caf3a-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="caf3a-111">Tenga en cuenta que los nombres de constantes que se encuentran en **ShellSpecialFolderConstants** están disponibles en Visual Basic, pero no en VBScript o JScript.</span><span class="sxs-lookup"><span data-stu-id="caf3a-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="caf3a-112">En esos casos, los valores numéricos deben usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="caf3a-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caf3a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="caf3a-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="caf3a-114">JScript</span><span class="sxs-lookup"><span data-stu-id="caf3a-114">JScript</span></span>

<span data-ttu-id="caf3a-115">Tipo: **[ **Carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="caf3a-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="caf3a-116">Referencia de objeto al [**objeto Folder**](folder.md) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="caf3a-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="caf3a-117">Si la carpeta no se ha creado correctamente, este valor devuelve **null.**</span><span class="sxs-lookup"><span data-stu-id="caf3a-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="caf3a-118">VB</span><span class="sxs-lookup"><span data-stu-id="caf3a-118">VB</span></span>

<span data-ttu-id="caf3a-119">Tipo: **[ **Carpeta**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="caf3a-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="caf3a-120">Referencia de objeto al [**objeto Folder**](folder.md) para la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="caf3a-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="caf3a-121">Si la carpeta no se ha creado correctamente, este valor devuelve **null.**</span><span class="sxs-lookup"><span data-stu-id="caf3a-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="caf3a-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="caf3a-122">Remarks</span></span>

<span data-ttu-id="caf3a-123">Este método se implementa y se accede a través del [**método Shell.NameSpace.**](shell-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="caf3a-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="caf3a-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="caf3a-124">Examples</span></span>

<span data-ttu-id="caf3a-125">En los ejemplos siguientes se muestra el uso [**de NameSpace**](shell-namespace.md) en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="caf3a-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="caf3a-126">Jscript:</span><span class="sxs-lookup"><span data-stu-id="caf3a-126">JScript:</span></span>


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



<span data-ttu-id="caf3a-127">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="caf3a-127">VBScript:</span></span>


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



<span data-ttu-id="caf3a-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="caf3a-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="caf3a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caf3a-129">Requirements</span></span>



| <span data-ttu-id="caf3a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="caf3a-130">Requirement</span></span> | <span data-ttu-id="caf3a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="caf3a-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf3a-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="caf3a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="caf3a-133">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="caf3a-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="caf3a-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="caf3a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="caf3a-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="caf3a-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="caf3a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="caf3a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="caf3a-137"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="caf3a-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="caf3a-138">Idl</span><span class="sxs-lookup"><span data-stu-id="caf3a-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="caf3a-139"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="caf3a-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="caf3a-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="caf3a-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="caf3a-141"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="caf3a-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




