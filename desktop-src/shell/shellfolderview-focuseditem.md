---
description: 'Propiedad ShellFolderView.FocusedItem: obtiene un objeto FolderItem que representa el elemento que tiene el foco de entrada.'
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: Propiedad ShellFolderView.FocusedItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4f661f555f1492a3323fa3749a8dffd6f00f411d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104013"
---
# <a name="shellfolderviewfocuseditem-property"></a><span data-ttu-id="dc02e-103">Propiedad ShellFolderView.FocusedItem</span><span class="sxs-lookup"><span data-stu-id="dc02e-103">ShellFolderView.FocusedItem property</span></span>

<span data-ttu-id="dc02e-104">Obtiene un [**objeto FolderItem**](folderitem.md) que representa el elemento que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="dc02e-104">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="dc02e-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dc02e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc02e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc02e-106">Syntax</span></span>


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="dc02e-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="dc02e-107">Property value</span></span>

<span data-ttu-id="dc02e-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de elemento centrado.</span><span class="sxs-lookup"><span data-stu-id="dc02e-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc02e-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dc02e-109">Remarks</span></span>

<span data-ttu-id="dc02e-110">Solo se puede llamar a **FocusedItem** en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="dc02e-110">**FocusedItem** can only be called on the local system.</span></span> <span data-ttu-id="dc02e-111">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="dc02e-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="dc02e-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="dc02e-112">Examples</span></span>

<span data-ttu-id="dc02e-113">En el ejemplo siguiente se muestra el uso adecuado de este método en JScript insertado en HTML.</span><span class="sxs-lookup"><span data-stu-id="dc02e-113">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
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
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="dc02e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc02e-114">Requirements</span></span>



| <span data-ttu-id="dc02e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc02e-115">Requirement</span></span> | <span data-ttu-id="dc02e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dc02e-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc02e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc02e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc02e-118">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="dc02e-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dc02e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc02e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc02e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc02e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dc02e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc02e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc02e-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="dc02e-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="dc02e-123">Idl</span><span class="sxs-lookup"><span data-stu-id="dc02e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc02e-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc02e-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="dc02e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc02e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc02e-126"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="dc02e-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
