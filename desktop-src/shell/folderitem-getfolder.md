---
description: Contiene el objeto de la carpeta del elemento, si el elemento es una carpeta.
ms.assetid: 87afd0b6-245b-4550-9f21-aa0426ba8470
title: Propiedad carpeta. GetFolder (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.GetFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d08c774b53d1fa0db74a7d8d282c4f88f237cfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808029"
---
# <a name="folderitemgetfolder-property"></a><span data-ttu-id="44577-103">Propiedad carpeta. GetFolder</span><span class="sxs-lookup"><span data-stu-id="44577-103">FolderItem.GetFolder property</span></span>

<span data-ttu-id="44577-104">Contiene el objeto de la [**carpeta**](folder.md) del elemento, si el elemento es una carpeta.</span><span class="sxs-lookup"><span data-stu-id="44577-104">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span>

<span data-ttu-id="44577-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="44577-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44577-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44577-106">Syntax</span></span>


```JScript
objGetFolder = FolderItem.GetFolder
```



## <a name="property-value"></a><span data-ttu-id="44577-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="44577-107">Property value</span></span>

<span data-ttu-id="44577-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de [**carpeta**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="44577-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the [**Folder**](folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="44577-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="44577-109">Examples</span></span>

<span data-ttu-id="44577-110">En el ejemplo siguiente se usa **GetFolder** para recuperar el objeto de [**carpeta**](folder.md) de la carpeta system32.</span><span class="sxs-lookup"><span data-stu-id="44577-110">The following example uses **GetFolder** to retrieve the [**Folder**](folder.md) object for the System32 folder.</span></span> <span data-ttu-id="44577-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="44577-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="44577-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="44577-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("system32");
            if (objFolderItem != null)
            {
                var objFolder;
                
                objFolder = objFolderItem.GetFolder;
                if (objFolder != null)
                {
                    ...
                }
            }
        }
    }
 </script>
```



<span data-ttu-id="44577-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="44577-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetFolderVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(36)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("system32")
                if (not objFolderItem is nothing) then
                    dim objFolder
                                
                    set objFolder = objFolderItem.GetFolder
                    if (not objFolder is nothing) then
                        'Add code here         
                    end if
                    set objFolder = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="44577-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="44577-114">Visual Basic:</span></span>


```VB
Private Sub fnGetFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("system32")
                If (Not objFolderItem Is Nothing) Then
                    Dim objFolder As Folder2
                    
                    Set objFolder = objFolderItem.GetFolder
                        If (Not objFolder Is Nothing) Then
                            'Add code here
                            Debug.Print "Yes"
                        Else
                            'Folder object returned nothing
                        End If
                    Set objFolder = Nothing
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="44577-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44577-115">Requirements</span></span>



| <span data-ttu-id="44577-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="44577-116">Requirement</span></span> | <span data-ttu-id="44577-117">Value</span><span class="sxs-lookup"><span data-stu-id="44577-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44577-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44577-118">Minimum supported client</span></span><br/> | <span data-ttu-id="44577-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="44577-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44577-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44577-120">Minimum supported server</span></span><br/> | <span data-ttu-id="44577-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="44577-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44577-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44577-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="44577-123"><dt>ShlObj. h (incluye Shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44577-123"><dt>Shlobj.h (include Shldisp.h)</dt></span></span> </dl>        |
| <span data-ttu-id="44577-124">IDL</span><span class="sxs-lookup"><span data-stu-id="44577-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44577-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44577-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="44577-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44577-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44577-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="44577-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44577-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="44577-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44577-129">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="44577-129">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="44577-130">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="44577-130">**IsFolder**</span></span>](folderitem-isfolder.md)
</dt> </dl>

 

 
