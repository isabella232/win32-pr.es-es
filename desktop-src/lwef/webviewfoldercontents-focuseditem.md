---
title: Propiedad WebViewFolderContents.FocusedItem (Shldisp.h)
description: 'Propiedad WebViewFolderContents.FocusedItem: obtiene un objeto FolderItem que representa el elemento que tiene el foco de entrada.'
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Características heredadas del entorno de Windows de la propiedad FocusedItem
- Objeto WebViewFolderContents de características heredadas del entorno de Windows de la propiedad FocusedItem
- Objeto WebViewFolderContents Características heredadas del entorno de Windows, propiedad FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102733"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a><span data-ttu-id="d35a4-106">Propiedad WebViewFolderContents.FocusedItem</span><span class="sxs-lookup"><span data-stu-id="d35a4-106">WebViewFolderContents.FocusedItem property</span></span>

<span data-ttu-id="d35a4-107">Obtiene un [**objeto FolderItem**](../shell/folderitem.md) que representa el elemento que tiene el foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="d35a4-107">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span>

<span data-ttu-id="d35a4-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d35a4-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d35a4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d35a4-109">Syntax</span></span>


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a><span data-ttu-id="d35a4-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d35a4-110">Property value</span></span>

<span data-ttu-id="d35a4-111">Variable de tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de elemento centrado.</span><span class="sxs-lookup"><span data-stu-id="d35a4-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the focused item object.</span></span>

## <a name="examples"></a><span data-ttu-id="d35a4-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d35a4-112">Examples</span></span>

<span data-ttu-id="d35a4-113">En el ejemplo siguiente se muestra el uso adecuado de esta propiedad en JScript insertado en HTML.</span><span class="sxs-lookup"><span data-stu-id="d35a4-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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



## <a name="requirements"></a><span data-ttu-id="d35a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35a4-114">Requirements</span></span>



| <span data-ttu-id="d35a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35a4-115">Requirement</span></span> | <span data-ttu-id="d35a4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d35a4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35a4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d35a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d35a4-118">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="d35a4-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d35a4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d35a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d35a4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d35a4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d35a4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d35a4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35a4-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d35a4-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d35a4-123">Idl</span><span class="sxs-lookup"><span data-stu-id="d35a4-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d35a4-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="d35a4-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d35a4-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d35a4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d35a4-126"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d35a4-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

