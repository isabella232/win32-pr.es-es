---
description: Contiene la respuesta a una consulta de D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT estructura (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720294"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a><span data-ttu-id="8a935-103">Estructura de salida de D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_</span><span class="sxs-lookup"><span data-stu-id="8a935-103">D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="8a935-104">Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="8a935-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) query.</span></span>

<span data-ttu-id="8a935-105">Para enviar esta consulta, llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="8a935-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a935-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a935-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="8a935-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a935-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a935-108">**Salida**</span><span class="sxs-lookup"><span data-stu-id="8a935-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="8a935-109">Una estructura de [**\_ \_ salida de consulta de D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) que contiene un código de autentificación de mensajes (Mac) (Mac) y otros datos.</span><span class="sxs-lookup"><span data-stu-id="8a935-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="8a935-110">**BusType**</span><span class="sxs-lookup"><span data-stu-id="8a935-110">**BusType**</span></span>
</dt> <dd>

<span data-ttu-id="8a935-111">Una operación **OR bit a bit** de marcas de la enumeración [**D3DBUSTYPE**](d3dbustype.md) .</span><span class="sxs-lookup"><span data-stu-id="8a935-111">A bitwise **OR** of flags from the [**D3DBUSTYPE**](d3dbustype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="8a935-112">**bAccessibleInContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="8a935-112">**bAccessibleInContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="8a935-113">Si **es true**, los bloques contiguos de memoria de vídeo pueden estar accesibles para la CPU o el bus.</span><span class="sxs-lookup"><span data-stu-id="8a935-113">If **TRUE**, contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> <dt>

<span data-ttu-id="8a935-114">**bAccessibleInNonContiguousBlocks**</span><span class="sxs-lookup"><span data-stu-id="8a935-114">**bAccessibleInNonContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="8a935-115">Si **es true**, los bloques no contiguos de memoria de vídeo pueden estar accesibles para la CPU o el bus.</span><span class="sxs-lookup"><span data-stu-id="8a935-115">If **TRUE**, non-contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a935-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a935-116">Requirements</span></span>



| <span data-ttu-id="8a935-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a935-117">Requirement</span></span> | <span data-ttu-id="8a935-118">Value</span><span class="sxs-lookup"><span data-stu-id="8a935-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a935-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a935-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8a935-120">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a935-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8a935-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a935-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8a935-122">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a935-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8a935-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a935-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a935-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a935-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a935-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a935-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a935-126">Estructuras de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8a935-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="8a935-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="8a935-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




