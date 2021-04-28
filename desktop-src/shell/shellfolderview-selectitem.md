---
description: 'Método ShellFolderView.SelectItem: establece el estado de selección de un elemento en la vista.'
title: Método ShellFolderView.SelectItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116753"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="1e116-103">Método ShellFolderView.SelectItem</span><span class="sxs-lookup"><span data-stu-id="1e116-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="1e116-104">Establece el estado de selección de un elemento en la vista.</span><span class="sxs-lookup"><span data-stu-id="1e116-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e116-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e116-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="1e116-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e116-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e116-107">*vItem* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1e116-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e116-108">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="1e116-108">Type: **Variant\***</span></span>

<span data-ttu-id="1e116-109">Objeto [**FolderItem**](folderitem.md) para el que se establecerá el estado de selección.</span><span class="sxs-lookup"><span data-stu-id="1e116-109">The [**FolderItem**](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="1e116-110">*dwFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="1e116-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e116-111">Tipo: **Entero**</span><span class="sxs-lookup"><span data-stu-id="1e116-111">Type: **Integer**</span></span>

<span data-ttu-id="1e116-112">Conjunto de marcas que indican el nuevo estado de selección.</span><span class="sxs-lookup"><span data-stu-id="1e116-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="1e116-113">Puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1e116-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="1e116-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="1e116-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1e116-115">Anule la selección del elemento.</span><span class="sxs-lookup"><span data-stu-id="1e116-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1e116-116">(1)</span><span class="sxs-lookup"><span data-stu-id="1e116-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1e116-117">Seleccione el elemento.</span><span class="sxs-lookup"><span data-stu-id="1e116-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1e116-118">(3)</span><span class="sxs-lookup"><span data-stu-id="1e116-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1e116-119">Coloque el elemento en modo de edición.</span><span class="sxs-lookup"><span data-stu-id="1e116-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="1e116-120">(4)</span><span class="sxs-lookup"><span data-stu-id="1e116-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1e116-121">Anule la selección de todos los elementos menos el especificado.</span><span class="sxs-lookup"><span data-stu-id="1e116-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="1e116-122">(8)</span><span class="sxs-lookup"><span data-stu-id="1e116-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1e116-123">Asegúrese de que el elemento se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="1e116-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="1e116-124">(16)</span><span class="sxs-lookup"><span data-stu-id="1e116-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1e116-125">Dé el foco al elemento.</span><span class="sxs-lookup"><span data-stu-id="1e116-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e116-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e116-126">Return value</span></span>

<span data-ttu-id="1e116-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1e116-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e116-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e116-128">Remarks</span></span>

<span data-ttu-id="1e116-129">Solo se puede llamar a [**FocusedItem**](shellfolderview-focuseditem.md) en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="1e116-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="1e116-130">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="1e116-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="1e116-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1e116-131">Examples</span></span>

<span data-ttu-id="1e116-132">En el ejemplo siguiente se muestra el uso adecuado de este método en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="1e116-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="1e116-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e116-133">Requirements</span></span>



| <span data-ttu-id="1e116-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e116-134">Requirement</span></span> | <span data-ttu-id="1e116-135">Valor</span><span class="sxs-lookup"><span data-stu-id="1e116-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e116-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e116-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1e116-137">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="1e116-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e116-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e116-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1e116-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e116-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e116-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e116-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e116-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1e116-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1e116-142">Idl</span><span class="sxs-lookup"><span data-stu-id="1e116-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e116-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e116-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1e116-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e116-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e116-145"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1e116-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




