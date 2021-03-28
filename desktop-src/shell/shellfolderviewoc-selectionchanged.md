---
description: Indica que ha cambiado el estado de selección de uno o varios elementos de la vista.
title: Evento ShellFolderViewOC. SelectionChanged (Shldisp. h)
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
ms.openlocfilehash: 3f88ad698b990847a9b7f2fa1b74cc5b53ec7beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361183"
---
# <a name="shellfolderviewocselectionchanged-event"></a><span data-ttu-id="2bf9b-103">Evento ShellFolderViewOC. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="2bf9b-103">ShellFolderViewOC.SelectionChanged event</span></span>

<span data-ttu-id="2bf9b-104">Indica que ha cambiado el estado de selección de uno o varios elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="2bf9b-104">Indicates that the selection state of one or more items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bf9b-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="2bf9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2bf9b-106">Parameters</span></span>

<span data-ttu-id="2bf9b-107">Este controlador de eventos no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2bf9b-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf9b-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bf9b-108">Remarks</span></span>

<span data-ttu-id="2bf9b-109">Proporcione el código de control de eventos para este evento, tal como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="2bf9b-109">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_SelectionChanged()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="2bf9b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bf9b-110">Requirements</span></span>



| <span data-ttu-id="2bf9b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bf9b-111">Requirement</span></span> | <span data-ttu-id="2bf9b-112">Value</span><span class="sxs-lookup"><span data-stu-id="2bf9b-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf9b-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bf9b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2bf9b-114">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2bf9b-114">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2bf9b-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bf9b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2bf9b-116">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bf9b-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2bf9b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bf9b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bf9b-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bf9b-118"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2bf9b-119">IDL</span><span class="sxs-lookup"><span data-stu-id="2bf9b-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2bf9b-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2bf9b-120"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2bf9b-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bf9b-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bf9b-122"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf9b-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bf9b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bf9b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf9b-124">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="2bf9b-124">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




