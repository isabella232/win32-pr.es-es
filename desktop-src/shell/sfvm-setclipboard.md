---
description: Notifica a IShellView cuando uno de sus objetos se coloca en el portapapeles como resultado de un comando de menú. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_SETCLIPBOARD (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c9c30848de77ef7de101eaa9d724f2f26f9d384c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997945"
---
# <a name="sfvm_setclipboard-message"></a><span data-ttu-id="20484-104">\_Mensaje SETCLIPBOARD SFVM</span><span class="sxs-lookup"><span data-stu-id="20484-104">SFVM\_SETCLIPBOARD message</span></span>

<span data-ttu-id="20484-105">Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) cuando uno de sus objetos se coloca en el portapapeles como resultado de un comando de menú.</span><span class="sxs-lookup"><span data-stu-id="20484-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) when one of its objects is placed on the Clipboard as a result of a menu command.</span></span> <span data-ttu-id="20484-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="20484-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a><span data-ttu-id="20484-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20484-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20484-108">*dwEffect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="20484-108">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20484-109">Use (WPARAM)-2 Si el elemento se está cortando en el portapapeles o (WPARAM)-3 si el elemento se va a copiar en el portapapeles.</span><span class="sxs-lookup"><span data-stu-id="20484-109">Use (WPARAM)-2 if the item is being cut to the Clipboard or (WPARAM)-3 if the item is being copied to the Clipboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20484-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20484-110">Return value</span></span>

<span data-ttu-id="20484-111">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="20484-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20484-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20484-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="20484-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20484-113">Requirements</span></span>



| <span data-ttu-id="20484-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="20484-114">Requirement</span></span> | <span data-ttu-id="20484-115">Value</span><span class="sxs-lookup"><span data-stu-id="20484-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="20484-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20484-116">Minimum supported client</span></span><br/> | <span data-ttu-id="20484-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="20484-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="20484-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="20484-118">Minimum supported server</span></span><br/> | <span data-ttu-id="20484-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="20484-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="20484-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20484-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="20484-121"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="20484-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




