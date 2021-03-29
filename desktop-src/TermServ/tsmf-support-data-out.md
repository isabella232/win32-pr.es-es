---
title: Estructura de TSMF_SUPPORT_DATA_OUT
description: Contiene información acerca de los formatos de medios. | Estructura de TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- Estructura de TSMF_SUPPORT_DATA_OUT Servicios de Escritorio remoto
- PTSMF_SUPPORT_DATA_OUT puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003536"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="b2382-106">\_Estructura de \_ salida de datos de TSMF support \_</span><span class="sxs-lookup"><span data-stu-id="b2382-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="b2382-107">Contiene información acerca de los formatos de medios.</span><span class="sxs-lookup"><span data-stu-id="b2382-107">Contains information about media formats.</span></span> <span data-ttu-id="b2382-108">El método [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) usa esta estructura durante las consultas **\_ \_ \_ \_ compatibles con el formato MF de la consulta Wrds** .</span><span class="sxs-lookup"><span data-stu-id="b2382-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2382-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2382-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="b2382-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2382-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2382-111">**guidMfSession**</span><span class="sxs-lookup"><span data-stu-id="b2382-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="b2382-112">Debe coincidir con la propiedad **guidMfSession** en los [**\_ \_ datos de soporte \_ de TSMF correspondientes en**](tsmf-support-data-in.md) la estructura.</span><span class="sxs-lookup"><span data-stu-id="b2382-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2382-113">**numEntries**</span><span class="sxs-lookup"><span data-stu-id="b2382-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="b2382-114">El número de estructuras en los datos de longitud variable.</span><span class="sxs-lookup"><span data-stu-id="b2382-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="b2382-115">**...**</span><span class="sxs-lookup"><span data-stu-id="b2382-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="b2382-116">Número variable de estructuras que contienen datos de formato multimedia.</span><span class="sxs-lookup"><span data-stu-id="b2382-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2382-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2382-117">Requirements</span></span>



| <span data-ttu-id="b2382-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2382-118">Requirement</span></span> | <span data-ttu-id="b2382-119">Value</span><span class="sxs-lookup"><span data-stu-id="b2382-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="b2382-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2382-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b2382-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2382-121">None supported</span></span><br/>         |
| <span data-ttu-id="b2382-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2382-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b2382-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b2382-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2382-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2382-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2382-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="b2382-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="b2382-126">**\_compatibilidad con TSMF \_ NODEDATA \_ out**</span><span class="sxs-lookup"><span data-stu-id="b2382-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





