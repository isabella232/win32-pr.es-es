---
description: Busca el destino de un vínculo de Shell, incluso si el destino se ha quitado o cambiado de nombre.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Método ShellLinkObject. Resolve (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b1cb0760f1ee19acfa10208711e73919fd084ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986059"
---
# <a name="shelllinkobjectresolve-method"></a><span data-ttu-id="4c11b-103">ShellLinkObject. Resolve (método)</span><span class="sxs-lookup"><span data-stu-id="4c11b-103">ShellLinkObject.Resolve method</span></span>

<span data-ttu-id="4c11b-104">Busca el destino de un vínculo de Shell, incluso si el destino se ha quitado o cambiado de nombre.</span><span class="sxs-lookup"><span data-stu-id="4c11b-104">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c11b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c11b-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a><span data-ttu-id="4c11b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c11b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c11b-107">*fFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c11b-107">*fFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c11b-108">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="4c11b-108">Type: **Integer**</span></span>

<span data-ttu-id="4c11b-109">Marcas que especifican la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="4c11b-109">Flags that specify the action to be taken.</span></span> <span data-ttu-id="4c11b-110">Puede ser una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="4c11b-110">This can be a combination of the following values:</span></span>

<dt>



 <span data-ttu-id="4c11b-111">(1)</span><span class="sxs-lookup"><span data-stu-id="4c11b-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-112">No muestre un cuadro de diálogo si no se puede resolver el vínculo.</span><span class="sxs-lookup"><span data-stu-id="4c11b-112">Do not display a dialog box if the link cannot be resolved.</span></span> <span data-ttu-id="4c11b-113">Cuando se establece esta marca, la palabra de orden superior de *fFlags* especifica una duración de tiempo de espera, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="4c11b-113">When this flag is set, the high-order word of *fFlags* specifies a time-out duration, in milliseconds.</span></span> <span data-ttu-id="4c11b-114">El método devuelve si no se puede resolver el vínculo dentro de la duración del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="4c11b-114">The method returns if the link cannot be resolved within the time-out duration.</span></span> <span data-ttu-id="4c11b-115">Si la palabra de orden superior se establece en cero, la duración de tiempo de espera predeterminada es de 3000 milisegundos (3 segundos).</span><span class="sxs-lookup"><span data-stu-id="4c11b-115">If the high-order word is set to zero, the time-out duration defaults to 3000 milliseconds (3 seconds).</span></span>

</dd> <dt>



 <span data-ttu-id="4c11b-116">(4)</span><span class="sxs-lookup"><span data-stu-id="4c11b-116">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-117">Si el vínculo ha cambiado, actualice su ruta de acceso y la lista de identificadores.</span><span class="sxs-lookup"><span data-stu-id="4c11b-117">If the link has changed, update its path and list of identifiers.</span></span>

</dd> <dt>



 <span data-ttu-id="4c11b-118">(8)</span><span class="sxs-lookup"><span data-stu-id="4c11b-118">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-119">No actualice la información del vínculo.</span><span class="sxs-lookup"><span data-stu-id="4c11b-119">Do not update the link information.</span></span>

</dd> <dt>



 <span data-ttu-id="4c11b-120">(16)</span><span class="sxs-lookup"><span data-stu-id="4c11b-120">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-121">No ejecute la heurística de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4c11b-121">Do not execute the search heuristics.</span></span>

</dd> <dt>



 <span data-ttu-id="4c11b-122">(32)</span><span class="sxs-lookup"><span data-stu-id="4c11b-122">(32)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-123">No utilice el seguimiento de vínculos distribuidos.</span><span class="sxs-lookup"><span data-stu-id="4c11b-123">Do not use distributed link tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="4c11b-124">(64)</span><span class="sxs-lookup"><span data-stu-id="4c11b-124">(64)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-125">Deshabilite el seguimiento de vínculos distribuidos.</span><span class="sxs-lookup"><span data-stu-id="4c11b-125">Disable distributed link tracking.</span></span> <span data-ttu-id="4c11b-126">De forma predeterminada, el seguimiento de vínculos distribuidos realiza un seguimiento de los medios extraíbles en varios dispositivos según el nombre del volumen.</span><span class="sxs-lookup"><span data-stu-id="4c11b-126">By default, distributed link tracking tracks removable media across multiple devices based on the volume name.</span></span> <span data-ttu-id="4c11b-127">También utiliza la ruta de acceso UNC para realizar el seguimiento de los sistemas de archivos remotos cuya letra de unidad ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="4c11b-127">It also uses the UNC path to track remote file systems whose drive letter has changed.</span></span> <span data-ttu-id="4c11b-128">Al establecer esta marca, se deshabilitan ambos tipos de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="4c11b-128">Setting this flag disables both types of tracking.</span></span>

</dd> <dt>



 <span data-ttu-id="4c11b-129">(128)</span><span class="sxs-lookup"><span data-stu-id="4c11b-129">(128)</span></span>


</dt> <dd>

<span data-ttu-id="4c11b-130">Llame al Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4c11b-130">Call the Windows Installer.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c11b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c11b-131">Remarks</span></span>

<span data-ttu-id="4c11b-132">Este método es esencialmente idéntico en la funcionalidad que se va a [**resolver**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span><span class="sxs-lookup"><span data-stu-id="4c11b-132">This method is essentially identical in functionality to [**Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span> <span data-ttu-id="4c11b-133">Para obtener más información sobre la resolución de vínculos, vea la sección Comentarios de esa página.</span><span class="sxs-lookup"><span data-stu-id="4c11b-133">For further discussion of link resolution, see the Remarks section of that page.</span></span>

## <a name="examples"></a><span data-ttu-id="4c11b-134">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c11b-134">Examples</span></span>

<span data-ttu-id="4c11b-135">En el ejemplo siguiente se muestra el uso correcto de este método para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4c11b-135">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4c11b-136">JScript.net</span><span class="sxs-lookup"><span data-stu-id="4c11b-136">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
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
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="4c11b-137">VBScript</span><span class="sxs-lookup"><span data-stu-id="4c11b-137">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
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
                                objShellLink.Resolve(1)
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



<span data-ttu-id="4c11b-138">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4c11b-138">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectResolveVB()
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
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4c11b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c11b-139">Requirements</span></span>



| <span data-ttu-id="4c11b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c11b-140">Requirement</span></span> | <span data-ttu-id="4c11b-141">Value</span><span class="sxs-lookup"><span data-stu-id="4c11b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c11b-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c11b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4c11b-143">Solo para aplicaciones de escritorio de Windows 2000 Professional con SP3 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c11b-143">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4c11b-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c11b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4c11b-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4c11b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4c11b-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c11b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c11b-147"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c11b-147"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4c11b-148">IDL</span><span class="sxs-lookup"><span data-stu-id="4c11b-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c11b-149"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c11b-149"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4c11b-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c11b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c11b-151"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4c11b-151"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
