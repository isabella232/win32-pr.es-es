---
description: 'Evento ShellFolderView.SelectionChanged: se produce cuando el estado de selección de cualquier elemento o elemento de la vista ha cambiado.'
title: Evento ShellFolderView.SelectionChanged (Shldisp.h)
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
ms.assetid: e91b72fd-fd26-4e38-8e80-41febec3ca03
ms.openlocfilehash: 31a32865a979bf6b5fa115912bdc32a9680e5064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104003"
---
# <a name="shellfolderviewselectionchanged-event"></a><span data-ttu-id="7b915-103">Evento ShellFolderView.SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="7b915-103">ShellFolderView.SelectionChanged event</span></span>

<span data-ttu-id="7b915-104">Se produce cuando el estado de selección de cualquier elemento o elemento de la vista ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="7b915-104">Occurs when the selection state of any item or items in the view has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b915-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b915-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderView.SelectionChanged = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="7b915-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b915-106">Parameters</span></span>

<span data-ttu-id="7b915-107">Este controlador de eventos no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7b915-107">This event handler has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b915-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b915-108">Requirements</span></span>



| <span data-ttu-id="7b915-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b915-109">Requirement</span></span> | <span data-ttu-id="7b915-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7b915-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b915-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b915-111">Minimum supported client</span></span><br/> | <span data-ttu-id="7b915-112">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="7b915-112">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7b915-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b915-113">Minimum supported server</span></span><br/> | <span data-ttu-id="7b915-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7b915-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7b915-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b915-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b915-116"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="7b915-116"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7b915-117">Idl</span><span class="sxs-lookup"><span data-stu-id="7b915-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b915-118"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b915-118"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7b915-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b915-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b915-120"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7b915-120"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




