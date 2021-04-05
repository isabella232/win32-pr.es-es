---
title: Elemento EapHostConfig
description: Contiene el elemento EapMethod y el elemento config o ConfigBlob. Los elementos config y ConfigBlob no se pueden usar simultáneamente.
ms.assetid: 6c42d71e-0c61-48e4-a447-cfd1eae90297
keywords:
- Elemento EapHostConfig EAPHost
topic_type:
- apiref
api_name:
- EapHostConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 125b5fa2cab8bf3f9da12bd842a1a102beee3fb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078794"
---
# <a name="eaphostconfig-element"></a><span data-ttu-id="388fb-105">Elemento EapHostConfig</span><span class="sxs-lookup"><span data-stu-id="388fb-105">EapHostConfig Element</span></span>

<span data-ttu-id="388fb-106">El elemento **EapHostConfig** contiene el elemento [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) y el elemento [**config**](eaphostconfigschema-config-eaphostconfig-element.md) o [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="388fb-106">The **EapHostConfig** element contains the [**EapMethod**](eaphostconfigschema-eapmethod-eaphostconfig-element.md) element and [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) or [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) element.</span></span>

<span data-ttu-id="388fb-107">Los elementos [**config**](eaphostconfigschema-config-eaphostconfig-element.md) y [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="388fb-107">The [**Config**](eaphostconfigschema-config-eaphostconfig-element.md) and [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) elements cannot both be used simultaneously.</span></span>

``` syntax
<xs:element name="EapHostConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Config"
                    type="BaseEapMethodConfig"
                 />
                <xs:element name="ConfigBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="388fb-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="388fb-108">Child elements</span></span>



| <span data-ttu-id="388fb-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="388fb-109">Element</span></span>                                                                    | <span data-ttu-id="388fb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="388fb-110">Type</span></span>                                                                                     | <span data-ttu-id="388fb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="388fb-111">Description</span></span>                                                                                          |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="388fb-112">**Configurar**</span><span class="sxs-lookup"><span data-stu-id="388fb-112">**Config**</span></span>](eaphostconfigschema-config-eaphostconfig-element.md)         | [<span data-ttu-id="388fb-113">**BaseEapMethodConfig**</span><span class="sxs-lookup"><span data-stu-id="388fb-113">**BaseEapMethodConfig**</span></span>](baseeapmethodconfigschema-baseeapmethodconfig-complextype.md) | <span data-ttu-id="388fb-114">Se usa cuando la configuración del método está en formato de texto XML en lugar de un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="388fb-114">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>       |
| [<span data-ttu-id="388fb-115">**ConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="388fb-115">**ConfigBlob**</span></span>](eaphostconfigschema-configblob-eaphostconfig-element.md) | <span data-ttu-id="388fb-116">hexBinary</span><span class="sxs-lookup"><span data-stu-id="388fb-116">hexBinary</span></span>                                                                                | <span data-ttu-id="388fb-117">Se usa cuando la configuración del método está en formato de BLOB binario en lugar de en formato de texto de cadena.</span><span class="sxs-lookup"><span data-stu-id="388fb-117">Is used when the method configuration is in binary BLOB form instead of string text form.</span></span><br/> |
| [<span data-ttu-id="388fb-118">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="388fb-118">**EapMethod**</span></span>](eaphostconfigschema-eapmethod-eaphostconfig-element.md)   | [<span data-ttu-id="388fb-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="388fb-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                       | <span data-ttu-id="388fb-120">Identifica el método al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="388fb-120">Identifies the method being referred to.</span></span> <br/>                                                 |



## <a name="remarks"></a><span data-ttu-id="388fb-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="388fb-121">Remarks</span></span>

<span data-ttu-id="388fb-122">El elemento **processContents** permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="388fb-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="388fb-123">El elemento **processContents** es opcional.</span><span class="sxs-lookup"><span data-stu-id="388fb-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="388fb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="388fb-124">Requirements</span></span>



| <span data-ttu-id="388fb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="388fb-125">Requirement</span></span> | <span data-ttu-id="388fb-126">Value</span><span class="sxs-lookup"><span data-stu-id="388fb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="388fb-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="388fb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="388fb-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="388fb-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="388fb-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="388fb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="388fb-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="388fb-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="388fb-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="388fb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="388fb-132">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="388fb-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="388fb-133">Esquema eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="388fb-133">eaphostconfig Schema</span></span>](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





