---
description: Especifica el nivel de protección del contenido de vídeo.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696156"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="8995d-103">Estructura de marcas de \_ protección de D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="8995d-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="8995d-104">Especifica el nivel de protección del contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8995d-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="8995d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8995d-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="8995d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="8995d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8995d-107">**ProtectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="8995d-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="8995d-108">Si es 1, se habilita la protección de contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8995d-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="8995d-109">**OverlayOrFullscreenRequired**</span><span class="sxs-lookup"><span data-stu-id="8995d-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="8995d-110">Si es 1, la aplicación requiere que el vídeo se muestre mediante una superposición de hardware o el modo exclusivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8995d-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="8995d-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="8995d-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="8995d-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8995d-112">Reserved.</span></span> <span data-ttu-id="8995d-113">Establezca todos los bits en cero.</span><span class="sxs-lookup"><span data-stu-id="8995d-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8995d-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8995d-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="8995d-115">Utilice este miembro para tener acceso a todos los bits de la Unión.</span><span class="sxs-lookup"><span data-stu-id="8995d-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8995d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8995d-116">Requirements</span></span>



| <span data-ttu-id="8995d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8995d-117">Requirement</span></span> | <span data-ttu-id="8995d-118">Value</span><span class="sxs-lookup"><span data-stu-id="8995d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8995d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8995d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8995d-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8995d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8995d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8995d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8995d-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8995d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8995d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8995d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8995d-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8995d-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8995d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8995d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8995d-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8995d-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




