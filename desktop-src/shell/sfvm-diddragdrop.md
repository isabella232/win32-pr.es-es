---
description: SFVM \_ DIDDRAGDROP puede modificarse o no estar disponible.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Mensaje de SFVM_DIDDRAGDROP (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997825"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="40890-103">SFVM \_ DIDDRAGDROP</span><span class="sxs-lookup"><span data-stu-id="40890-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="40890-104">\[**SFVM \_ DIDDRAGDROP** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="40890-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="40890-105">En versiones posteriores podría modificarse o no estar disponible.\]</span><span class="sxs-lookup"><span data-stu-id="40890-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="40890-106">Notifica a la función de devolución de llamada que se ha iniciado una operación de arrastrar y colocar.</span><span class="sxs-lookup"><span data-stu-id="40890-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="40890-107">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="40890-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="40890-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40890-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40890-109">*dwEffect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40890-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40890-110">Un especificador de efecto de colocación de la enumeración [**DROPEFFECT**](../com/dropeffect-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="40890-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="40890-111">Esto se obtiene llamando a [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span><span class="sxs-lookup"><span data-stu-id="40890-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="40890-112">*pIdo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="40890-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40890-113">Puntero a la instancia de [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="40890-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40890-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40890-114">Requirements</span></span>



| <span data-ttu-id="40890-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="40890-115">Requirement</span></span> | <span data-ttu-id="40890-116">Value</span><span class="sxs-lookup"><span data-stu-id="40890-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40890-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40890-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40890-118">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="40890-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="40890-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40890-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40890-120">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="40890-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="40890-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="40890-121">End of client support</span></span><br/>    | <span data-ttu-id="40890-122">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="40890-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="40890-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="40890-123">End of server support</span></span><br/>    | <span data-ttu-id="40890-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40890-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="40890-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40890-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="40890-126"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="40890-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
