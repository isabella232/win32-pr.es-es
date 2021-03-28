---
description: Obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.
title: Método ShellFolderView. SelectedItems (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: c6ade3a6e25d5de6bfa1661207473dac72ace2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997868"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="a73f3-103">ShellFolderView. SelectedItems (método)</span><span class="sxs-lookup"><span data-stu-id="a73f3-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="a73f3-104">Obtiene un objeto [**FolderItems**](folderitems.md) que representa todos los elementos seleccionados en la vista.</span><span class="sxs-lookup"><span data-stu-id="a73f3-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73f3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a73f3-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="a73f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a73f3-106">Parameters</span></span>

<span data-ttu-id="a73f3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a73f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a73f3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a73f3-108">Return value</span></span>

<span data-ttu-id="a73f3-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a73f3-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="a73f3-110">Una referencia de objeto al objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="a73f3-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a73f3-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a73f3-111">Remarks</span></span>

<span data-ttu-id="a73f3-112">Solo se puede llamar a **SelectedItems** en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="a73f3-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="a73f3-113">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="a73f3-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="a73f3-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a73f3-114">Examples</span></span>

<span data-ttu-id="a73f3-115">En el ejemplo siguiente se muestra el uso correcto de este método en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="a73f3-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="a73f3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73f3-116">Requirements</span></span>



| <span data-ttu-id="a73f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73f3-117">Requirement</span></span> | <span data-ttu-id="a73f3-118">Value</span><span class="sxs-lookup"><span data-stu-id="a73f3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73f3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a73f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a73f3-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a73f3-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a73f3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a73f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a73f3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a73f3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a73f3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a73f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a73f3-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73f3-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a73f3-125">IDL</span><span class="sxs-lookup"><span data-stu-id="a73f3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a73f3-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a73f3-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a73f3-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a73f3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a73f3-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="a73f3-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




