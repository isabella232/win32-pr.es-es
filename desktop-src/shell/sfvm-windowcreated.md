---
description: 'Notifica al objeto de devolución de llamada que se está creando la ventana vista de carpetas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_WINDOWCREATED (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986094"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="cd068-104">SFVM \_ WINDOWCREATED</span><span class="sxs-lookup"><span data-stu-id="cd068-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="cd068-105">Notifica al objeto de devolución de llamada que se está creando la ventana vista de carpetas.</span><span class="sxs-lookup"><span data-stu-id="cd068-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="cd068-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="cd068-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="cd068-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd068-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd068-108">*hwndView* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd068-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd068-109">Identificador de la ventana de la vista de carpetas.</span><span class="sxs-lookup"><span data-stu-id="cd068-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd068-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd068-110">Requirements</span></span>



| <span data-ttu-id="cd068-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd068-111">Requirement</span></span> | <span data-ttu-id="cd068-112">Value</span><span class="sxs-lookup"><span data-stu-id="cd068-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd068-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd068-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cd068-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="cd068-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cd068-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd068-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cd068-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="cd068-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cd068-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd068-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd068-118"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd068-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
