---
description: Contiene el número de elementos de la colección.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Propiedad FolderItemVerbs. Count (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b41e78261dfc9bc72e9262615bc395a9d559e33a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997728"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="dfb2e-103">FolderItemVerbs. Count (propiedad)</span><span class="sxs-lookup"><span data-stu-id="dfb2e-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="dfb2e-104">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="dfb2e-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="dfb2e-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dfb2e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb2e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfb2e-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="dfb2e-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dfb2e-107">Property value</span></span>

<span data-ttu-id="dfb2e-108">**Entero** que recibe la propiedad de **recuento** .</span><span class="sxs-lookup"><span data-stu-id="dfb2e-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="dfb2e-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dfb2e-109">Examples</span></span>

<span data-ttu-id="dfb2e-110">En el ejemplo siguiente se usa **Count** para recuperar el recuento de verbos disponibles para la carpeta del panel de control.</span><span class="sxs-lookup"><span data-stu-id="dfb2e-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="dfb2e-111">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dfb2e-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dfb2e-112">JScript.net</span><span class="sxs-lookup"><span data-stu-id="dfb2e-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="dfb2e-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="dfb2e-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="dfb2e-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dfb2e-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dfb2e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb2e-115">Requirements</span></span>



| <span data-ttu-id="dfb2e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb2e-116">Requirement</span></span> | <span data-ttu-id="dfb2e-117">Value</span><span class="sxs-lookup"><span data-stu-id="dfb2e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb2e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfb2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb2e-119">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="dfb2e-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dfb2e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfb2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb2e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfb2e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dfb2e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfb2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfb2e-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb2e-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dfb2e-124">IDL</span><span class="sxs-lookup"><span data-stu-id="dfb2e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfb2e-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfb2e-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dfb2e-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dfb2e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb2e-127"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dfb2e-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




