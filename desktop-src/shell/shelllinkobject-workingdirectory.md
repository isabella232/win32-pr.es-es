---
description: Obtiene o establece el directorio de trabajo especificado en el vínculo.
ms.assetid: c3820deb-9f00-42a9-ab0e-c0f6389e9f29
title: Propiedad ShellLinkObject. WorkingDirectory (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.WorkingDirectory
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d8788899a06179056cd871b68e4e64566bcd5ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360824"
---
# <a name="shelllinkobjectworkingdirectory-property"></a><span data-ttu-id="8a15d-103">Propiedad ShellLinkObject. WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="8a15d-103">ShellLinkObject.WorkingDirectory property</span></span>

<span data-ttu-id="8a15d-104">Obtiene o establece el directorio de trabajo especificado en el vínculo.</span><span class="sxs-lookup"><span data-stu-id="8a15d-104">Gets or sets the working directory specified in the link.</span></span>

<span data-ttu-id="8a15d-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8a15d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a15d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a15d-106">Syntax</span></span>


```JScript
strWorkingDirectory = ShellLinkObject.WorkingDirectory
ShellLinkObject.WorkingDirectory(sWorkingDirectory) = strWorkingDirectory
```



## <a name="property-value"></a><span data-ttu-id="8a15d-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8a15d-107">Property value</span></span>

<span data-ttu-id="8a15d-108">Ruta de acceso completa del directorio de trabajo del vínculo.</span><span class="sxs-lookup"><span data-stu-id="8a15d-108">the fully qualified path of the link's working directory.</span></span>

## <a name="examples"></a><span data-ttu-id="8a15d-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8a15d-109">Examples</span></span>

<span data-ttu-id="8a15d-110">En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8a15d-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8a15d-111">JScript.net</span><span class="sxs-lookup"><span data-stu-id="8a15d-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectWorkingDirectoryJ()
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
                    var szDirectory;
                    
                    // Get the working directory for the ShellLinkObject.
                    szDirectory = objShellLink.WorkingDirectory;
                    alert(szDirectory);
                    
                    // Set the working directory for the ShellLinkObject.
                    objShellLink.WorkingDirectory = "";
                }
            }
        }
    }
</script>
```



<span data-ttu-id="8a15d-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="8a15d-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectWorkingDirectoryVB()
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
                                dim szDirectory
                                
                                'Get the working directory.
                                szDirectory = objShellLink.WorkingDirectory
                                alert(szDirectory)
                                
                                'Set the working directory.
                                objShellLink.WorkingDirectory = ""
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



<span data-ttu-id="8a15d-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8a15d-113">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectWorkingDirectoryVB()
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
                            Dim szDirectory As String
                            
                            'Get the working directory.
                            szDirectory = objShellLink.WorkingDirectory
                            Debug.Print szDirectory
                            
                            'Set the working directory.
                            objShellLink.WorkingDirectory = ""
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="8a15d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a15d-114">Requirements</span></span>



| <span data-ttu-id="8a15d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a15d-115">Requirement</span></span> | <span data-ttu-id="8a15d-116">Value</span><span class="sxs-lookup"><span data-stu-id="8a15d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a15d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a15d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8a15d-118">Solo para aplicaciones de escritorio de Windows 2000 Professional con SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a15d-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8a15d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a15d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8a15d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a15d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8a15d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a15d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a15d-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a15d-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8a15d-123">IDL</span><span class="sxs-lookup"><span data-stu-id="8a15d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a15d-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a15d-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8a15d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a15d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a15d-126"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8a15d-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




