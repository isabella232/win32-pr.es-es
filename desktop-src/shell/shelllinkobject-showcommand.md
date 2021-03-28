---
description: Obtiene o establece el estado de presentación inicial (con tamaño, minimizada o maximizada) del comando del vínculo.
ms.assetid: 139c6924-f554-4fde-9ed0-bc117bafbb16
title: Propiedad ShellLinkObject. información showcommand (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.ShowCommand
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9bacdf98a24d749b5128bc286f06e99299aef437
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997949"
---
# <a name="shelllinkobjectshowcommand-property"></a><span data-ttu-id="7d637-103">Propiedad ShellLinkObject. información showcommand</span><span class="sxs-lookup"><span data-stu-id="7d637-103">ShellLinkObject.ShowCommand property</span></span>

<span data-ttu-id="7d637-104">Obtiene o establece el estado de presentación inicial (con tamaño, minimizada o maximizada) del comando del vínculo.</span><span class="sxs-lookup"><span data-stu-id="7d637-104">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span>

<span data-ttu-id="7d637-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7d637-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d637-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d637-106">Syntax</span></span>


```JScript
iShowCommand = ShellLinkObject.ShowCommand
ShellLinkObject.ShowCommand(intShowCommand) = iShowCommand
```



## <a name="property-value"></a><span data-ttu-id="7d637-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7d637-107">Property value</span></span>

<span data-ttu-id="7d637-108">Estado de visualización del vínculo.</span><span class="sxs-lookup"><span data-stu-id="7d637-108">the link's display state.</span></span> <span data-ttu-id="7d637-109">Puede ser uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="7d637-109">This can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="7d637-110">(1)</span><span class="sxs-lookup"><span data-stu-id="7d637-110">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7d637-111">Activa y muestra una ventana.</span><span class="sxs-lookup"><span data-stu-id="7d637-111">Activates and displays a window.</span></span> <span data-ttu-id="7d637-112">Si la ventana está minimizada o maximizada, el sistema la restaura a su tamaño y posición originales.</span><span class="sxs-lookup"><span data-stu-id="7d637-112">If the window is minimized or maximized, the system restores it to its original size and position.</span></span>

</dd> <dt>



 <span data-ttu-id="7d637-113">(2)</span><span class="sxs-lookup"><span data-stu-id="7d637-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="7d637-114">Activa la ventana y la muestra como una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="7d637-114">Activates the window and displays it as a minimized window.</span></span>

</dd> <dt>



 <span data-ttu-id="7d637-115">(3)</span><span class="sxs-lookup"><span data-stu-id="7d637-115">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7d637-116">Activa la ventana y la muestra como una ventana maximizada.</span><span class="sxs-lookup"><span data-stu-id="7d637-116">Activates the window and displays it as a maximized window.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7d637-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7d637-117">Examples</span></span>

<span data-ttu-id="7d637-118">En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7d637-118">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7d637-119">JScript.net</span><span class="sxs-lookup"><span data-stu-id="7d637-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectShowCommandJ()
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
                    var nShow;
                    
                    // Get the ShowCommand for the ShellLinkObject.
                    nShow = objShellLink.ShowCommand;
                    alert(nShow);
                    
                    // Set the ShowCommand for the ShellLinkObject.
                    objShellLink.ShowCommand = 1
                }
            }
        }
    }
</script>
```



<span data-ttu-id="7d637-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="7d637-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectShowCommandVB()
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
                                dim nShow
                                
                                'Get the ShowCommand for the ShellLinkObject.
                                nShow = objShellLink.ShowCommand
                                alert(nShow)
                                
                                'Set the ShowCommand for the ShellLinkObject.
                                objShellLink.ShowCommand = 1
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



<span data-ttu-id="7d637-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7d637-121">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectShowCommandVB()
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
                            Dim nShow As Integer
                            
                            'Get the ShowCommand for the ShellLinkObject.
                            nShow = objShellLink.ShowCommand
                            Debug.Print nShow
                            
                            'Set the ShowCommand for the ShellLinkObject.
                            objShellLink.ShowCommand = 1
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7d637-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d637-122">Requirements</span></span>



| <span data-ttu-id="7d637-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d637-123">Requirement</span></span> | <span data-ttu-id="7d637-124">Value</span><span class="sxs-lookup"><span data-stu-id="7d637-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d637-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d637-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7d637-126">Solo para aplicaciones de escritorio de Windows 2000 Professional con SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d637-126">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d637-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d637-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7d637-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7d637-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7d637-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7d637-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d637-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d637-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7d637-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7d637-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7d637-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7d637-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7d637-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d637-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d637-134"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7d637-134"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




