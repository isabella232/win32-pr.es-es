---
description: 'Permite que el objeto de devolución de llamada especifique el número de elementos en la vista de carpeta. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_DEFITEMCOUNT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002209"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="5ba2d-104">SFVM \_ DEFITEMCOUNT</span><span class="sxs-lookup"><span data-stu-id="5ba2d-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="5ba2d-105">Permite que el objeto de devolución de llamada especifique el número de elementos en la vista de carpeta.</span><span class="sxs-lookup"><span data-stu-id="5ba2d-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="5ba2d-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="5ba2d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="5ba2d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ba2d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ba2d-108">*cItems* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ba2d-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba2d-109">Número de elementos de la vista de carpeta.</span><span class="sxs-lookup"><span data-stu-id="5ba2d-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ba2d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ba2d-110">Requirements</span></span>



| <span data-ttu-id="5ba2d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ba2d-111">Requirement</span></span> | <span data-ttu-id="5ba2d-112">Value</span><span class="sxs-lookup"><span data-stu-id="5ba2d-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba2d-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ba2d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5ba2d-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5ba2d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5ba2d-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ba2d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5ba2d-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ba2d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5ba2d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ba2d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ba2d-118"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba2d-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
