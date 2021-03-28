---
description: 'Notifica al objeto de devolución de llamada que se ha producido un evento que afecta a uno de sus elementos. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_FSNOTIFY (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2021
ms.locfileid: "104997977"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="033e4-104">SFVM \_ FSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="033e4-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="033e4-105">Notifica al objeto de devolución de llamada que se ha producido un evento que afecta a uno de sus elementos.</span><span class="sxs-lookup"><span data-stu-id="033e4-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="033e4-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="033e4-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="033e4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="033e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="033e4-108">*ppidl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="033e4-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033e4-109">Puntero de PIDL del elemento afectado.</span><span class="sxs-lookup"><span data-stu-id="033e4-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="033e4-110">*lEvent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="033e4-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="033e4-111">Valor de SHCNE que indica qué evento se ha producido.</span><span class="sxs-lookup"><span data-stu-id="033e4-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="033e4-112">Para obtener una lista de los valores posibles, vea [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span><span class="sxs-lookup"><span data-stu-id="033e4-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="033e4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="033e4-113">Requirements</span></span>



| <span data-ttu-id="033e4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="033e4-114">Requirement</span></span> | <span data-ttu-id="033e4-115">Value</span><span class="sxs-lookup"><span data-stu-id="033e4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="033e4-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="033e4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="033e4-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="033e4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="033e4-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="033e4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="033e4-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="033e4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="033e4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="033e4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="033e4-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="033e4-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
