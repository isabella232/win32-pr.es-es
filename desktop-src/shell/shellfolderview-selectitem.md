---
description: Establece el estado de selección de un elemento en la vista.
title: Método ShellFolderView. SelectItem (Shldisp. h)
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
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278496"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="4d280-103">ShellFolderView. SelectItem, método</span><span class="sxs-lookup"><span data-stu-id="4d280-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="4d280-104">Establece el estado de selección de un elemento en la vista.</span><span class="sxs-lookup"><span data-stu-id="4d280-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d280-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d280-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="4d280-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d280-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d280-107">*vItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d280-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d280-108">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="4d280-108">Type: \**Variant\** _</span></span>

<span data-ttu-id="4d280-109">El objeto [_ *carpeta* \*](folderitem.md) para el que se establecerá el estado de selección.</span><span class="sxs-lookup"><span data-stu-id="4d280-109">The [_ *FolderItem*\*](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="4d280-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d280-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d280-111">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="4d280-111">Type: **Integer**</span></span>

<span data-ttu-id="4d280-112">Un conjunto de marcas que indican el nuevo estado de la selección.</span><span class="sxs-lookup"><span data-stu-id="4d280-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="4d280-113">Puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4d280-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="4d280-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="4d280-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4d280-115">Anule la selección del elemento.</span><span class="sxs-lookup"><span data-stu-id="4d280-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="4d280-116">(1)</span><span class="sxs-lookup"><span data-stu-id="4d280-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4d280-117">Seleccione el elemento.</span><span class="sxs-lookup"><span data-stu-id="4d280-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="4d280-118">(3)</span><span class="sxs-lookup"><span data-stu-id="4d280-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4d280-119">Poner el elemento en modo de edición.</span><span class="sxs-lookup"><span data-stu-id="4d280-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="4d280-120">(4)</span><span class="sxs-lookup"><span data-stu-id="4d280-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4d280-121">Anule la selección de todos los elementos excepto el especificado.</span><span class="sxs-lookup"><span data-stu-id="4d280-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="4d280-122">(8)</span><span class="sxs-lookup"><span data-stu-id="4d280-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4d280-123">Asegúrese de que el elemento se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="4d280-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="4d280-124">(16)</span><span class="sxs-lookup"><span data-stu-id="4d280-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4d280-125">Asigne al elemento el foco.</span><span class="sxs-lookup"><span data-stu-id="4d280-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d280-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d280-126">Return value</span></span>

<span data-ttu-id="4d280-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4d280-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d280-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d280-128">Remarks</span></span>

<span data-ttu-id="4d280-129">Solo se puede llamar a [**FocusedItem**](shellfolderview-focuseditem.md) en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="4d280-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="4d280-130">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="4d280-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="4d280-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d280-131">Examples</span></span>

<span data-ttu-id="4d280-132">En el ejemplo siguiente se muestra el uso correcto de este método en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="4d280-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4d280-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d280-133">Requirements</span></span>



| <span data-ttu-id="4d280-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d280-134">Requirement</span></span> | <span data-ttu-id="4d280-135">Value</span><span class="sxs-lookup"><span data-stu-id="4d280-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d280-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d280-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4d280-137">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4d280-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4d280-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d280-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4d280-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4d280-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4d280-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d280-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d280-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d280-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4d280-142">IDL</span><span class="sxs-lookup"><span data-stu-id="4d280-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4d280-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4d280-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4d280-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d280-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d280-145"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4d280-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




