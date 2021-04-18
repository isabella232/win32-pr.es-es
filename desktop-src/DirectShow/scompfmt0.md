---
description: Contiene información de formato para la recompresión inteligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Estructura SCompFmt0 (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680190"
---
# <a name="scompfmt0-structure"></a><span data-ttu-id="bf3c0-103">Estructura SCompFmt0</span><span class="sxs-lookup"><span data-stu-id="bf3c0-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="bf3c0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="bf3c0-104">\[Deprecated.</span></span> <span data-ttu-id="bf3c0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bf3c0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bf3c0-106">Contiene información de formato para la recompresión inteligente.</span><span class="sxs-lookup"><span data-stu-id="bf3c0-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf3c0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf3c0-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="bf3c0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf3c0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf3c0-109">**nFormatId**</span><span class="sxs-lookup"><span data-stu-id="bf3c0-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="bf3c0-110">Sector debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="bf3c0-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf3c0-111">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="bf3c0-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="bf3c0-112">[**AM \_ Estructura de \_ tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type) que describe el formato de compresión.</span><span class="sxs-lookup"><span data-stu-id="bf3c0-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf3c0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf3c0-113">Requirements</span></span>



| <span data-ttu-id="bf3c0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf3c0-114">Requirement</span></span> | <span data-ttu-id="bf3c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="bf3c0-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3c0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf3c0-116">Header</span></span><br/> | <dl> <span data-ttu-id="bf3c0-117"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf3c0-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf3c0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf3c0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf3c0-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="bf3c0-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="bf3c0-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="bf3c0-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




