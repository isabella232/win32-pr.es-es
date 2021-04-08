---
title: Elemento EapType
description: Es un tipo derivado del elemento EapType del esquema BaseEapConnectionProperties. | Elemento EapType
ms.assetid: cf92d500-f815-48e2-a7d5-1364cb13a1f0
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d1fdb4026c72b99bf2434a9fd6937743a9edb40
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003571"
---
# <a name="eaptype-element"></a><span data-ttu-id="666c9-105">Elemento EapType</span><span class="sxs-lookup"><span data-stu-id="666c9-105">EapType Element</span></span>

<span data-ttu-id="666c9-106">El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) del esquema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="666c9-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="666c9-107">Este elemento **EapType** derivado contiene los siguientes elementos: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)y [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span><span class="sxs-lookup"><span data-stu-id="666c9-107">This derived **EapType** element contains the following elements: [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md), [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md), [**PerformServerValidation**](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md), [**AcceptServerName**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md), and [**TLSExtensions**](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md).</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="CredentialsSource"
                        type="CredentialsSourceParameters"
                        minOccurs="0"
                     />
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="DifferentUsername"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: PerformServerValidation"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: AcceptServerName"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="1"
                        ref="extendedTLS: TLSExtensions"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="666c9-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="666c9-108">Child elements</span></span>



| <span data-ttu-id="666c9-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="666c9-109">Element</span></span>                                                                                                                               | <span data-ttu-id="666c9-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="666c9-110">Type</span></span>                                                                                                              | <span data-ttu-id="666c9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="666c9-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="666c9-112">**extendedTLS: PerformServerValidation**</span><span class="sxs-lookup"><span data-stu-id="666c9-112">**extendedTLS: PerformServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-performservervalidation-peapextensionstype-element.md) |                                                                                                                   | <span data-ttu-id="666c9-113">Windows 7 y versiones posteriores: indica si se realiza la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="666c9-113">Windows 7 and later: indicates whether server validation is performed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="666c9-114">**extendedTLS: AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="666c9-114">**extendedTLS: AcceptServerName**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)              |                                                                                                                   | <span data-ttu-id="666c9-115">Windows 7 y versiones posteriores: indica si se lee el nombre de un servidor.</span><span class="sxs-lookup"><span data-stu-id="666c9-115">Windows 7 and later: indicates whether the name of a server is read.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="666c9-116">**extendedTLS: TLSExtensions**</span><span class="sxs-lookup"><span data-stu-id="666c9-116">**extendedTLS: TLSExtensions**</span></span>](eaptlsconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)                  |                                                                                                                   | <span data-ttu-id="666c9-117">Windows 7 y versiones posteriores: permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="666c9-117">Windows 7 and later: enables future enhancements to the schema.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="666c9-118">**CredentialsSource**</span><span class="sxs-lookup"><span data-stu-id="666c9-118">**CredentialsSource**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)                                     | [<span data-ttu-id="666c9-119">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="666c9-119">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) | <span data-ttu-id="666c9-120">Contiene información acerca de la ubicación del certificado de seguridad de nivel de transporte (EAP-TLS) de EAP.</span><span class="sxs-lookup"><span data-stu-id="666c9-120">Contains information about the location of the EAP Transport Level Security (EAP-TLS) certificate.</span></span> <br/> <span data-ttu-id="666c9-121">El elemento [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="666c9-121">The [**CredentialsSource**](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="666c9-122">**DifferentUsername**</span><span class="sxs-lookup"><span data-stu-id="666c9-122">**DifferentUsername**</span></span>](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md)                                     | <span data-ttu-id="666c9-123">boolean</span><span class="sxs-lookup"><span data-stu-id="666c9-123">boolean</span></span>                                                                                                           | <span data-ttu-id="666c9-124">Determina el nombre de usuario EAP-TLS que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="666c9-124">Determines which user name EAP-TLS is to use.</span></span> <br/> <span data-ttu-id="666c9-125">Si el elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) es **true**, EAP-TLS debe usar un nombre de usuario distinto del nombre que aparece en el certificado.</span><span class="sxs-lookup"><span data-stu-id="666c9-125">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **TRUE**, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="666c9-126">Si el elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) es **false**, EAP-TLS usa el nombre de usuario que aparece en el certificado.</span><span class="sxs-lookup"><span data-stu-id="666c9-126">If the [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is **FALSE**, EAP-TLS uses the user name that appears on the certificate.</span></span><br/> <span data-ttu-id="666c9-127">El elemento [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="666c9-127">The [**DifferentUsername**](eaptlsconnectionpropertiesv1schema-differentusername-eaptype-element.md) element is optional.</span></span> <br/> |
| [<span data-ttu-id="666c9-128">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="666c9-128">**ServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)                                       | [<span data-ttu-id="666c9-129">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="666c9-129">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)   | <span data-ttu-id="666c9-130">Contiene información sobre cómo realizar la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="666c9-130">Contains information about how to perform server validation.</span></span> <span data-ttu-id="666c9-131">El elemento [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="666c9-131">The [**ServerValidation**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="requirements"></a><span data-ttu-id="666c9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="666c9-132">Requirements</span></span>



| <span data-ttu-id="666c9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="666c9-133">Requirement</span></span> | <span data-ttu-id="666c9-134">Value</span><span class="sxs-lookup"><span data-stu-id="666c9-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="666c9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="666c9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="666c9-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="666c9-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="666c9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="666c9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="666c9-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="666c9-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="666c9-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="666c9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666c9-140">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="666c9-140">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="666c9-141">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="666c9-141">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="666c9-142">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="666c9-142">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





