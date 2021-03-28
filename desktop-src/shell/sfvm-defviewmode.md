---
description: 'Permite que el objeto de devolución de llamada especifique el modo de vista. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_DEFVIEWMODE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997921"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="c674a-104">SFVM \_ DEFVIEWMODE</span><span class="sxs-lookup"><span data-stu-id="c674a-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="c674a-105">Permite que el objeto de devolución de llamada especifique el modo de vista.</span><span class="sxs-lookup"><span data-stu-id="c674a-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="c674a-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c674a-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="c674a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c674a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c674a-108">*pViewMode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c674a-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c674a-109">Uno de los valores del tipo enumerado [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .</span><span class="sxs-lookup"><span data-stu-id="c674a-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c674a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c674a-110">Requirements</span></span>



| <span data-ttu-id="c674a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c674a-111">Requirement</span></span> | <span data-ttu-id="c674a-112">Value</span><span class="sxs-lookup"><span data-stu-id="c674a-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c674a-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c674a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c674a-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c674a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c674a-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c674a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c674a-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c674a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c674a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c674a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c674a-118"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c674a-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
