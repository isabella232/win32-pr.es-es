---
title: Estructura de TSMF_SUPPORT_DATA_IN
description: Contiene información acerca de los formatos de medios. | Estructura de TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_DATA_IN Servicios de Escritorio remoto
- PTSMF_SUPPORT_DATA_IN puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689776"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="b35dc-106">TSMF \_ admiten \_ datos \_ en la estructura</span><span class="sxs-lookup"><span data-stu-id="b35dc-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="b35dc-107">Contiene información acerca de los formatos de medios.</span><span class="sxs-lookup"><span data-stu-id="b35dc-107">Contains information about media formats.</span></span> <span data-ttu-id="b35dc-108">El método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) usa esta estructura durante las consultas **\_ \_ \_ \_ compatibles con el formato MF de la consulta Wrds** .</span><span class="sxs-lookup"><span data-stu-id="b35dc-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="b35dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b35dc-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="b35dc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b35dc-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b35dc-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="b35dc-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="b35dc-112">La sesión.</span><span class="sxs-lookup"><span data-stu-id="b35dc-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="b35dc-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="b35dc-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b35dc-114">El número de estructuras en los datos de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="b35dc-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="b35dc-115">**...**</span><span class="sxs-lookup"><span data-stu-id="b35dc-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="b35dc-116">Número variable de estructuras que contienen datos de formato multimedia.</span><span class="sxs-lookup"><span data-stu-id="b35dc-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b35dc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b35dc-117">Requirements</span></span>



| <span data-ttu-id="b35dc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b35dc-118">Requirement</span></span> | <span data-ttu-id="b35dc-119">Value</span><span class="sxs-lookup"><span data-stu-id="b35dc-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b35dc-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b35dc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b35dc-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b35dc-121">None supported</span></span><br/>         |
| <span data-ttu-id="b35dc-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b35dc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b35dc-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b35dc-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b35dc-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b35dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b35dc-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="b35dc-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="b35dc-126">**TSMF \_ admite \_ NODEDATA \_ en**</span><span class="sxs-lookup"><span data-stu-id="b35dc-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





