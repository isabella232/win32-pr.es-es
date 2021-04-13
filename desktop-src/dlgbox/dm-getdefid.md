---
title: Mensaje de DM_GETDEFID (Winuser. h)
description: Recupera el identificador del control de botón de opción predeterminado para un cuadro de diálogo.
ms.assetid: 9f00a494-f5a2-4c4e-a9fc-2220d9326eb9
keywords:
- DM_GETDEFID cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- DM_GETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fdcdfc2cd278ab452d48ecb1c254bdb00ffbb7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535266"
---
# <a name="dm_getdefid-message"></a><span data-ttu-id="35cf9-104">\_Mensaje GETDEFID de DM</span><span class="sxs-lookup"><span data-stu-id="35cf9-104">DM\_GETDEFID message</span></span>

<span data-ttu-id="35cf9-105">Recupera el identificador del control de botón de opción predeterminado para un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35cf9-105">Retrieves the identifier of the default push button control for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_GETDEFID         (WM_USER+0)
```



## <a name="parameters"></a><span data-ttu-id="35cf9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35cf9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35cf9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35cf9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35cf9-108">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="35cf9-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="35cf9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35cf9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35cf9-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="35cf9-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35cf9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35cf9-111">Return value</span></span>

<span data-ttu-id="35cf9-112">Si existe un botón de control predeterminado, la palabra de orden superior del valor devuelto contiene el valor **DC \_ HASDEFID** y la palabra de orden inferior contiene el identificador de control.</span><span class="sxs-lookup"><span data-stu-id="35cf9-112">If a default push button exists, the high-order word of the return value contains the value **DC\_HASDEFID** and the low-order word contains the control identifier.</span></span> <span data-ttu-id="35cf9-113">De lo contrario, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="35cf9-113">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="35cf9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35cf9-114">Remarks</span></span>

<span data-ttu-id="35cf9-115">La función [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="35cf9-115">The [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="35cf9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35cf9-116">Requirements</span></span>



| <span data-ttu-id="35cf9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="35cf9-117">Requirement</span></span> | <span data-ttu-id="35cf9-118">Value</span><span class="sxs-lookup"><span data-stu-id="35cf9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35cf9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35cf9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="35cf9-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="35cf9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35cf9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35cf9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="35cf9-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35cf9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35cf9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35cf9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="35cf9-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35cf9-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35cf9-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="35cf9-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="35cf9-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="35cf9-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35cf9-127">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="35cf9-127">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="35cf9-128">**DM \_ SETDEFID**</span><span class="sxs-lookup"><span data-stu-id="35cf9-128">**DM\_SETDEFID**</span></span>](dm-setdefid.md)
</dt> <dt>

<span data-ttu-id="35cf9-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="35cf9-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35cf9-130">Cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="35cf9-130">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





