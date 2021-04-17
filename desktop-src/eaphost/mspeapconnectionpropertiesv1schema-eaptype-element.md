---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Este elemento es un tipo derivado del elemento EapType del esquema BaseEapConnectionProperties. Para mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 3336e943170afa0ec1f239d4cf7a0c603a0c8e71
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187754"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a><span data-ttu-id="0a8bc-105">Elemento EapType (mspeapconnectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="0a8bc-105">EapType element (mspeapconnectionpropertiesv1schema)</span></span>

<span data-ttu-id="0a8bc-106">El elemento **EapType** es un tipo derivado del elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) del esquema [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="0a8bc-106">The **EapType** element is a derived type of the [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [BaseEapConnectionProperties](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span>

<span data-ttu-id="0a8bc-107">Este elemento **EapType** derivado contiene los siguientes elementos: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) y [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span><span class="sxs-lookup"><span data-stu-id="0a8bc-107">This derived **EapType** element contains the following elements: [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md), [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md), [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md), [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md), [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) and [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md).</span></span>

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="0a8bc-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0a8bc-108">Child elements</span></span>



| <span data-ttu-id="0a8bc-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="0a8bc-109">Element</span></span>                                                                                                     | <span data-ttu-id="0a8bc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a8bc-110">Type</span></span>                                                                                                            | <span data-ttu-id="0a8bc-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a8bc-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a8bc-112">**Participante**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-112">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | <span data-ttu-id="0a8bc-113">Describe el método interno y la configuración del método.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-113">Describes the inner method and the method configuration.</span></span> <span data-ttu-id="0a8bc-114">Si el elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es true, el elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar presente.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-114">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present.</span></span> <span data-ttu-id="0a8bc-115">Si el elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es false, el elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar ausente.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-115">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is FALSE, the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be absent.</span></span><br/>           |
| [<span data-ttu-id="0a8bc-116">**EnableQuarantineChecks**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-116">**EnableQuarantineChecks**</span></span>](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | <span data-ttu-id="0a8bc-117">boolean</span><span class="sxs-lookup"><span data-stu-id="0a8bc-117">boolean</span></span>                                                                                                         | <span data-ttu-id="0a8bc-118">Indica si se deben realizar comprobaciones de protección de acceso a redes (NAP).</span><span class="sxs-lookup"><span data-stu-id="0a8bc-118">Indicates whether to perform Network Access Protection (NAP) checks.</span></span> <span data-ttu-id="0a8bc-119">Si el elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) es true, PEAP realizará comprobaciones de NAP; Si FALSE PEAP no realiza comprobaciones de NAP.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-119">If the [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is TRUE, then PEAP will perform NAP checks; if FALSE PEAP will not perform NAP checks.</span></span> <span data-ttu-id="0a8bc-120">El elemento [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-120">The [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) element is optional.</span></span><br/>                                                                                |
| [<span data-ttu-id="0a8bc-121">**FastReconnect**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-121">**FastReconnect**</span></span>](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | <span data-ttu-id="0a8bc-122">boolean</span><span class="sxs-lookup"><span data-stu-id="0a8bc-122">boolean</span></span>                                                                                                         | <span data-ttu-id="0a8bc-123">Indica si se debe realizar una reconexión rápida.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-123">Indicates whether to perform a fast reconnect.</span></span> <span data-ttu-id="0a8bc-124">Si el elemento [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) es true, PEAP intenta realizar una reconexión rápida. Si es FALSE, PEAP realiza la autenticación completa.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-124">If the [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="0a8bc-125">El elemento [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-125">The [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="0a8bc-126">**IdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-126">**IdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [<span data-ttu-id="0a8bc-127">**IdentityPrivacyParameters**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-127">**IdentityPrivacyParameters**</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | <span data-ttu-id="0a8bc-128">Windows 7 o posterior: indica si se envía una identidad verdadera o una identidad anónima de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-128">Windows 7 or later: Indicates whether a user's true identity or an anonymous identity is sent.</span></span> <span data-ttu-id="0a8bc-129">El elemento [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-129">The [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="0a8bc-130">**InnerEapOptional**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-130">**InnerEapOptional**</span></span>](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | <span data-ttu-id="0a8bc-131">boolean</span><span class="sxs-lookup"><span data-stu-id="0a8bc-131">boolean</span></span>                                                                                                         | <span data-ttu-id="0a8bc-132">Indica si se va a realizar el acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-132">Indicates whether to perform GUEST access.</span></span> <span data-ttu-id="0a8bc-133">Si el elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es true, el elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar presente y describir el método interno y su configuración; Si es FALSE, PEAP realizará el acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-133">If the [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and its configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="0a8bc-134">El elemento [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-134">The [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) element is optional.</span></span><br/>            |
| [<span data-ttu-id="0a8bc-135">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-135">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [<span data-ttu-id="0a8bc-136">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-136">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | <span data-ttu-id="0a8bc-137">El elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) permite futuras mejoras en el esquema.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-137">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element enables future enhancements to the schema.</span></span> <span data-ttu-id="0a8bc-138">El elemento [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-138">The [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="0a8bc-139">**RequireCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-139">**RequireCryptoBinding**</span></span>](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | <span data-ttu-id="0a8bc-140">boolean</span><span class="sxs-lookup"><span data-stu-id="0a8bc-140">boolean</span></span>                                                                                                         | <span data-ttu-id="0a8bc-141">Indica si se va a autenticar con servidores que admiten cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-141">Indicates whether to authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="0a8bc-142">Si el elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) es true, PEAP se autenticará con servidores que no admitan cryptobinding; Si es FALSE, PEAP solo se autenticará con servidores que admitan cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-142">If the [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="0a8bc-143">El elemento [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-143">The [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="0a8bc-144">**ServerValidation**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-144">**ServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [<span data-ttu-id="0a8bc-145">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="0a8bc-145">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | <span data-ttu-id="0a8bc-146">Contiene información sobre cómo realizar la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-146">Contains information about how to perform server validation.</span></span> <span data-ttu-id="0a8bc-147">El elemento [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a8bc-147">The [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="0a8bc-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a8bc-148">Requirements</span></span>



| <span data-ttu-id="0a8bc-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a8bc-149">Requirement</span></span> | <span data-ttu-id="0a8bc-150">Value</span><span class="sxs-lookup"><span data-stu-id="0a8bc-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a8bc-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a8bc-151">Minimum supported client</span></span><br/> | <span data-ttu-id="0a8bc-152">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0a8bc-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a8bc-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a8bc-153">Minimum supported server</span></span><br/> | <span data-ttu-id="0a8bc-154">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a8bc-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a8bc-155">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0a8bc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a8bc-156">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="0a8bc-156">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0a8bc-157">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0a8bc-157">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="0a8bc-158">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0a8bc-158">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





