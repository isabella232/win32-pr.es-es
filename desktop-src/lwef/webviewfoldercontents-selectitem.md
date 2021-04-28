---
title: Método WebViewFolderContents.SelectItem (Shldisp.h)
description: 'Método WebViewFolderContents.SelectItem: establece el estado de selección de un elemento en la vista.'
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Características heredadas del entorno de Windows del método SelectItem
- SelectItem method Legacy Windows Environment Features , WebViewFolderContents (Objeto WebViewFolderContents)
- WebViewFolderContents object Legacy Windows Environment Features , SelectItem method (Características heredadas del entorno de Windows del objeto WebViewFolderContents), método SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66e2d05c010199f05826df7ed4591e8c7c1723e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102614"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="85a0f-106">Método WebViewFolderContents.SelectItem</span><span class="sxs-lookup"><span data-stu-id="85a0f-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="85a0f-107">Establece el estado de selección de un elemento en la vista.</span><span class="sxs-lookup"><span data-stu-id="85a0f-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a0f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85a0f-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="85a0f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85a0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a0f-110">*vItem* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="85a0f-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a0f-111">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="85a0f-111">Type: **Variant\***</span></span>

<span data-ttu-id="85a0f-112">Objeto [**FolderItem**](../shell/folderitem.md) para el que se establecerá el estado de selección.</span><span class="sxs-lookup"><span data-stu-id="85a0f-112">The [**FolderItem**](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="85a0f-113">*dwFlags* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="85a0f-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a0f-114">Tipo: **Entero**</span><span class="sxs-lookup"><span data-stu-id="85a0f-114">Type: **Integer**</span></span>

<span data-ttu-id="85a0f-115">Conjunto de marcas que indican el nuevo estado de selección.</span><span class="sxs-lookup"><span data-stu-id="85a0f-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="85a0f-116">Puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="85a0f-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="85a0f-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="85a0f-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="85a0f-118">Anule la selección del elemento.</span><span class="sxs-lookup"><span data-stu-id="85a0f-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="85a0f-119">(1)</span><span class="sxs-lookup"><span data-stu-id="85a0f-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="85a0f-120">Seleccione el elemento.</span><span class="sxs-lookup"><span data-stu-id="85a0f-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="85a0f-121">(3)</span><span class="sxs-lookup"><span data-stu-id="85a0f-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="85a0f-122">Coloque el elemento en modo de edición.</span><span class="sxs-lookup"><span data-stu-id="85a0f-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="85a0f-123">(4)</span><span class="sxs-lookup"><span data-stu-id="85a0f-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="85a0f-124">Anule la selección de todos los elementos menos el especificado.</span><span class="sxs-lookup"><span data-stu-id="85a0f-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="85a0f-125">(8)</span><span class="sxs-lookup"><span data-stu-id="85a0f-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="85a0f-126">Asegúrese de que el elemento se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="85a0f-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="85a0f-127">(16)</span><span class="sxs-lookup"><span data-stu-id="85a0f-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="85a0f-128">Dé el foco al elemento.</span><span class="sxs-lookup"><span data-stu-id="85a0f-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a0f-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85a0f-129">Return value</span></span>

<span data-ttu-id="85a0f-130">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="85a0f-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="85a0f-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="85a0f-131">Examples</span></span>

<span data-ttu-id="85a0f-132">En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML.</span><span class="sxs-lookup"><span data-stu-id="85a0f-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="85a0f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85a0f-133">Requirements</span></span>



| <span data-ttu-id="85a0f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="85a0f-134">Requirement</span></span> | <span data-ttu-id="85a0f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="85a0f-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85a0f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85a0f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="85a0f-137">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="85a0f-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="85a0f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85a0f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="85a0f-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="85a0f-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="85a0f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85a0f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="85a0f-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="85a0f-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="85a0f-142">Idl</span><span class="sxs-lookup"><span data-stu-id="85a0f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85a0f-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="85a0f-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="85a0f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85a0f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85a0f-145"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="85a0f-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

