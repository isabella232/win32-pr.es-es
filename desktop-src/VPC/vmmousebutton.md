---
title: Enumeración VMMouseButton (VPCCOMInterfaces. h)
description: Especifica el botón del mouse.
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- Enumeración de VMMouseButton Virtual PC
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492202"
---
# <a name="vmmousebutton-enumeration"></a><span data-ttu-id="ed454-104">Enumeración VMMouseButton</span><span class="sxs-lookup"><span data-stu-id="ed454-104">VMMouseButton enumeration</span></span>

<span data-ttu-id="ed454-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ed454-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ed454-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ed454-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ed454-107">Especifica el botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="ed454-107">Specifies the mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed454-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed454-108">Syntax</span></span>


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a><span data-ttu-id="ed454-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="ed454-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ed454-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton a la \_ izquierda**</span><span class="sxs-lookup"><span data-stu-id="ed454-110"><span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**vmMouseButton\_Left**</span></span>
</dt> <dd>

<span data-ttu-id="ed454-111">Botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="ed454-111">The left mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="ed454-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ derecha**</span><span class="sxs-lookup"><span data-stu-id="ed454-112"><span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton\_Right**</span></span>
</dt> <dd>

<span data-ttu-id="ed454-113">Botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="ed454-113">The right mouse button.</span></span>

</dd> <dt>

<span data-ttu-id="ed454-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**Centro de vmMouseButton \_**</span><span class="sxs-lookup"><span data-stu-id="ed454-114"><span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton\_Center**</span></span>
</dt> <dd>

<span data-ttu-id="ed454-115">Botón central del mouse.</span><span class="sxs-lookup"><span data-stu-id="ed454-115">The center mouse button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed454-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed454-116">Requirements</span></span>



| <span data-ttu-id="ed454-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed454-117">Requirement</span></span> | <span data-ttu-id="ed454-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed454-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed454-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed454-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ed454-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="ed454-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed454-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ed454-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ed454-122">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ed454-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ed454-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ed454-123">End of client support</span></span><br/>    | <span data-ttu-id="ed454-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ed454-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ed454-125">Producto</span><span class="sxs-lookup"><span data-stu-id="ed454-125">Product</span></span><br/>                  | <span data-ttu-id="ed454-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ed454-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ed454-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed454-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed454-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed454-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed454-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed454-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed454-130">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="ed454-130">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

