---
description: Establece u obtiene el nombre del elemento.
ms.assetid: 079efc8d-3d08-48b1-bdb1-83f4b89fd633
title: Propiedad FolderItem.Name (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f5eb757455b8bbbd4161eae477ca4677eef4fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907559"
---
# <a name="folderitemname-property"></a><span data-ttu-id="b8a74-103">Propiedad FolderItem.Name</span><span class="sxs-lookup"><span data-stu-id="b8a74-103">FolderItem.Name property</span></span>

<span data-ttu-id="b8a74-104">Establece u obtiene el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="b8a74-104">Sets or gets the item's name.</span></span>

<span data-ttu-id="b8a74-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b8a74-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a74-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8a74-106">Syntax</span></span>


```JScript
strName = FolderItem.Name
FolderItem.Name = strName
```



## <a name="property-value"></a><span data-ttu-id="b8a74-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b8a74-107">Property value</span></span>

<span data-ttu-id="b8a74-108">Variable de tipo [**BSTR**](/previous-versions/windows/desktop/automat/bstr) que especifica o recibe el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="b8a74-108">A variable of type [**BSTR**](/previous-versions/windows/desktop/automat/bstr) that specifies or receives the item's name.</span></span>

## <a name="examples"></a><span data-ttu-id="b8a74-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b8a74-109">Examples</span></span>

<span data-ttu-id="b8a74-110">En el ejemplo siguiente se usa **Name** para recuperar el nombre del archivo de Autoexec.bat y, a continuación, restablecer el nombre a Test.bat.</span><span class="sxs-lookup"><span data-stu-id="b8a74-110">The following example uses **Name** to retrieve the name of the Autoexec.bat file, then reset the name to Test.bat.</span></span> <span data-ttu-id="b8a74-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b8a74-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b8a74-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="b8a74-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnNameGetSetJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        
        objFolder2 = objShell.NameSpace("C:\\");
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Name;
                objFolderItem.Name = "TEST.BAT";
            }
        }
    }
</script>
```



<span data-ttu-id="b8a74-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="b8a74-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnNameGetSetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
                
            set objFolder2 = objShell.NameSpace("C:\")
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b8a74-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b8a74-114">Visual Basic:</span></span>


```VB
Private Sub fnNameGetSetVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\")
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("AUTOEXEC.BAT")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Name
                    objFolderItem.Name = "TEST.BAT"
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



## <a name="requirements"></a><span data-ttu-id="b8a74-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8a74-115">Requirements</span></span>



| <span data-ttu-id="b8a74-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a74-116">Requirement</span></span> | <span data-ttu-id="b8a74-117">Value</span><span class="sxs-lookup"><span data-stu-id="b8a74-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a74-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8a74-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a74-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b8a74-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b8a74-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8a74-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a74-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b8a74-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b8a74-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8a74-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a74-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a74-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b8a74-124">IDL</span><span class="sxs-lookup"><span data-stu-id="b8a74-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8a74-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8a74-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b8a74-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8a74-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8a74-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b8a74-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
