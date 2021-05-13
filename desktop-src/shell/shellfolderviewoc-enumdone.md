---
description: Indica que el objeto ShellFolderView ha terminado de enumerar el contenido de la carpeta.
title: Evento ShellFolderViewOC.EnumDone (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841056"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="e187f-103">Evento ShellFolderViewOC.EnumDone</span><span class="sxs-lookup"><span data-stu-id="e187f-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="e187f-104">Indica que el [**objeto ShellFolderView**](shellfolderview.md) ha terminado de enumerar el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e187f-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="e187f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e187f-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="e187f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e187f-106">Parameters</span></span>

<span data-ttu-id="e187f-107">Este controlador de eventos no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e187f-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e187f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e187f-108">Remarks</span></span>

<span data-ttu-id="e187f-109">El [**objeto ShellFolderView**](shellfolderview.md) debe enumerar el contenido de una carpeta para poder mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="e187f-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="e187f-110">Con carpetas grandes o ubicadas en un sistema remoto, este proceso puede tardar hasta varios minutos.</span><span class="sxs-lookup"><span data-stu-id="e187f-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="e187f-111">Durante este tiempo, se muestra un gráfico animado de la luz para indicar al usuario que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="e187f-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="e187f-112">Una vez completada la enumeración, se desencadena el evento **EnumDone** y el gráfico de la mano se reemplaza por el contenido de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e187f-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="e187f-113">Proporcione código de control de eventos para este evento como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="e187f-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="e187f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e187f-114">Requirements</span></span>



| <span data-ttu-id="e187f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e187f-115">Requirement</span></span> | <span data-ttu-id="e187f-116">Value</span><span class="sxs-lookup"><span data-stu-id="e187f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e187f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e187f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e187f-118">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="e187f-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e187f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e187f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e187f-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e187f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e187f-121">Header</span><span class="sxs-lookup"><span data-stu-id="e187f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e187f-122"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="e187f-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e187f-123">Idl</span><span class="sxs-lookup"><span data-stu-id="e187f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e187f-124"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="e187f-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e187f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e187f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e187f-126"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="e187f-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e187f-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e187f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e187f-128">**ShellFolderViewOC**</span><span class="sxs-lookup"><span data-stu-id="e187f-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




