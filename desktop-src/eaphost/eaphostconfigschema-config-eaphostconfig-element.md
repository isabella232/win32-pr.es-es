---
title: Elemento config (EapHostConfig)
description: Se usa cuando la configuración del método está en formato de texto XML en lugar de un BLOB binario.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento de configuración EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491062"
---
# <a name="config-eaphostconfig-element"></a><span data-ttu-id="98d66-104">Elemento config (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="98d66-104">Config (EapHostConfig) Element</span></span>

<span data-ttu-id="98d66-105">El elemento de **configuración (EapHostConfig)** se usa cuando la configuración del método está en formato de texto XML en lugar de un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="98d66-105">The **Config (EapHostConfig)** element is used when the method configuration is in XML text form instead of a binary BLOB.</span></span>

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

<span data-ttu-id="98d66-106">El elemento de **configuración** se define mediante el elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="98d66-106">The **Config** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="98d66-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98d66-107">Remarks</span></span>

<span data-ttu-id="98d66-108">Los elementos **config** y [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="98d66-108">The **Config** and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d66-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d66-109">Requirements</span></span>



| <span data-ttu-id="98d66-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d66-110">Requirement</span></span> | <span data-ttu-id="98d66-111">Value</span><span class="sxs-lookup"><span data-stu-id="98d66-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98d66-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98d66-112">Minimum supported client</span></span><br/> | <span data-ttu-id="98d66-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="98d66-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98d66-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98d66-114">Minimum supported server</span></span><br/> | <span data-ttu-id="98d66-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="98d66-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98d66-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="98d66-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="98d66-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="98d66-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="98d66-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="98d66-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="98d66-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="98d66-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="98d66-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="98d66-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="98d66-121">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="98d66-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="98d66-122">Esquema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="98d66-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





