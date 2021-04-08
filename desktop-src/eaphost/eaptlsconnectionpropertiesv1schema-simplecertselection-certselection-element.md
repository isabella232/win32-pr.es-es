---
title: Elemento SimpleCertSelection (CertSelection)
description: Obtenga información sobre el elemento SimpleCertSelection (CertSelection). Este elemento determina el modo en que el usuario selecciona un certificado.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Elemento SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078381"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="bb2bb-105">Elemento SimpleCertSelection (CertSelection)</span><span class="sxs-lookup"><span data-stu-id="bb2bb-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="bb2bb-106">El elemento **SimpleCertSelection (CertSelection)** determina el modo en que el usuario selecciona un certificado.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="bb2bb-107">El elemento **SimpleCertSelection** se define mediante el tipo complejo de [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bb2bb-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2bb-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb2bb-108">Remarks</span></span>

<span data-ttu-id="bb2bb-109">**SimpleCertSelection** es true de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="bb2bb-110">Si **SimpleCertSelection** es true, EAP-TLS realiza una búsqueda de certificados simple sin ninguna lista desplegable para la selección de certificados.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="bb2bb-111">Si **SimpleCertSelection** es false, EAP-TLS muestra al usuario el certificado adecuado que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="bb2bb-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2bb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb2bb-112">Requirements</span></span>



| <span data-ttu-id="bb2bb-113">Role</span><span class="sxs-lookup"><span data-stu-id="bb2bb-113">Role</span></span> | <span data-ttu-id="bb2bb-114">Versión mínima del SO admitida</span><span class="sxs-lookup"><span data-stu-id="bb2bb-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="bb2bb-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="bb2bb-115">Client</span></span><br/> | <span data-ttu-id="bb2bb-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bb2bb-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bb2bb-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="bb2bb-117">Server</span></span><br/> | <span data-ttu-id="bb2bb-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bb2bb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bb2bb-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb2bb-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb2bb-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="bb2bb-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bb2bb-121">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="bb2bb-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="bb2bb-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="bb2bb-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bb2bb-123">**CertificateStore (CredentialsSourceParameters)**</span><span class="sxs-lookup"><span data-stu-id="bb2bb-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="bb2bb-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="bb2bb-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="bb2bb-125">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="bb2bb-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bb2bb-126">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="bb2bb-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bb2bb-127">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="bb2bb-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





