---
description: Establece un filtro comodín que se va a aplicar a los elementos devueltos.
ms.assetid: 19ca82c5-16ff-46c7-8ea1-ddbfc2ce3ac9
title: Método FolderItems3. Filter (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Filter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26a24dc3ef1f4d0de09dbd97a5dce4c8ed8c783b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808005"
---
# <a name="folderitems3filter-method"></a><span data-ttu-id="deca8-103">FolderItems3. Filter (método)</span><span class="sxs-lookup"><span data-stu-id="deca8-103">FolderItems3.Filter method</span></span>

<span data-ttu-id="deca8-104">Establece un filtro comodín que se va a aplicar a los elementos devueltos.</span><span class="sxs-lookup"><span data-stu-id="deca8-104">Sets a wildcard filter to apply to the items returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="deca8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="deca8-105">Syntax</span></span>


```JScript
iRetVal = FolderItems3.Filter(
  grfFlags,
  bstrFilter
)
```



## <a name="parameters"></a><span data-ttu-id="deca8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="deca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deca8-107">*grfFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="deca8-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deca8-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="deca8-108">Type: **Integer**</span></span>

<span data-ttu-id="deca8-109">Este parámetro puede ser una de las marcas enumeradas en [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span><span class="sxs-lookup"><span data-stu-id="deca8-109">This parameter can be one of the flags listed in [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span></span>

</dd> <dt>

<span data-ttu-id="deca8-110">*bstrFilter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="deca8-110">*bstrFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deca8-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="deca8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="deca8-112">Cadena de filtro que especifica lo que debe aparecer en la colección [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="deca8-112">A filter string that specifies what should be listed in the [**FolderItems**](folderitems.md) collection.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="deca8-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="deca8-113">Examples</span></span>

<span data-ttu-id="deca8-114">En el ejemplo siguiente se muestra el uso correcto del **filtro** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="deca8-114">The following example shows the proper usage of **Filter** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="deca8-115">JScript.net</span><span class="sxs-lookup"><span data-stu-id="deca8-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems3FilterJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var SHCONTF_NONFOLDERS = 64;
                
                alert(objFolderItems3.Count);
                objFolderItems3.Filter(SHCONTF_NONFOLDERS, "*.txt");
                alert(objFolderItems3.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="deca8-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="deca8-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems3FilterVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim SHCONTF_NONFOLDERS
                
                    SHCONTF_NONFOLDERS = 64
                    alert(objFolderItems3.Count)
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.txt"
                    alert(objFolderItems3.Count)
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="deca8-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="deca8-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems3FilterVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim SHCONTF_NONFOLDERS As Long
                    
                    SHCONTF_NONFOLDERS = 64
                    Debug.Print objFolderItems3.Count
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.exe"
                    Debug.Print objFolderItems3.Count
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="deca8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deca8-118">Requirements</span></span>



| <span data-ttu-id="deca8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="deca8-119">Requirement</span></span> | <span data-ttu-id="deca8-120">Value</span><span class="sxs-lookup"><span data-stu-id="deca8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deca8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deca8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="deca8-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="deca8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="deca8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="deca8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="deca8-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="deca8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="deca8-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="deca8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="deca8-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="deca8-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="deca8-127">IDL</span><span class="sxs-lookup"><span data-stu-id="deca8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="deca8-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="deca8-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="deca8-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="deca8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="deca8-130"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="deca8-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="deca8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="deca8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deca8-132">**FolderItems3**</span><span class="sxs-lookup"><span data-stu-id="deca8-132">**FolderItems3**</span></span>](folderitems3-object.md)
</dt> <dt>

[<span data-ttu-id="deca8-133">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="deca8-133">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="deca8-134">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="deca8-134">**FolderItem**</span></span>](folderitem.md)
</dt> </dl>

 

 
