---
title: Estructura de TSMF_SUPPORT_NODEDATA_IN
description: Se utiliza dentro de \_ los \_ datos \_ de soporte de TSMF en la estructura para contener información acerca de los formatos multimedia admitidos.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_NODEDATA_IN Servicios de Escritorio remoto
- PTSMF_SUPPORT_NODEDATA_IN puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686012"
---
# <a name="tsmf_support_nodedata_in-structure"></a><span data-ttu-id="e17de-105">TSMF \_ admite \_ NODEDATA \_ en la estructura</span><span class="sxs-lookup"><span data-stu-id="e17de-105">TSMF\_SUPPORT\_NODEDATA\_IN structure</span></span>

<span data-ttu-id="e17de-106">Se utiliza dentro de los [**\_ \_ datos \_ de soporte de TSMF en**](tsmf-support-data-in.md) la estructura para contener información acerca de los formatos multimedia admitidos.</span><span class="sxs-lookup"><span data-stu-id="e17de-106">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="e17de-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e17de-107">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a><span data-ttu-id="e17de-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e17de-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e17de-109">**byteCount**</span><span class="sxs-lookup"><span data-stu-id="e17de-109">**byteCount**</span></span>
</dt> <dd>

<span data-ttu-id="e17de-110">Tamaño de la estructura en bytes.</span><span class="sxs-lookup"><span data-stu-id="e17de-110">The size of the structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e17de-111">**nodeId**</span><span class="sxs-lookup"><span data-stu-id="e17de-111">**nodeId**</span></span>
</dt> <dd>

<span data-ttu-id="e17de-112">El nodo.</span><span class="sxs-lookup"><span data-stu-id="e17de-112">The node.</span></span>

</dd> <dt>

<span data-ttu-id="e17de-113">**numMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e17de-113">**numMediaTypes**</span></span>
</dt> <dd>

<span data-ttu-id="e17de-114">Número de estructuras de formato multimedia.</span><span class="sxs-lookup"><span data-stu-id="e17de-114">The number of media format structures.</span></span>

</dd> <dt>

<span data-ttu-id="e17de-115">**...**</span><span class="sxs-lookup"><span data-stu-id="e17de-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="e17de-116">Un número variable de estructuras que definen formatos multimedia de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="e17de-116">A variable number of structures defining audio or video media formats.</span></span> <span data-ttu-id="e17de-117">El **formatType** es **format \_ WaveFormatEx** para audio o **format \_ MFVideoFormat** para vídeo.</span><span class="sxs-lookup"><span data-stu-id="e17de-117">The **FormatType** is either **FORMAT\_WaveFormatEx** for audio or **FORMAT\_MFVideoFormat** for video.</span></span>

<span data-ttu-id="e17de-118">Para más información sobre esta estructura, consulte la [estructura de tipo de medio de TS \_ AM \_ \_ ](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span><span class="sxs-lookup"><span data-stu-id="e17de-118">For details of this structure, see [TS\_AM\_MEDIA\_TYPE Structure](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e17de-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e17de-119">Requirements</span></span>



| <span data-ttu-id="e17de-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e17de-120">Requirement</span></span> | <span data-ttu-id="e17de-121">Value</span><span class="sxs-lookup"><span data-stu-id="e17de-121">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="e17de-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e17de-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e17de-123">None supported</span></span><br/>         |
| <span data-ttu-id="e17de-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e17de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e17de-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e17de-125">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e17de-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e17de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17de-127">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="e17de-127">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="e17de-128">**TSMF \_ admiten \_ datos \_ en**</span><span class="sxs-lookup"><span data-stu-id="e17de-128">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> </dl>

 

