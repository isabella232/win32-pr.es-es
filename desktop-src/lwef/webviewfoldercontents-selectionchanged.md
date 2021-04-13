---
title: Evento WebViewFolderContents. SelectionChanged (Shldisp. h)
description: Se produce cuando cambia el estado de selección de cualquier elemento o elementos de la vista.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- Evento SelectionChanged características del entorno de Windows heredado
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8421e9d06ff9fd24256da8a23cdd100b5749968
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535134"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a><span data-ttu-id="23c1f-104">Evento WebViewFolderContents. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="23c1f-104">WebViewFolderContents.SelectionChanged event</span></span>

<span data-ttu-id="23c1f-105">Se produce cuando cambia el estado de selección de cualquier elemento o elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="23c1f-105">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="23c1f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23c1f-106">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="23c1f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23c1f-107">Parameters</span></span>

<span data-ttu-id="23c1f-108">Este controlador de eventos no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="23c1f-108">This event handler has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="23c1f-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="23c1f-109">Examples</span></span>

<span data-ttu-id="23c1f-110">En el ejemplo siguiente se muestra el uso correcto de este evento para JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="23c1f-110">The following example shows the proper usage of this event for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="23c1f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23c1f-111">Requirements</span></span>



| <span data-ttu-id="23c1f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="23c1f-112">Requirement</span></span> | <span data-ttu-id="23c1f-113">Value</span><span class="sxs-lookup"><span data-stu-id="23c1f-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23c1f-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23c1f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="23c1f-115">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="23c1f-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="23c1f-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23c1f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="23c1f-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="23c1f-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="23c1f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23c1f-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c1f-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c1f-119"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="23c1f-120">IDL</span><span class="sxs-lookup"><span data-stu-id="23c1f-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23c1f-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23c1f-121"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="23c1f-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23c1f-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23c1f-123"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="23c1f-123"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 





