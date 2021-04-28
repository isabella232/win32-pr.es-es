---
title: Propiedad WebViewFolderContents.Folder (Shldisp.h)
description: 'Propiedad WebViewFolderContents.Folder: obtiene un objeto Folder que representa la vista.'
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Propiedades de carpeta Características heredadas del entorno de Windows
- Propiedad de carpeta Características heredadas del entorno de Windows , Objeto WebViewFolderContents
- Objeto WebViewFolderContents Características heredadas del entorno de Windows, propiedad Carpeta
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102703"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="c7a38-106">Propiedad WebViewFolderContents.Folder</span><span class="sxs-lookup"><span data-stu-id="c7a38-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="c7a38-107">Obtiene un [**objeto Folder**](../shell/folder.md) que representa la vista.</span><span class="sxs-lookup"><span data-stu-id="c7a38-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="c7a38-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c7a38-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a38-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7a38-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="c7a38-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c7a38-110">Property value</span></span>

<span data-ttu-id="c7a38-111">Objeto que recibe el [**objeto Folder.**](../shell/folder.md)</span><span class="sxs-lookup"><span data-stu-id="c7a38-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="c7a38-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7a38-112">Examples</span></span>

<span data-ttu-id="c7a38-113">En el ejemplo siguiente se muestra el uso adecuado de esta propiedad en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="c7a38-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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



## <a name="requirements"></a><span data-ttu-id="c7a38-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7a38-114">Requirements</span></span>



| <span data-ttu-id="c7a38-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7a38-115">Requirement</span></span> | <span data-ttu-id="c7a38-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c7a38-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a38-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7a38-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a38-118">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="c7a38-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c7a38-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7a38-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a38-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c7a38-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c7a38-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7a38-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7a38-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c7a38-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c7a38-123">Idl</span><span class="sxs-lookup"><span data-stu-id="c7a38-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7a38-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7a38-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c7a38-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7a38-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7a38-126"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c7a38-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

