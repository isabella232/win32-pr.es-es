---
description: 'Método ShellFolderView.SelectedItems: obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.'
title: Método ShellFolderView.SelectedItems (Shldisp.h)
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
ms.openlocfilehash: 485eda530adc4955abb27899d67ac0900eb0a910
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840746"
---
# <a name="shellfolderviewselecteditems-method"></a><span data-ttu-id="2bb45-103">Método ShellFolderView.SelectedItems</span><span class="sxs-lookup"><span data-stu-id="2bb45-103">ShellFolderView.SelectedItems method</span></span>

<span data-ttu-id="2bb45-104">Obtiene un [**objeto FolderItems**](folderitems.md) que representa todos los elementos seleccionados en la vista.</span><span class="sxs-lookup"><span data-stu-id="2bb45-104">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bb45-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="2bb45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bb45-106">Parameters</span></span>

<span data-ttu-id="2bb45-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2bb45-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2bb45-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2bb45-108">Return value</span></span>

<span data-ttu-id="2bb45-109">Tipo: **[ **FolderItems**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2bb45-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="2bb45-110">Referencia de objeto al [**objeto FolderItems.**](folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="2bb45-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bb45-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bb45-111">Remarks</span></span>

<span data-ttu-id="2bb45-112">Solo se puede llamar a **SelectedItems** en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="2bb45-112">**SelectedItems** can only be called on the local system.</span></span> <span data-ttu-id="2bb45-113">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="2bb45-113">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="2bb45-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2bb45-114">Examples</span></span>

<span data-ttu-id="2bb45-115">En el ejemplo siguiente se muestra el uso adecuado de este método en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="2bb45-115">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2bb45-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bb45-116">Requirements</span></span>



| <span data-ttu-id="2bb45-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bb45-117">Requirement</span></span> | <span data-ttu-id="2bb45-118">Value</span><span class="sxs-lookup"><span data-stu-id="2bb45-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb45-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb45-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb45-120">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="2bb45-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2bb45-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb45-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb45-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2bb45-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2bb45-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bb45-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bb45-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="2bb45-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2bb45-125">Idl</span><span class="sxs-lookup"><span data-stu-id="2bb45-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bb45-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bb45-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2bb45-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bb45-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bb45-128"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2bb45-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




