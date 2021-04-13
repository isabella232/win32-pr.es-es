---
title: Elemento CertificateStore (CredentialsSourceParameters)
description: Indica que EAP-TLS debe leer el certificado del almacén My del usuario o el equipo que se va a autenticar.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Elemento CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534719"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="7c1ad-104">Elemento CertificateStore (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="7c1ad-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="7c1ad-105">El elemento **CertificateStore (CredentialsSourceParameters)** indica que EAP-TLS debe leer el certificado del almacén My del usuario o el equipo que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="7c1ad-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="7c1ad-106">El elemento **CertificateStore** se define mediante el tipo complejo de [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7c1ad-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c1ad-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c1ad-107">Remarks</span></span>

<span data-ttu-id="7c1ad-108">Los elementos **CertificateStore** y [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="7c1ad-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c1ad-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c1ad-109">Requirements</span></span>



| <span data-ttu-id="7c1ad-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c1ad-110">Requirement</span></span> | <span data-ttu-id="7c1ad-111">Value</span><span class="sxs-lookup"><span data-stu-id="7c1ad-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c1ad-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c1ad-112">Minimum supported client</span></span><br/> | <span data-ttu-id="7c1ad-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7c1ad-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7c1ad-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c1ad-114">Minimum supported server</span></span><br/> | <span data-ttu-id="7c1ad-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c1ad-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c1ad-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c1ad-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c1ad-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="7c1ad-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7c1ad-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="7c1ad-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="7c1ad-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="7c1ad-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7c1ad-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="7c1ad-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="7c1ad-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="7c1ad-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="7c1ad-122">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="7c1ad-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="7c1ad-123">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7c1ad-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="7c1ad-124">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="7c1ad-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





