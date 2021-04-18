---
description: 'Permite que el objeto de devolución de llamada especifique un parámetro de ordenación predeterminado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_GETSORTDEFAULTS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986102"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="95b85-104">SFVM \_ GETSORTDEFAULTS</span><span class="sxs-lookup"><span data-stu-id="95b85-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="95b85-105">Permite que el objeto de devolución de llamada especifique un parámetro de ordenación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="95b85-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="95b85-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="95b85-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="95b85-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95b85-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b85-108">*iDirection* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="95b85-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b85-109">Dirección de ordenación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="95b85-109">The default sorting direction.</span></span> <span data-ttu-id="95b85-110">Establezca este parámetro en un valor positivo para ordenar en orden ascendente.</span><span class="sxs-lookup"><span data-stu-id="95b85-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="95b85-111">Establezca este parámetro en cero o en un valor negativo para ordenar en orden descendente.</span><span class="sxs-lookup"><span data-stu-id="95b85-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="95b85-112">*iColumn* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="95b85-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95b85-113">Columna usada para la ordenación.</span><span class="sxs-lookup"><span data-stu-id="95b85-113">The column used for the sort.</span></span> <span data-ttu-id="95b85-114">Esto se pasará a [**IShellFolder:: CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) en los 16 bits inferiores de su valor *lParam* .</span><span class="sxs-lookup"><span data-stu-id="95b85-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95b85-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95b85-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95b85-116">: El objeto de vista de carpeta del sistema no reconoce **SFVM \_ GETSORTDEFAULTS** .</span><span class="sxs-lookup"><span data-stu-id="95b85-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95b85-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95b85-117">Requirements</span></span>



| <span data-ttu-id="95b85-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b85-118">Requirement</span></span> | <span data-ttu-id="95b85-119">Value</span><span class="sxs-lookup"><span data-stu-id="95b85-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="95b85-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95b85-120">Minimum supported client</span></span><br/> | <span data-ttu-id="95b85-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="95b85-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="95b85-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95b85-122">Minimum supported server</span></span><br/> | <span data-ttu-id="95b85-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="95b85-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="95b85-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95b85-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="95b85-125"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b85-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
