---
description: 'Notifica al objeto de devolución de llamada que se está actualizando la barra de estado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_UPDATESTATUSBAR (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997773"
---
# <a name="sfvm_updatestatusbar-message"></a><span data-ttu-id="09155-104">SFVM \_ UPDATESTATUSBAR</span><span class="sxs-lookup"><span data-stu-id="09155-104">SFVM\_UPDATESTATUSBAR message</span></span>

<span data-ttu-id="09155-105">Notifica al objeto de devolución de llamada que se está actualizando la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="09155-105">Notifies the callback object that the status bar is being updated.</span></span> <span data-ttu-id="09155-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="09155-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a><span data-ttu-id="09155-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09155-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09155-108">*fInitialize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="09155-108">*fInitialize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09155-109">Valor **booleano** que se establece en **true** si se está inicializando la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="09155-109">A **BOOL** value that is set to **TRUE** if the status bar is being initialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09155-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09155-110">Remarks</span></span>

<span data-ttu-id="09155-111">Cuando reciba esta notificación:</span><span class="sxs-lookup"><span data-stu-id="09155-111">When you receive this notification:</span></span>

-   <span data-ttu-id="09155-112">Vuelva a \_ Aceptar si va a controlar la actualización.</span><span class="sxs-lookup"><span data-stu-id="09155-112">Return S\_OK if you will handle the update.</span></span>
-   <span data-ttu-id="09155-113">Devuelve MAKE \_ HRESULT (Severity \_ Success, 0, 1) para que el objeto de vista de carpeta del sistema establezca el texto de la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="09155-113">Return MAKE\_HRESULT(SEVERITY\_SUCCESS,0,1) to have the system folder view object set the status bar text.</span></span>
-   <span data-ttu-id="09155-114">Devolver E \_ no puede hacer que el objeto de vista de carpeta del sistema controle la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="09155-114">Return E\_FAIL to have the system folder view object handle the status bar.</span></span>

<span data-ttu-id="09155-115">El texto predeterminado de la barra de estado es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="09155-115">The default status bar text is as follows.</span></span>



| <span data-ttu-id="09155-116">Estado</span><span class="sxs-lookup"><span data-stu-id="09155-116">Status</span></span>                      | <span data-ttu-id="09155-117">Texto de la barra de estado</span><span class="sxs-lookup"><span data-stu-id="09155-117">Status bar text</span></span>                         |
|-----------------------------|-----------------------------------------|
| <span data-ttu-id="09155-118">No hay elementos seleccionados</span><span class="sxs-lookup"><span data-stu-id="09155-118">No items selected</span></span>           | <span data-ttu-id="09155-119">" \# \# objetos" (en la carpeta)</span><span class="sxs-lookup"><span data-stu-id="09155-119">"\#\# objects" (in the folder)</span></span>          |
| <span data-ttu-id="09155-120">Un elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="09155-120">One item selected</span></span>           | <span data-ttu-id="09155-121">El recuadro informativo para el elemento, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="09155-121">The infotip for the item, if available.</span></span> |
| <span data-ttu-id="09155-122">Hay más de un elemento seleccionado</span><span class="sxs-lookup"><span data-stu-id="09155-122">More than one item selected</span></span> | <span data-ttu-id="09155-123">" \# \# objetos seleccionados"</span><span class="sxs-lookup"><span data-stu-id="09155-123">"\#\# objects selected"</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="09155-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09155-124">Requirements</span></span>



| <span data-ttu-id="09155-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="09155-125">Requirement</span></span> | <span data-ttu-id="09155-126">Value</span><span class="sxs-lookup"><span data-stu-id="09155-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09155-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09155-127">Minimum supported client</span></span><br/> | <span data-ttu-id="09155-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="09155-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09155-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09155-129">Minimum supported server</span></span><br/> | <span data-ttu-id="09155-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="09155-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09155-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09155-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="09155-132"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="09155-132"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
