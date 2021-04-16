---
title: Propiedad WebViewFolderContents. script (Shldisp. h)
description: Obtiene el objeto de scripting para la vista.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- Características del entorno de Windows heredado de propiedades de script
- Propiedad de script características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredadas, propiedad de script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92133278d73851fa43353c116a2385da9b0fd3da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105696006"
---
# <a name="webviewfoldercontentsscript-property"></a><span data-ttu-id="4eb95-106">Propiedad WebViewFolderContents. script</span><span class="sxs-lookup"><span data-stu-id="4eb95-106">WebViewFolderContents.Script property</span></span>

<span data-ttu-id="4eb95-107">Obtiene el objeto de scripting para la vista.</span><span class="sxs-lookup"><span data-stu-id="4eb95-107">Gets the scripting object for the view.</span></span>

<span data-ttu-id="4eb95-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4eb95-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb95-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4eb95-109">Syntax</span></span>


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a><span data-ttu-id="4eb95-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4eb95-110">Property value</span></span>

<span data-ttu-id="4eb95-111">Variable de tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de scripting.</span><span class="sxs-lookup"><span data-stu-id="4eb95-111">A variable of type [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) that receives the scripting object.</span></span>

## <a name="examples"></a><span data-ttu-id="4eb95-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4eb95-112">Examples</span></span>

<span data-ttu-id="4eb95-113">En el ejemplo siguiente se muestra el uso correcto de esta propiedad en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="4eb95-113">The following example shows the proper usage of this property in JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
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



## <a name="requirements"></a><span data-ttu-id="4eb95-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eb95-114">Requirements</span></span>



| <span data-ttu-id="4eb95-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb95-115">Requirement</span></span> | <span data-ttu-id="4eb95-116">Value</span><span class="sxs-lookup"><span data-stu-id="4eb95-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb95-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eb95-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb95-118">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4eb95-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4eb95-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eb95-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb95-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4eb95-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4eb95-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4eb95-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb95-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eb95-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4eb95-123">IDL</span><span class="sxs-lookup"><span data-stu-id="4eb95-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4eb95-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4eb95-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4eb95-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4eb95-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4eb95-126"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4eb95-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

