---
description: Recupera el identificador de menú de la ventana actual.
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: Mensaje de MN_GETHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64d501654af426a292156d05242b372336eee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276885"
---
# <a name="mn_gethmenu-message"></a><span data-ttu-id="865a4-103">MN \_ GETHMENU Message</span><span class="sxs-lookup"><span data-stu-id="865a4-103">MN\_GETHMENU message</span></span>

<span data-ttu-id="865a4-104">Recupera el identificador de menú de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="865a4-104">Retrieves the menu handle for the current window.</span></span>


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a><span data-ttu-id="865a4-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="865a4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="865a4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="865a4-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="865a4-107">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="865a4-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="865a4-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="865a4-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="865a4-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="865a4-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="865a4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="865a4-110">Return value</span></span>

<span data-ttu-id="865a4-111">Tipo: **HMENU**</span><span class="sxs-lookup"><span data-stu-id="865a4-111">Type: **HMENU**</span></span>

<span data-ttu-id="865a4-112">Si se realiza correctamente, el valor devuelto es el **HMENU** de la ventana actual.</span><span class="sxs-lookup"><span data-stu-id="865a4-112">If successful, the return value is the **HMENU** for the current window.</span></span> <span data-ttu-id="865a4-113">Si se produce un error, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="865a4-113">If it fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="865a4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="865a4-114">Requirements</span></span>



| <span data-ttu-id="865a4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="865a4-115">Requirement</span></span> | <span data-ttu-id="865a4-116">Value</span><span class="sxs-lookup"><span data-stu-id="865a4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="865a4-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="865a4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="865a4-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="865a4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="865a4-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="865a4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="865a4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="865a4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="865a4-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="865a4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="865a4-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="865a4-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 




