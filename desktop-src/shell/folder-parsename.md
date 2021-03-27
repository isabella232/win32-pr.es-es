---
description: Crea y devuelve un objeto carpeta que representa un elemento especificado.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Método Folder. ParseName (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808030"
---
# <a name="folderparsename-method"></a><span data-ttu-id="842b5-103">Folder. ParseName (método)</span><span class="sxs-lookup"><span data-stu-id="842b5-103">Folder.ParseName method</span></span>

<span data-ttu-id="842b5-104">Crea y devuelve un objeto [**carpeta**](folderitem.md) que representa un elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="842b5-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="842b5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="842b5-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="842b5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="842b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="842b5-107">*bName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="842b5-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842b5-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="842b5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="842b5-109">Cadena que especifica el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="842b5-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="842b5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="842b5-110">Return value</span></span>

<span data-ttu-id="842b5-111">Tipo: **[ **carpeta**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="842b5-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="842b5-112">Una referencia de objeto al objeto [**carpeta**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="842b5-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="842b5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="842b5-113">Remarks</span></span>

<span data-ttu-id="842b5-114">**ParseName** no debe usarse para carpetas virtuales como mis documentos.</span><span class="sxs-lookup"><span data-stu-id="842b5-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="842b5-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="842b5-115">Examples</span></span>

<span data-ttu-id="842b5-116">En el ejemplo siguiente se usa **ParseName** para crear un objeto que representa el elemento de carpeta Clock.avi en la carpeta C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="842b5-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="842b5-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="842b5-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="842b5-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="842b5-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="842b5-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="842b5-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="842b5-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="842b5-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="842b5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="842b5-121">Requirements</span></span>



| <span data-ttu-id="842b5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="842b5-122">Requirement</span></span> | <span data-ttu-id="842b5-123">Value</span><span class="sxs-lookup"><span data-stu-id="842b5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842b5-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="842b5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="842b5-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="842b5-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="842b5-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="842b5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="842b5-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="842b5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="842b5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="842b5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="842b5-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="842b5-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="842b5-130">IDL</span><span class="sxs-lookup"><span data-stu-id="842b5-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="842b5-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="842b5-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="842b5-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="842b5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="842b5-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="842b5-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
