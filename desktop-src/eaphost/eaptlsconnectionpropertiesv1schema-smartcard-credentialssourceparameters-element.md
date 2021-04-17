---
title: Tarjeta inteligente (CredentialsSourceParameters)
description: Indica que EAP-TLS debe leer el certificado de la tarjeta inteligente.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Elemento de tarjeta inteligente EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714603"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="c1768-104">Tarjeta inteligente (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="c1768-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="c1768-105">El elemento de **tarjeta inteligente (CredentialsSourceParameters)** indica que EAP-TLS debe leer el certificado de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="c1768-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="c1768-106">El elemento de **tarjeta inteligente** se define mediante el tipo complejo de [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1768-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1768-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1768-107">Remarks</span></span>

<span data-ttu-id="c1768-108">Los elementos [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) y **SmartCard** no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="c1768-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1768-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1768-109">Requirements</span></span>



| <span data-ttu-id="c1768-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1768-110">Requirement</span></span> | <span data-ttu-id="c1768-111">Value</span><span class="sxs-lookup"><span data-stu-id="c1768-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1768-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1768-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c1768-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c1768-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1768-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1768-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c1768-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1768-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1768-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1768-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1768-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="c1768-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c1768-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="c1768-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="c1768-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="c1768-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c1768-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="c1768-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="c1768-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c1768-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c1768-122">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="c1768-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c1768-123">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1768-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c1768-124">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1768-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





