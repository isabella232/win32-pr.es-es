---
description: Notifica a IShellView que reorganice sus elementos. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_REARRANGE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083406"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="4089e-104">SFVM \_ reorganizar mensaje</span><span class="sxs-lookup"><span data-stu-id="4089e-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="4089e-105">Notifica a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) que reorganice sus elementos.</span><span class="sxs-lookup"><span data-stu-id="4089e-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="4089e-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="4089e-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="4089e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4089e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4089e-108">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4089e-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4089e-109">Se pasa a [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span><span class="sxs-lookup"><span data-stu-id="4089e-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="4089e-110">Vea [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) para obtener más información sobre este parámetro.</span><span class="sxs-lookup"><span data-stu-id="4089e-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4089e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4089e-111">Return value</span></span>

<span data-ttu-id="4089e-112">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4089e-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4089e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4089e-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4089e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4089e-114">Requirements</span></span>



| <span data-ttu-id="4089e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4089e-115">Requirement</span></span> | <span data-ttu-id="4089e-116">Value</span><span class="sxs-lookup"><span data-stu-id="4089e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4089e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4089e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4089e-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4089e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4089e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4089e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4089e-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4089e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4089e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4089e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4089e-122"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4089e-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




