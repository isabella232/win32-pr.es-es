---
title: Enumeración VMDisplayVideoMode (VPCCOMInterfaces. h)
description: Especifica el modo de visualización de vídeo.
ms.assetid: 9ffd1bb5-115d-4554-92c6-5dcf86f904a5
keywords:
- Enumeración de VMDisplayVideoMode Virtual PC
topic_type:
- apiref
api_name:
- VMDisplayVideoMode
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b159a8c251c83643ae9897842b313ea9be567e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490438"
---
# <a name="vmdisplayvideomode-enumeration"></a><span data-ttu-id="7421f-104">Enumeración VMDisplayVideoMode</span><span class="sxs-lookup"><span data-stu-id="7421f-104">VMDisplayVideoMode enumeration</span></span>

<span data-ttu-id="7421f-105">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7421f-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7421f-106">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7421f-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7421f-107">Especifica el modo de visualización de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7421f-107">Specifies the display video mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="7421f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7421f-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVideoMode_TextMode  = 0,
  vmVideoMode_CGAMode   = 1,
  vmVideoMode_VGAMode   = 2,
  vmVideoMode_SVGAMode  = 3
} VMDisplayVideoMode;
```



## <a name="constants"></a><span data-ttu-id="7421f-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="7421f-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7421f-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode \_ textmode**</span><span class="sxs-lookup"><span data-stu-id="7421f-110"><span id="vmVideoMode_TextMode"></span><span id="vmvideomode_textmode"></span><span id="VMVIDEOMODE_TEXTMODE"></span>**vmVideoMode\_TextMode**</span></span>
</dt> <dd>

<span data-ttu-id="7421f-111">Modo de texto.</span><span class="sxs-lookup"><span data-stu-id="7421f-111">Text mode.</span></span>

</dd> <dt>

<span data-ttu-id="7421f-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode \_ CGAMode**</span><span class="sxs-lookup"><span data-stu-id="7421f-112"><span id="vmVideoMode_CGAMode"></span><span id="vmvideomode_cgamode"></span><span id="VMVIDEOMODE_CGAMODE"></span>**vmVideoMode\_CGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="7421f-113">Modo CGA.</span><span class="sxs-lookup"><span data-stu-id="7421f-113">CGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="7421f-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode \_ VGAMode**</span><span class="sxs-lookup"><span data-stu-id="7421f-114"><span id="vmVideoMode_VGAMode"></span><span id="vmvideomode_vgamode"></span><span id="VMVIDEOMODE_VGAMODE"></span>**vmVideoMode\_VGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="7421f-115">Modo VGA.</span><span class="sxs-lookup"><span data-stu-id="7421f-115">VGA mode.</span></span>

</dd> <dt>

<span data-ttu-id="7421f-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode \_ SVGAMode**</span><span class="sxs-lookup"><span data-stu-id="7421f-116"><span id="vmVideoMode_SVGAMode"></span><span id="vmvideomode_svgamode"></span><span id="VMVIDEOMODE_SVGAMODE"></span>**vmVideoMode\_SVGAMode**</span></span>
</dt> <dd>

<span data-ttu-id="7421f-117">Modo SVGA.</span><span class="sxs-lookup"><span data-stu-id="7421f-117">SVGA mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7421f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7421f-118">Requirements</span></span>



| <span data-ttu-id="7421f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7421f-119">Requirement</span></span> | <span data-ttu-id="7421f-120">Value</span><span class="sxs-lookup"><span data-stu-id="7421f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7421f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7421f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7421f-122">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="7421f-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7421f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7421f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7421f-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7421f-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7421f-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7421f-125">End of client support</span></span><br/>    | <span data-ttu-id="7421f-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7421f-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7421f-127">Producto</span><span class="sxs-lookup"><span data-stu-id="7421f-127">Product</span></span><br/>                  | <span data-ttu-id="7421f-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7421f-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7421f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7421f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7421f-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7421f-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7421f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="7421f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7421f-132">**IVMDisplay:: VideoMode**</span><span class="sxs-lookup"><span data-stu-id="7421f-132">**IVMDisplay::VideoMode**</span></span>](ivmdisplay-videomode.md)
</dt> </dl>

 

