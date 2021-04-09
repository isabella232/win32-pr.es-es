---
title: Mensaje de DM_REPOSITION (Winuser. h)
description: Cambia de posición un cuadro de diálogo de nivel superior para que quepa en el área del escritorio. Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar el tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.
ms.assetid: 8386d23e-06ea-4ea7-adde-ac97fc97861d
keywords:
- DM_REPOSITION cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- DM_REPOSITION
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19425d4d77a62117f3fadfdd98f0629b81bf334c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079727"
---
# <a name="dm_reposition-message"></a><span data-ttu-id="3d6a3-105">\_Mensaje de REposición de DM</span><span class="sxs-lookup"><span data-stu-id="3d6a3-105">DM\_REPOSITION message</span></span>

<span data-ttu-id="3d6a3-106">Cambia de posición un cuadro de diálogo de nivel superior para que quepa en el área del escritorio.</span><span class="sxs-lookup"><span data-stu-id="3d6a3-106">Repositions a top-level dialog box so that it fits within the desktop area.</span></span> <span data-ttu-id="3d6a3-107">Una aplicación puede enviar este mensaje a un cuadro de diálogo después de cambiar el tamaño para asegurarse de que todo el cuadro de diálogo permanece visible.</span><span class="sxs-lookup"><span data-stu-id="3d6a3-107">An application can send this message to a dialog box after resizing it to ensure that the entire dialog box remains visible.</span></span>


```C++
#define WM_USER              0x0400
#define DM_REPOSITION       (WM_USER+2)
```



## <a name="parameters"></a><span data-ttu-id="3d6a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d6a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6a3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d6a3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6a3-110">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3d6a3-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3d6a3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d6a3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6a3-112">Este parámetro no se utiliza y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3d6a3-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6a3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d6a3-113">Return value</span></span>

<span data-ttu-id="3d6a3-114">Este mensaje no tiene ningún valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3d6a3-114">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6a3-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d6a3-115">Remarks</span></span>

<span data-ttu-id="3d6a3-116">Este mensaje no tiene ningún efecto si el cuadro de diálogo es una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="3d6a3-116">This message has no effect if the dialog box is a child window.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6a3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d6a3-117">Requirements</span></span>



| <span data-ttu-id="3d6a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d6a3-118">Requirement</span></span> | <span data-ttu-id="3d6a3-119">Value</span><span class="sxs-lookup"><span data-stu-id="3d6a3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6a3-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d6a3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6a3-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3d6a3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3d6a3-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d6a3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6a3-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3d6a3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3d6a3-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d6a3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6a3-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d6a3-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d6a3-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d6a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d6a3-127">Información general sobre cuadros de diálogo</span><span class="sxs-lookup"><span data-stu-id="3d6a3-127">Dialog Boxes Overview</span></span>](dialog-boxes.md)
</dt> </dl>

 

 





