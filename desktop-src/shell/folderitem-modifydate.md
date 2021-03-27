---
description: Para un archivo, establece u obtiene la fecha y la hora en que se modificó por última vez. Para una carpeta, recupera la fecha y la hora en que se modificó por última vez una carpeta, pero no puede establecerla.
ms.assetid: bb60c800-863b-469b-b937-9816b8b338bf
title: Propiedad carpeta. ModifyDate (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.ModifyDate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9ea5fa6b611a0311840507fb2068d08801a5bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153612"
---
# <a name="folderitemmodifydate-property"></a><span data-ttu-id="4b7c9-104">Propiedad carpeta. ModifyDate</span><span class="sxs-lookup"><span data-stu-id="4b7c9-104">FolderItem.ModifyDate property</span></span>

<span data-ttu-id="4b7c9-105">Para un archivo, establece u obtiene la fecha y la hora en que se modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="4b7c9-105">For a file, sets or gets the date and time that it was last modified.</span></span> <span data-ttu-id="4b7c9-106">Para una carpeta, recupera la fecha y la hora en que se modificó por última vez una carpeta, pero no puede establecerla.</span><span class="sxs-lookup"><span data-stu-id="4b7c9-106">For a folder, retrieves the date and time that a folder was last modified, but cannot set it.</span></span>

<span data-ttu-id="4b7c9-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4b7c9-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7c9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b7c9-108">Syntax</span></span>


```JScript
iModifyDate = FolderItem.ModifyDate
FolderItem.ModifyDate = iModifyDate
```



## <a name="property-value"></a><span data-ttu-id="4b7c9-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4b7c9-109">Property value</span></span>

<span data-ttu-id="4b7c9-110">**Fecha** que especifica o recibe la fecha y la hora en que se modificó por última vez el elemento.</span><span class="sxs-lookup"><span data-stu-id="4b7c9-110">**Date** that specifies or receives the date and time that the item was last modified.</span></span>

## <a name="examples"></a><span data-ttu-id="4b7c9-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4b7c9-111">Examples</span></span>

<span data-ttu-id="4b7c9-112">En el ejemplo siguiente se usa **ModifyDate** para recuperar la fecha de la última modificación del Bloc de notas y, a continuación, restablecerla hace mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="4b7c9-112">The following example uses **ModifyDate** to retrieve the last modified date of Notepad and then reset it to a very long time ago.</span></span> <span data-ttu-id="4b7c9-113">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4b7c9-113">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4b7c9-114">JScript.net</span><span class="sxs-lookup"><span data-stu-id="4b7c9-114">JScript:</span></span>


```JScript
<script language="JScript">
    function fnModifyDateGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.ModifyDate;
                objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM";
            }
        }
    }
</script>
```



<span data-ttu-id="4b7c9-115">VBScript</span><span class="sxs-lookup"><span data-stu-id="4b7c9-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnModifyDateGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="4b7c9-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4b7c9-116">Visual Basic:</span></span>


```VB
Private Sub fnModifyDateGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.ModifyDate
                    objFolderItem.ModifyDate = "01/01/1900 6:05:00 PM"
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



## <a name="requirements"></a><span data-ttu-id="4b7c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b7c9-117">Requirements</span></span>



| <span data-ttu-id="4b7c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b7c9-118">Requirement</span></span> | <span data-ttu-id="4b7c9-119">Value</span><span class="sxs-lookup"><span data-stu-id="4b7c9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7c9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b7c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b7c9-121">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4b7c9-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b7c9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b7c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b7c9-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b7c9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b7c9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b7c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b7c9-125"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c9-125"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4b7c9-126">IDL</span><span class="sxs-lookup"><span data-stu-id="4b7c9-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b7c9-127"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c9-127"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4b7c9-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b7c9-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b7c9-129"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4b7c9-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




