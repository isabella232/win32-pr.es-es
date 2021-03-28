---
description: Recupera un objeto FolderItems que representa la colección de elementos de la carpeta.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Método Folder. items (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360680"
---
# <a name="folderitems-method"></a><span data-ttu-id="64dfd-103">Folder. items (método)</span><span class="sxs-lookup"><span data-stu-id="64dfd-103">Folder.Items method</span></span>

<span data-ttu-id="64dfd-104">Recupera un objeto [**FolderItems**](folderitems.md) que representa la colección de elementos de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="64dfd-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="64dfd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64dfd-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="64dfd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64dfd-106">Parameters</span></span>

<span data-ttu-id="64dfd-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="64dfd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64dfd-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64dfd-108">Return value</span></span>

<span data-ttu-id="64dfd-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="64dfd-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="64dfd-110">Una referencia de objeto al objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="64dfd-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64dfd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="64dfd-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64dfd-112">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="64dfd-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="64dfd-113">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="64dfd-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="64dfd-114">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="64dfd-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="64dfd-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="64dfd-115">Examples</span></span>

<span data-ttu-id="64dfd-116">En el ejemplo siguiente se usan **elementos** para determinar el número de elementos de la \\ carpeta C: Windows.</span><span class="sxs-lookup"><span data-stu-id="64dfd-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="64dfd-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="64dfd-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="64dfd-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="64dfd-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="64dfd-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="64dfd-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="64dfd-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="64dfd-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="64dfd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64dfd-121">Requirements</span></span>



| <span data-ttu-id="64dfd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="64dfd-122">Requirement</span></span> | <span data-ttu-id="64dfd-123">Value</span><span class="sxs-lookup"><span data-stu-id="64dfd-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64dfd-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64dfd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="64dfd-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="64dfd-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64dfd-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64dfd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="64dfd-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="64dfd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64dfd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="64dfd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="64dfd-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="64dfd-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="64dfd-130">IDL</span><span class="sxs-lookup"><span data-stu-id="64dfd-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64dfd-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64dfd-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="64dfd-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64dfd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64dfd-133"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="64dfd-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




