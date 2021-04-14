---
description: Recupera el objeto carpeta para un elemento especificado de la colección.
ms.assetid: 164f823d-12d9-4950-a881-63837c53760d
title: Método FolderItems. Item (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed670ed4af3882e38faf2699429c3d1c076f3056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984179"
---
# <a name="folderitemsitem-method"></a><span data-ttu-id="08bf9-103">FolderItems. Item (método)</span><span class="sxs-lookup"><span data-stu-id="08bf9-103">FolderItems.Item method</span></span>

<span data-ttu-id="08bf9-104">Recupera el objeto [**carpeta**](folderitem.md) para un elemento especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="08bf9-104">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bf9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08bf9-105">Syntax</span></span>


```JScript
FolderItems.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="08bf9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08bf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08bf9-107">*iIndex* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="08bf9-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="08bf9-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="08bf9-108">Type: **Variant**</span></span>

<span data-ttu-id="08bf9-109">Índice de base cero del elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="08bf9-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="08bf9-110">Este valor debe ser menor que el valor de la propiedad [**Count**](folderitems-count.md) .</span><span class="sxs-lookup"><span data-stu-id="08bf9-110">This value must be less than the value of the [**Count**](folderitems-count.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08bf9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08bf9-111">Return value</span></span>

<span data-ttu-id="08bf9-112">Una referencia de objeto al objeto [**carpeta**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="08bf9-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="08bf9-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="08bf9-113">Examples</span></span>

<span data-ttu-id="08bf9-114">En el ejemplo siguiente se usa **Item** para recuperar el objeto [**carpeta**](folderitem.md) que representa el archivo Notepad.exe que se encuentra en la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="08bf9-114">The following example uses **Item** to retrieve the [**FolderItem**](folderitem.md) object representing the Notepad.exe file found in the Windows folder.</span></span> <span data-ttu-id="08bf9-115">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="08bf9-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="08bf9-116">JScript.net</span><span class="sxs-lookup"><span data-stu-id="08bf9-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var objFolderItem;
                
                objFolderItem = objFolderItems.Item(objFolderItems.Count - 1);
                alert(objFolderItem.Name);
            }
        }
    }
</script>
```



<span data-ttu-id="08bf9-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="08bf9-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsItemVB()
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
                    dim objFolderItem
                    
                    set objFolderItem = objFolderItems.Item
                        if (not objFolderItem is nothing) then
                            alert(objFolderItem.Name)
                        end if
                    set objFolderItem = nothing
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="08bf9-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="08bf9-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsItemVB()
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
                    Dim objFolderItem As FolderItem
                    
                    Set objFolderItem = objFolderItems.Item("NOTEPAD.EXE")
                        If (Not objFolderItem Is Nothing) Then
                            Debug.Print objFolderItem.Path
                        End If
                    Set objFolderItem = Nothing
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="08bf9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08bf9-119">Requirements</span></span>



| <span data-ttu-id="08bf9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bf9-120">Requirement</span></span> | <span data-ttu-id="08bf9-121">Value</span><span class="sxs-lookup"><span data-stu-id="08bf9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08bf9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08bf9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="08bf9-123">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="08bf9-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08bf9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08bf9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="08bf9-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="08bf9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08bf9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08bf9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="08bf9-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="08bf9-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="08bf9-128">IDL</span><span class="sxs-lookup"><span data-stu-id="08bf9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08bf9-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08bf9-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="08bf9-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08bf9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08bf9-131"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="08bf9-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08bf9-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="08bf9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bf9-133">**FolderItems**</span><span class="sxs-lookup"><span data-stu-id="08bf9-133">**FolderItems**</span></span>](folderitems.md)
</dt> </dl>

 

 




