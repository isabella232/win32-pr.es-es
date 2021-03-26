---
description: 'Permite que el objeto de devolución de llamada modifique un menú emergente del explorador de Windows antes de que se muestre. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_INITMENUPOPUP (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986078"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="67cec-104">SFVM \_ INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="67cec-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="67cec-105">Permite que el objeto de devolución de llamada modifique un menú emergente del explorador de Windows antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="67cec-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="67cec-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="67cec-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="67cec-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67cec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67cec-108">*idCmd \_ NINDEX* \[\]</span><span class="sxs-lookup"><span data-stu-id="67cec-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67cec-109">La palabra de orden inferior de este parámetro contiene el valor del primer identificador de comando reservado para los comandos del cliente.</span><span class="sxs-lookup"><span data-stu-id="67cec-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="67cec-110">La palabra de orden superior contiene el índice del menú.</span><span class="sxs-lookup"><span data-stu-id="67cec-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="67cec-111">*HMENU* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="67cec-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67cec-112">Identificador del menú.</span><span class="sxs-lookup"><span data-stu-id="67cec-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67cec-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67cec-113">Remarks</span></span>

<span data-ttu-id="67cec-114">El objeto de vista de carpeta del sistema envía este mensaje cuando se selecciona un menú, pero antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="67cec-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="67cec-115">Procese este mensaje si, por ejemplo, necesita habilitar o deshabilitar comandos de menú.</span><span class="sxs-lookup"><span data-stu-id="67cec-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="67cec-116">El menú emergente puede ser:</span><span class="sxs-lookup"><span data-stu-id="67cec-116">The popup menu can be:</span></span>

-   <span data-ttu-id="67cec-117">Menú Archivo, editar o ver.</span><span class="sxs-lookup"><span data-stu-id="67cec-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="67cec-118">Un menú de nivel superior definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="67cec-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="67cec-119">Un submenú definido por el cliente.</span><span class="sxs-lookup"><span data-stu-id="67cec-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="67cec-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67cec-120">Requirements</span></span>



| <span data-ttu-id="67cec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="67cec-121">Requirement</span></span> | <span data-ttu-id="67cec-122">Value</span><span class="sxs-lookup"><span data-stu-id="67cec-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="67cec-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67cec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="67cec-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="67cec-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="67cec-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67cec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="67cec-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="67cec-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="67cec-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67cec-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="67cec-128"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="67cec-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67cec-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="67cec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67cec-130">**SFVM \_ MERGEMENU**</span><span class="sxs-lookup"><span data-stu-id="67cec-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
