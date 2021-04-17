---
title: Método WebViewFolderContents. SelectItem (Shldisp. h)
description: Establece el estado de selección de un elemento en la vista.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Método SelectItem características del entorno heredado de Windows
- Método SelectItem características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredado, método SelectItem
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714538"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="7c396-106">WebViewFolderContents. SelectItem, método</span><span class="sxs-lookup"><span data-stu-id="7c396-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="7c396-107">Establece el estado de selección de un elemento en la vista.</span><span class="sxs-lookup"><span data-stu-id="7c396-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c396-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c396-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="7c396-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c396-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c396-110">*vItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c396-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c396-111">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="7c396-111">Type: \**Variant\** _</span></span>

<span data-ttu-id="7c396-112">El objeto [_ *carpeta* \*](../shell/folderitem.md) para el que se establecerá el estado de selección.</span><span class="sxs-lookup"><span data-stu-id="7c396-112">The [_ *FolderItem*\*](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="7c396-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c396-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c396-114">Tipo: **Integer**</span><span class="sxs-lookup"><span data-stu-id="7c396-114">Type: **Integer**</span></span>

<span data-ttu-id="7c396-115">Un conjunto de marcas que indican el nuevo estado de la selección.</span><span class="sxs-lookup"><span data-stu-id="7c396-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="7c396-116">Puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7c396-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="7c396-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="7c396-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="7c396-118">Anule la selección del elemento.</span><span class="sxs-lookup"><span data-stu-id="7c396-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="7c396-119">(1)</span><span class="sxs-lookup"><span data-stu-id="7c396-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="7c396-120">Seleccione el elemento.</span><span class="sxs-lookup"><span data-stu-id="7c396-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="7c396-121">(3)</span><span class="sxs-lookup"><span data-stu-id="7c396-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="7c396-122">Poner el elemento en modo de edición.</span><span class="sxs-lookup"><span data-stu-id="7c396-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="7c396-123">(4)</span><span class="sxs-lookup"><span data-stu-id="7c396-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="7c396-124">Anule la selección de todos los elementos excepto el especificado.</span><span class="sxs-lookup"><span data-stu-id="7c396-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="7c396-125">(8)</span><span class="sxs-lookup"><span data-stu-id="7c396-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="7c396-126">Asegúrese de que el elemento se muestra en la vista.</span><span class="sxs-lookup"><span data-stu-id="7c396-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="7c396-127">(16)</span><span class="sxs-lookup"><span data-stu-id="7c396-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="7c396-128">Asigne al elemento el foco.</span><span class="sxs-lookup"><span data-stu-id="7c396-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c396-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c396-129">Return value</span></span>

<span data-ttu-id="7c396-130">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7c396-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7c396-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7c396-131">Examples</span></span>

<span data-ttu-id="7c396-132">En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="7c396-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="7c396-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c396-133">Requirements</span></span>



| <span data-ttu-id="7c396-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c396-134">Requirement</span></span> | <span data-ttu-id="7c396-135">Value</span><span class="sxs-lookup"><span data-stu-id="7c396-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c396-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c396-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7c396-137">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7c396-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7c396-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c396-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7c396-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7c396-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c396-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c396-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c396-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c396-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7c396-142">IDL</span><span class="sxs-lookup"><span data-stu-id="7c396-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c396-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c396-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7c396-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c396-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c396-145"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7c396-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

