---
description: Quita un objeto de la vista de Shell. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_REMOVEOBJECT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986103"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="e591d-104">SFVM \_ REMOVEOBJECT</span><span class="sxs-lookup"><span data-stu-id="e591d-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="e591d-105">Quita un objeto de la vista de Shell.</span><span class="sxs-lookup"><span data-stu-id="e591d-105">Removes an object from the shell view.</span></span> <span data-ttu-id="e591d-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="e591d-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="e591d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e591d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e591d-108">*PIDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e591d-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="e591d-109">PIDL del objeto que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="e591d-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e591d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e591d-110">Return value</span></span>

<span data-ttu-id="e591d-111">Devuelve el índice del elemento que se quitó si se encontró un elemento que coincide con el PIDL especificado; de lo contrario, devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="e591d-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="e591d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e591d-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e591d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e591d-113">Requirements</span></span>



| <span data-ttu-id="e591d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e591d-114">Requirement</span></span> | <span data-ttu-id="e591d-115">Value</span><span class="sxs-lookup"><span data-stu-id="e591d-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e591d-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e591d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e591d-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e591d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e591d-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e591d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e591d-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e591d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e591d-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e591d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e591d-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e591d-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




