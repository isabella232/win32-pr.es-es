---
title: Propiedad WebViewFolderContents.Folder (Shldisp.h)
description: Obtiene un objeto de carpeta que representa la vista.
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Propiedades de carpeta características de entorno heredado de Windows
- Propiedades de carpeta características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredadas, propiedad de carpeta
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
ms.openlocfilehash: 4c0640d4e29b903b32a6c9ed1e0b1de9f458b132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489316"
---
# <a name="webviewfoldercontentsfolder-property"></a><span data-ttu-id="5655c-106">Propiedad WebViewFolderContents. Folder</span><span class="sxs-lookup"><span data-stu-id="5655c-106">WebViewFolderContents.Folder property</span></span>

<span data-ttu-id="5655c-107">Obtiene un objeto de [**carpeta**](../shell/folder.md) que representa la vista.</span><span class="sxs-lookup"><span data-stu-id="5655c-107">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span>

<span data-ttu-id="5655c-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5655c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5655c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5655c-109">Syntax</span></span>


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a><span data-ttu-id="5655c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5655c-110">Property value</span></span>

<span data-ttu-id="5655c-111">Objeto que recibe el objeto de [**carpeta**](../shell/folder.md) .</span><span class="sxs-lookup"><span data-stu-id="5655c-111">An object that receives the [**Folder**](../shell/folder.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="5655c-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5655c-112">Examples</span></span>

<span data-ttu-id="5655c-113">En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="5655c-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5655c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5655c-114">Requirements</span></span>



| <span data-ttu-id="5655c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5655c-115">Requirement</span></span> | <span data-ttu-id="5655c-116">Value</span><span class="sxs-lookup"><span data-stu-id="5655c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5655c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5655c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5655c-118">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5655c-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5655c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5655c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5655c-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5655c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5655c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5655c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5655c-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5655c-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5655c-123">IDL</span><span class="sxs-lookup"><span data-stu-id="5655c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5655c-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5655c-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5655c-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5655c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5655c-126"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5655c-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

