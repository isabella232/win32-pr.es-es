---
title: Elemento ConfigBlob (EapHostConfig)
description: Se usa cuando la configuración del método está en formato de BLOB binario en lugar de en formato de cadena de texto.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Elemento ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800920"
---
# <a name="configblob-eaphostconfig-element"></a><span data-ttu-id="a058c-104">Elemento ConfigBlob (EapHostConfig)</span><span class="sxs-lookup"><span data-stu-id="a058c-104">ConfigBlob (EapHostConfig) Element</span></span>

<span data-ttu-id="a058c-105">El elemento **ConfigBlob (EapHostConfig)** se usa cuando la configuración del método está en formato de BLOB binario en lugar de en formato de cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="a058c-105">The **ConfigBlob (EapHostConfig)** element is used when the method configuration is in binary BLOB form instead of text string form.</span></span>

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="a058c-106">El elemento **ConfigBlob** se define mediante el elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a058c-106">The **ConfigBlob** element is defined by the [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a058c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a058c-107">Remarks</span></span>

<span data-ttu-id="a058c-108">Los elementos [**config**](eaphostconfigschema-config-eaphostconfig-element.md) y **ConfigBlob** no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="a058c-108">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and **ConfigBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="a058c-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a058c-109">Requirements</span></span>



| <span data-ttu-id="a058c-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a058c-110">Requirement</span></span> | <span data-ttu-id="a058c-111">Value</span><span class="sxs-lookup"><span data-stu-id="a058c-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a058c-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a058c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a058c-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a058c-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a058c-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a058c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a058c-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a058c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a058c-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="a058c-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="a058c-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a058c-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a058c-118">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="a058c-118">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

<span data-ttu-id="a058c-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="a058c-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a058c-120">**EapHostConfig**</span><span class="sxs-lookup"><span data-stu-id="a058c-120">**EapHostConfig**</span></span>](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[<span data-ttu-id="a058c-121">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="a058c-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a058c-122">Esquema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="a058c-122">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





