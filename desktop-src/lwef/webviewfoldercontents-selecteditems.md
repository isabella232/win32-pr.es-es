---
title: Método WebViewFolderContents.SelectedItems (Shldisp.h)
description: Obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Método SelectedItems características del entorno heredado de Windows
- Método SelectedItems herencia de características de entorno de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredadas, método SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079681"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="bee6d-106">WebViewFolderContents. SelectedItems (método)</span><span class="sxs-lookup"><span data-stu-id="bee6d-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="bee6d-107">Obtiene un objeto [**FolderItems**](../shell/folderitems.md) que representa todos los elementos seleccionados en la vista.</span><span class="sxs-lookup"><span data-stu-id="bee6d-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="bee6d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bee6d-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="bee6d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bee6d-109">Parameters</span></span>

<span data-ttu-id="bee6d-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bee6d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bee6d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bee6d-111">Return value</span></span>

<span data-ttu-id="bee6d-112">Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bee6d-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="bee6d-113">Una referencia de objeto al objeto [**FolderItems**](../shell/folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="bee6d-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="bee6d-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bee6d-114">Examples</span></span>

<span data-ttu-id="bee6d-115">En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="bee6d-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



## <a name="requirements"></a><span data-ttu-id="bee6d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bee6d-116">Requirements</span></span>



| <span data-ttu-id="bee6d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bee6d-117">Requirement</span></span> | <span data-ttu-id="bee6d-118">Value</span><span class="sxs-lookup"><span data-stu-id="bee6d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bee6d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bee6d-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bee6d-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bee6d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bee6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bee6d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bee6d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bee6d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bee6d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bee6d-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bee6d-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bee6d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="bee6d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bee6d-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bee6d-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bee6d-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bee6d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bee6d-128"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bee6d-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

