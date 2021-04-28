---
description: 'Propiedad ShellFolderView.Folder: obtiene un objeto Folder que representa la vista.'
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Propiedad ShellFolderView.Folder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 370fddc1428c8f77edb77cdac2dc04123fc5211f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083423"
---
# <a name="shellfolderviewfolder-property"></a><span data-ttu-id="c6f2d-103">Propiedad ShellFolderView.Folder</span><span class="sxs-lookup"><span data-stu-id="c6f2d-103">ShellFolderView.Folder property</span></span>

<span data-ttu-id="c6f2d-104">Obtiene un [**objeto Folder**](folder.md) que representa la vista.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-104">Gets a [**Folder**](folder.md) object that represents the view.</span></span>

<span data-ttu-id="c6f2d-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f2d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6f2d-106">Syntax</span></span>


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a><span data-ttu-id="c6f2d-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c6f2d-107">Property value</span></span>

<span data-ttu-id="c6f2d-108">Objeto que recibe el [**objeto Folder.**](folder.md)</span><span class="sxs-lookup"><span data-stu-id="c6f2d-108">Object that receives the [**Folder**](folder.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6f2d-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c6f2d-109">Remarks</span></span>

<span data-ttu-id="c6f2d-110">**Solo** se puede llamar a la carpeta en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-110">**Folder** can only be called on the local system.</span></span> <span data-ttu-id="c6f2d-111">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-111">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="c6f2d-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c6f2d-112">Examples</span></span>

<span data-ttu-id="c6f2d-113">En el ejemplo siguiente se muestra el uso adecuado de esta propiedad para JScript insertado en HTML.</span><span class="sxs-lookup"><span data-stu-id="c6f2d-113">The following example shows the proper usage of this property for JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
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
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="c6f2d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6f2d-114">Requirements</span></span>



| <span data-ttu-id="c6f2d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f2d-115">Requirement</span></span> | <span data-ttu-id="c6f2d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c6f2d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f2d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6f2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f2d-118">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="c6f2d-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6f2d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6f2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f2d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c6f2d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6f2d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6f2d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6f2d-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c6f2d-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c6f2d-123">Idl</span><span class="sxs-lookup"><span data-stu-id="c6f2d-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6f2d-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6f2d-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c6f2d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6f2d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f2d-126"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c6f2d-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




