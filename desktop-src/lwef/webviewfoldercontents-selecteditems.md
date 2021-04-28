---
title: Método WebViewFolderContents.SelectedItems (Shldisp.h)
description: 'Método WebViewFolderContents.SelectedItems: obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.'
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Características heredadas del entorno de Windows del método SelectedItems
- SelectedItems method Legacy Windows Environment Features , WebViewFolderContents (Objeto WebViewFolderContents)
- WebViewFolderContents object Legacy Windows Environment Features , SelectedItems method
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
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102653"
---
# <a name="webviewfoldercontentsselecteditems-method"></a><span data-ttu-id="00a0b-106">Método WebViewFolderContents.SelectedItems</span><span class="sxs-lookup"><span data-stu-id="00a0b-106">WebViewFolderContents.SelectedItems method</span></span>

<span data-ttu-id="00a0b-107">Obtiene un [**objeto FolderItems**](../shell/folderitems.md) que representa todos los elementos seleccionados en la vista.</span><span class="sxs-lookup"><span data-stu-id="00a0b-107">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a0b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00a0b-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a><span data-ttu-id="00a0b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00a0b-109">Parameters</span></span>

<span data-ttu-id="00a0b-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="00a0b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="00a0b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00a0b-111">Return value</span></span>

<span data-ttu-id="00a0b-112">Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="00a0b-112">Type: **[**FolderItems**](../shell/folderitems.md)\*\***</span></span>

<span data-ttu-id="00a0b-113">Referencia de objeto al [**objeto FolderItems.**](../shell/folderitems.md)</span><span class="sxs-lookup"><span data-stu-id="00a0b-113">An object reference to the [**FolderItems**](../shell/folderitems.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="00a0b-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="00a0b-114">Examples</span></span>

<span data-ttu-id="00a0b-115">En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML.</span><span class="sxs-lookup"><span data-stu-id="00a0b-115">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="00a0b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a0b-116">Requirements</span></span>



| <span data-ttu-id="00a0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a0b-117">Requirement</span></span> | <span data-ttu-id="00a0b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="00a0b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a0b-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00a0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00a0b-120">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="00a0b-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="00a0b-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00a0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00a0b-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00a0b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="00a0b-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00a0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a0b-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="00a0b-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="00a0b-125">Idl</span><span class="sxs-lookup"><span data-stu-id="00a0b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="00a0b-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="00a0b-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="00a0b-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00a0b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00a0b-128"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="00a0b-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

