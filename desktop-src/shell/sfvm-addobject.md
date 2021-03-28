---
description: Agrega un objeto a la vista de Shell. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_ADDOBJECT (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997812"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="1ed50-104">SFVM \_ ADDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1ed50-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="1ed50-105">Agrega un objeto a la vista de Shell.</span><span class="sxs-lookup"><span data-stu-id="1ed50-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="1ed50-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="1ed50-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="1ed50-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ed50-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed50-108">*PIDL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ed50-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="1ed50-109">Puntero al objeto de interés que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="1ed50-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed50-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ed50-110">Return value</span></span>

<span data-ttu-id="1ed50-111">Devuelve el nuevo identificador de elemento ListView del objeto agregado si el proceso se realizó correctamente; de lo contrario, devuelve-1.</span><span class="sxs-lookup"><span data-stu-id="1ed50-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed50-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed50-112">Requirements</span></span>



| <span data-ttu-id="1ed50-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed50-113">Requirement</span></span> | <span data-ttu-id="1ed50-114">Value</span><span class="sxs-lookup"><span data-stu-id="1ed50-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed50-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ed50-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed50-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1ed50-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1ed50-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ed50-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed50-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1ed50-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ed50-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ed50-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ed50-120"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed50-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




