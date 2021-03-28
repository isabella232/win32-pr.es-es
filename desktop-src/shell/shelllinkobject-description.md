---
description: Obtiene o establece la descripción del vínculo.
ms.assetid: d3a95281-fb1f-4fd4-9d26-2a6e10a36a86
title: Propiedad ShellLinkObject. Description (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Description
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aff08831bf194da5c7ce958e5a0746abdd533dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985575"
---
# <a name="shelllinkobjectdescription-property"></a><span data-ttu-id="307af-103">ShellLinkObject. Description (propiedad)</span><span class="sxs-lookup"><span data-stu-id="307af-103">ShellLinkObject.Description property</span></span>

<span data-ttu-id="307af-104">Obtiene o establece la descripción del vínculo.</span><span class="sxs-lookup"><span data-stu-id="307af-104">Gets or sets the description of the link.</span></span>

<span data-ttu-id="307af-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="307af-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="307af-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="307af-106">Syntax</span></span>


```JScript
strDescription = ShellLinkObject.Description
ShellLinkObject.Description(sDescription) = strDescription
```



## <a name="property-value"></a><span data-ttu-id="307af-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="307af-107">Property value</span></span>

<span data-ttu-id="307af-108">la descripción del vínculo.</span><span class="sxs-lookup"><span data-stu-id="307af-108">the link's description.</span></span>

## <a name="examples"></a><span data-ttu-id="307af-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="307af-109">Examples</span></span>

<span data-ttu-id="307af-110">En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="307af-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="307af-111">JScript.net</span><span class="sxs-lookup"><span data-stu-id="307af-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectDescriptionJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var szDescription;
                    
                    // Get the description for the ShellLinkObject.
                    szDescription = objShellLink.Description;
                    alert(szDescription);
                    
                    // Set the description for the ShellLinkObject.
                    objShellLink.Description = "Test"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="307af-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="307af-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectDescriptionVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim szDescription
                                
                                'Get the description for the ShellLinkObject.
                                szDescription = objShellLink.Description
                                alert(szDescription)
                                
                                'Set the description for the ShellLinkObject.
                                objShellLink.Description = "Test"
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="307af-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="307af-113">Visual Basic:</span></span>


```VB
rivate Sub fnShellLinkObjectDescriptionVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim szDescription As String
                            
                            'Get the description for the ShellLinkObject.
                            szDescription = objShellLink.Description
                            Debug.Print szDescription
                            
                            'Set the description for the ShellLinkObject.
                            objShellLink.Description = "Test"
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="307af-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="307af-114">Requirements</span></span>



| <span data-ttu-id="307af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="307af-115">Requirement</span></span> | <span data-ttu-id="307af-116">Value</span><span class="sxs-lookup"><span data-stu-id="307af-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307af-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="307af-117">Minimum supported client</span></span><br/> | <span data-ttu-id="307af-118">Solo para aplicaciones de escritorio de Windows 2000 Professional con SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="307af-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="307af-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="307af-119">Minimum supported server</span></span><br/> | <span data-ttu-id="307af-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="307af-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="307af-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="307af-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="307af-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="307af-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="307af-123">IDL</span><span class="sxs-lookup"><span data-stu-id="307af-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="307af-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="307af-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="307af-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="307af-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="307af-126"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="307af-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




