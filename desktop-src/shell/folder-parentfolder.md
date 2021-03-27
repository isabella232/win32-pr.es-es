---
description: Contiene el objeto de carpeta principal.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Propiedad Folder. ParentFolder (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001912"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="0f7e6-103">Propiedad Folder. ParentFolder</span><span class="sxs-lookup"><span data-stu-id="0f7e6-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="0f7e6-104">Contiene el objeto de [**carpeta**](folder.md) principal.</span><span class="sxs-lookup"><span data-stu-id="0f7e6-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="0f7e6-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0f7e6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7e6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f7e6-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="0f7e6-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0f7e6-107">Property value</span></span>

<span data-ttu-id="0f7e6-108">Una referencia de objeto al objeto ParentFolder.</span><span class="sxs-lookup"><span data-stu-id="0f7e6-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7e6-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f7e6-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0f7e6-110">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="0f7e6-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="0f7e6-111">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="0f7e6-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="0f7e6-112">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="0f7e6-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0f7e6-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0f7e6-113">Examples</span></span>

<span data-ttu-id="0f7e6-114">En el ejemplo siguiente se muestra el uso correcto de **ParentFolder** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0f7e6-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0f7e6-115">JScript.net</span><span class="sxs-lookup"><span data-stu-id="0f7e6-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



<span data-ttu-id="0f7e6-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="0f7e6-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0f7e6-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0f7e6-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0f7e6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f7e6-118">Requirements</span></span>



| <span data-ttu-id="0f7e6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f7e6-119">Requirement</span></span> | <span data-ttu-id="0f7e6-120">Value</span><span class="sxs-lookup"><span data-stu-id="0f7e6-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f7e6-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f7e6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0f7e6-122">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0f7e6-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0f7e6-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f7e6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0f7e6-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f7e6-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0f7e6-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f7e6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f7e6-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f7e6-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0f7e6-127">IDL</span><span class="sxs-lookup"><span data-stu-id="0f7e6-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f7e6-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f7e6-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0f7e6-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f7e6-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f7e6-130"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="0f7e6-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




