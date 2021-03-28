---
description: SFVM \_ THISIDLIST puede modificarse o no estar disponible.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Mensaje de SFVM_THISIDLIST (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818619"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="b4fdd-103">SFVM \_ THISIDLIST</span><span class="sxs-lookup"><span data-stu-id="b4fdd-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="b4fdd-104">\[**SFVM \_ THISIDLIST** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b4fdd-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4fdd-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="b4fdd-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b4fdd-106">Permite que el objeto de devolución de llamada especifique el puntero de la vista a una lista de identificadores de elemento (PIDL).</span><span class="sxs-lookup"><span data-stu-id="b4fdd-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="b4fdd-107">Solo se usa cuando se ha producido un error en [**IPersistIDList:: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) y [**IPersistFolder2:: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) .</span><span class="sxs-lookup"><span data-stu-id="b4fdd-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="b4fdd-108">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="b4fdd-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="b4fdd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4fdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4fdd-110">*PIDL* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b4fdd-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4fdd-111">Dirección de PIDL de la vista.</span><span class="sxs-lookup"><span data-stu-id="b4fdd-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4fdd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4fdd-112">Requirements</span></span>



| <span data-ttu-id="b4fdd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4fdd-113">Requirement</span></span> | <span data-ttu-id="b4fdd-114">Value</span><span class="sxs-lookup"><span data-stu-id="b4fdd-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fdd-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4fdd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fdd-116">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b4fdd-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b4fdd-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4fdd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fdd-118">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4fdd-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b4fdd-119">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b4fdd-119">End of client support</span></span><br/>    | <span data-ttu-id="b4fdd-120">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="b4fdd-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="b4fdd-121">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b4fdd-121">End of server support</span></span><br/>    | <span data-ttu-id="b4fdd-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4fdd-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="b4fdd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4fdd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4fdd-124"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4fdd-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
