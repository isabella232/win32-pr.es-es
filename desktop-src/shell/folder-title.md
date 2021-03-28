---
description: Contiene el título de la carpeta.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Propiedad Folder. title (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985502"
---
# <a name="foldertitle-property"></a><span data-ttu-id="f4b32-103">Folder. title (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f4b32-103">Folder.Title property</span></span>

<span data-ttu-id="f4b32-104">Contiene el título de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f4b32-104">Contains the title of the folder.</span></span>

<span data-ttu-id="f4b32-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f4b32-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b32-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4b32-106">Syntax</span></span>


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a><span data-ttu-id="f4b32-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f4b32-107">Property value</span></span>

<span data-ttu-id="f4b32-108">Cadena que contiene el título del objeto.</span><span class="sxs-lookup"><span data-stu-id="f4b32-108">A string containing the object's title.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b32-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4b32-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4b32-110">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="f4b32-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="f4b32-111">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="f4b32-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="f4b32-112">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="f4b32-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f4b32-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f4b32-113">Examples</span></span>

<span data-ttu-id="f4b32-114">En el ejemplo siguiente se usa **title** para recuperar el título de la carpeta que contiene los grupos de programas del usuario (normalmente, "Programs").</span><span class="sxs-lookup"><span data-stu-id="f4b32-114">The following example uses **Title** to retrieve the title of the folder holding the user's program groups (usually "Programs").</span></span> <span data-ttu-id="f4b32-115">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f4b32-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f4b32-116">JScript.net</span><span class="sxs-lookup"><span data-stu-id="f4b32-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="f4b32-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="f4b32-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f4b32-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f4b32-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f4b32-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4b32-119">Requirements</span></span>



| <span data-ttu-id="f4b32-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4b32-120">Requirement</span></span> | <span data-ttu-id="f4b32-121">Value</span><span class="sxs-lookup"><span data-stu-id="f4b32-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4b32-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4b32-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4b32-123">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f4b32-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4b32-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4b32-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4b32-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f4b32-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f4b32-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4b32-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4b32-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4b32-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f4b32-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f4b32-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4b32-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4b32-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f4b32-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4b32-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4b32-131"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f4b32-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




