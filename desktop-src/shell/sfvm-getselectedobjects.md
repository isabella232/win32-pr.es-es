---
description: Recupera una matriz de punteros a listas de identificadores de elementos (PIDL) para todos los objetos seleccionados. Usado por el \_ mensaje de SHShellFolderView.
title: Mensaje de SFVM_GETSELECTEDOBJECTS (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913314"
---
# <a name="sfvm_getselectedobjects-message"></a><span data-ttu-id="4b8b4-104">SFVM \_ GETSELECTEDOBJECTS</span><span class="sxs-lookup"><span data-stu-id="4b8b4-104">SFVM\_GETSELECTEDOBJECTS message</span></span>

<span data-ttu-id="4b8b4-105">Recupera una matriz de punteros a listas de identificadores de elementos (PIDL) para todos los objetos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="4b8b4-105">Retrieves an array of pointers to item identifier lists (PIDLs) for all selected objects.</span></span> <span data-ttu-id="4b8b4-106">Usado por [**el \_ mensaje de SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="4b8b4-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="4b8b4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b8b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b8b4-108">*ppidl* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b8b4-108">*ppidl* \[out\]</span></span>
</dt> <dd><span data-ttu-id="4b8b4-109">Dirección de una matriz de PIDL de los objetos seleccionados actualmente.</span><span class="sxs-lookup"><span data-stu-id="4b8b4-109">The address of an array of PIDLs of currently selected objects.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b8b4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b8b4-110">Return value</span></span>

<span data-ttu-id="4b8b4-111">Devuelve el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="4b8b4-111">Returns the number of items in the array.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b8b4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b8b4-112">Remarks</span></span>

<span data-ttu-id="4b8b4-113">Cuando termine, debe llamar a [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) en cada miembro de la matriz para liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="4b8b4-113">When finished, you should call [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) on each member of the array to free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8b4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b8b4-114">Requirements</span></span>



| <span data-ttu-id="4b8b4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8b4-115">Requirement</span></span> | <span data-ttu-id="4b8b4-116">Value</span><span class="sxs-lookup"><span data-stu-id="4b8b4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8b4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b8b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8b4-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b8b4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4b8b4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b8b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8b4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b8b4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4b8b4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b8b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b8b4-122"><dt>ShlObj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8b4-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




