---
title: Propiedad WebViewFolderContents. ViewOptions (Shldisp. h)
description: Obtiene un conjunto de marcas ShellFolderViewOptions que indican las opciones actuales de la vista.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Propiedad ViewOptions características de entorno heredado de Windows
- Propiedad ViewOptions características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredado, propiedad ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078958"
---
# <a name="webviewfoldercontentsviewoptions-property"></a><span data-ttu-id="f583f-106">Propiedad WebViewFolderContents. ViewOptions</span><span class="sxs-lookup"><span data-stu-id="f583f-106">WebViewFolderContents.ViewOptions property</span></span>

<span data-ttu-id="f583f-107">Obtiene un conjunto de marcas [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indican las opciones actuales de la vista.</span><span class="sxs-lookup"><span data-stu-id="f583f-107">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span>

<span data-ttu-id="f583f-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f583f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f583f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f583f-109">Syntax</span></span>


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="f583f-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f583f-110">Property value</span></span>

<span data-ttu-id="f583f-111">Variable de tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de opciones de vista.</span><span class="sxs-lookup"><span data-stu-id="f583f-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span>

## <a name="examples"></a><span data-ttu-id="f583f-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f583f-112">Examples</span></span>

<span data-ttu-id="f583f-113">En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="f583f-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



## <a name="requirements"></a><span data-ttu-id="f583f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f583f-114">Requirements</span></span>



| <span data-ttu-id="f583f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f583f-115">Requirement</span></span> | <span data-ttu-id="f583f-116">Value</span><span class="sxs-lookup"><span data-stu-id="f583f-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f583f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f583f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f583f-118">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f583f-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f583f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f583f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f583f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f583f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f583f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f583f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f583f-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f583f-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f583f-123">IDL</span><span class="sxs-lookup"><span data-stu-id="f583f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f583f-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f583f-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f583f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f583f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f583f-126"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f583f-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

