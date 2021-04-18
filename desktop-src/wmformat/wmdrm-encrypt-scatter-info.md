---
title: WMDRM_ENCRYPT_SCATTER_INFO estructura (wmdrmsdk. h)
description: La \_ \_ \_ estructura de la información de dispersión cifrada de WMDRM contiene información necesaria para configurar la interfaz IWMDRMEncryptScatter para su uso.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721587"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="e19ae-105">\_Estructura de \_ información de dispersión cifrada de WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="e19ae-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="e19ae-106">La estructura de la **\_ \_ \_ información de dispersión cifrada de WMDRM** contiene información necesaria para configurar la interfaz [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para su uso.</span><span class="sxs-lookup"><span data-stu-id="e19ae-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="e19ae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e19ae-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="e19ae-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e19ae-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e19ae-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="e19ae-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="e19ae-110">Identificador de la secuencia que se va a cifrar.</span><span class="sxs-lookup"><span data-stu-id="e19ae-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="e19ae-111">**dwSampleProtectionVersion**</span><span class="sxs-lookup"><span data-stu-id="e19ae-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e19ae-112">Versión de protección de ejemplo que se va a usar para codificar los datos de la secuencia especificada.</span><span class="sxs-lookup"><span data-stu-id="e19ae-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="e19ae-113">**cbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e19ae-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e19ae-114">Tamaño del búfer de **pbProtectionInfo** en bytes.</span><span class="sxs-lookup"><span data-stu-id="e19ae-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e19ae-115">**pbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="e19ae-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="e19ae-116">Búfer que contiene información de protección adicional.</span><span class="sxs-lookup"><span data-stu-id="e19ae-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e19ae-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e19ae-117">Remarks</span></span>

<span data-ttu-id="e19ae-118">El método [**IWMDRMEncryptScatter:: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="e19ae-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e19ae-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e19ae-119">Requirements</span></span>



| <span data-ttu-id="e19ae-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e19ae-120">Requirement</span></span> | <span data-ttu-id="e19ae-121">Value</span><span class="sxs-lookup"><span data-stu-id="e19ae-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e19ae-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e19ae-122">Header</span></span><br/> | <dl> <span data-ttu-id="e19ae-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e19ae-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e19ae-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e19ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19ae-125">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="e19ae-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





