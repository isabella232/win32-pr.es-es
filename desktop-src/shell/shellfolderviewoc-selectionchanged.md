---
description: Indica que el estado de selección de uno o varios elementos de la vista ha cambiado.
title: Evento ShellFolderViewOC.SelectionChanged (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 53d6fc3eb6f13d136af603a3129ba75a46c3c6a6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841046"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="f1750-103">Evento ShellFolderViewOC.SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="f1750-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="f1750-104">Indica que el estado de selección de uno o varios elementos de la vista ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f1750-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1750-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1750-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="f1750-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1750-106">Parameters</span></span>

<span data-ttu-id="f1750-107">Este controlador de eventos no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f1750-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1750-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1750-108">Remarks</span></span>

<span data-ttu-id="f1750-109">Proporcione código de control de eventos para este evento como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="f1750-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="f1750-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1750-110">Requirements</span></span>



| <span data-ttu-id="f1750-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1750-111">Requirement</span></span> | <span data-ttu-id="f1750-112">Value</span><span class="sxs-lookup"><span data-stu-id="f1750-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1750-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1750-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f1750-114">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="f1750-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1750-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1750-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f1750-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1750-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f1750-117">Header</span><span class="sxs-lookup"><span data-stu-id="f1750-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1750-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f1750-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f1750-119">Idl</span><span class="sxs-lookup"><span data-stu-id="f1750-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f1750-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f1750-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f1750-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f1750-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1750-122"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f1750-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1750-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1750-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1750-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="f1750-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




