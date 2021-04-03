---
title: Estructura de TSMF_SUPPORT_NODEDATA_OUT
description: Se usa dentro de la estructura de salida de datos de soporte de TSMF \_ \_ \_ para contener información acerca de los formatos multimedia admitidos.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_NODEDATA_OUT Servicios de Escritorio remoto
- PTSMF_SUPPORT_NODEDATA_OUT puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905378"
---
# <a name="tsmf_support_nodedata_out-structure"></a><span data-ttu-id="a9e2d-105">TSMF \_ support \_ NODEDATA \_ out Structure</span><span class="sxs-lookup"><span data-stu-id="a9e2d-105">TSMF\_SUPPORT\_NODEDATA\_OUT structure</span></span>

<span data-ttu-id="a9e2d-106">Se usa dentro de la estructura de salida de datos de soporte de TSMF para contener información acerca de los formatos multimedia admitidos. [**\_ \_ \_**](tsmf-support-data-out.md)</span><span class="sxs-lookup"><span data-stu-id="a9e2d-106">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e2d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9e2d-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a><span data-ttu-id="a9e2d-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9e2d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a9e2d-109">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="a9e2d-109">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="a9e2d-110">El nodo.</span><span class="sxs-lookup"><span data-stu-id="a9e2d-110">The node.</span></span>

</dd> <dt>

<span data-ttu-id="a9e2d-111">**hrSupportStatus**</span><span class="sxs-lookup"><span data-stu-id="a9e2d-111">**hrSupportStatus**</span></span>
</dt> <dd>

<span data-ttu-id="a9e2d-112">Indica si se admite el receptor identificado por el parámetro *clsidNewSink* .</span><span class="sxs-lookup"><span data-stu-id="a9e2d-112">Whether the sink identified by the *clsidNewSink* parameter is supported.</span></span>

<span data-ttu-id="a9e2d-113">Los valores posibles son.</span><span class="sxs-lookup"><span data-stu-id="a9e2d-113">The possible values are.</span></span>

<dt>

<span data-ttu-id="a9e2d-114">0</span><span class="sxs-lookup"><span data-stu-id="a9e2d-114">0</span></span>
</dt> <dd>

<span data-ttu-id="a9e2d-115">No compatible</span><span class="sxs-lookup"><span data-stu-id="a9e2d-115">Not supported</span></span>

</dd> <dt>

<span data-ttu-id="a9e2d-116">1</span><span class="sxs-lookup"><span data-stu-id="a9e2d-116">1</span></span>
</dt> <dd>

<span data-ttu-id="a9e2d-117">Compatible</span><span class="sxs-lookup"><span data-stu-id="a9e2d-117">Supported</span></span>

</dd> </dl>

<span data-ttu-id="a9e2d-118">Otros valores son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="a9e2d-118">Other values are undefined.</span></span>

</dd> <dt>

<span data-ttu-id="a9e2d-119">**clsidNewSink**</span><span class="sxs-lookup"><span data-stu-id="a9e2d-119">**clsidNewSink**</span></span>
</dt> <dd>

<span data-ttu-id="a9e2d-120">Receptor asociado al tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a9e2d-120">The sink associated with the media type.</span></span>

</dd> <dt>

<span data-ttu-id="a9e2d-121">**supportedMediaTypeIndex**</span><span class="sxs-lookup"><span data-stu-id="a9e2d-121">**supportedMediaTypeIndex**</span></span>
</dt> <dd>

<span data-ttu-id="a9e2d-122">Índice de base cero del tipo de medio admitido por el receptor.</span><span class="sxs-lookup"><span data-stu-id="a9e2d-122">The zero-based index of the media type supported by the sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9e2d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9e2d-123">Requirements</span></span>



| <span data-ttu-id="a9e2d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9e2d-124">Requirement</span></span> | <span data-ttu-id="a9e2d-125">Value</span><span class="sxs-lookup"><span data-stu-id="a9e2d-125">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="a9e2d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9e2d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e2d-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a9e2d-127">None supported</span></span><br/>         |
| <span data-ttu-id="a9e2d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9e2d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e2d-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9e2d-129">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a9e2d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9e2d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e2d-131">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="a9e2d-131">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="a9e2d-132">**TSMF \_ admiten \_ datos de \_ salida**</span><span class="sxs-lookup"><span data-stu-id="a9e2d-132">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> </dl>

 

 





