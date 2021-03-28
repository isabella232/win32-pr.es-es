---
description: 'Notifica al objeto de devolución de llamada que se está quitando un menú. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_UNMERGEMENU (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986067"
---
# <a name="sfvm_unmergemenu-message"></a><span data-ttu-id="5a113-104">SFVM \_ UNMERGEMENU</span><span class="sxs-lookup"><span data-stu-id="5a113-104">SFVM\_UNMERGEMENU message</span></span>

<span data-ttu-id="5a113-105">Notifica al objeto de devolución de llamada que se está quitando un menú.</span><span class="sxs-lookup"><span data-stu-id="5a113-105">Notifies the callback object that a menu is being removed.</span></span> <span data-ttu-id="5a113-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="5a113-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a><span data-ttu-id="5a113-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a113-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a113-108">*hmenuCurrent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5a113-108">*hmenuCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a113-109">Identificador del menú que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5a113-109">The handle of the menu that is being removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a113-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a113-110">Requirements</span></span>



| <span data-ttu-id="5a113-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a113-111">Requirement</span></span> | <span data-ttu-id="5a113-112">Value</span><span class="sxs-lookup"><span data-stu-id="5a113-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5a113-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a113-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5a113-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5a113-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5a113-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a113-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5a113-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5a113-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5a113-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a113-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a113-118"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a113-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
