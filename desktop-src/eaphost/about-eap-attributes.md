---
title: Atributos EAP
description: Es una \_ estructura de atributo EAP que contiene un tipo predeterminado de datos relacionados con una sesión de autenticación.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105714503"
---
# <a name="eap-attributes"></a><span data-ttu-id="d6740-103">Atributos EAP</span><span class="sxs-lookup"><span data-stu-id="d6740-103">EAP Attributes</span></span>

<span data-ttu-id="d6740-104">Un atributo EAP es una estructura de [**\_ atributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) que contiene un tipo predeterminado de datos relacionados con una sesión de autenticación.</span><span class="sxs-lookup"><span data-stu-id="d6740-104">An EAP attribute is an [**EAP\_ATTRIBUTE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) structure that contains a predetermined type of data relating to an authentication session.</span></span> <span data-ttu-id="d6740-105">Los atributos se utilizan para comunicar información entre los métodos y suplicantes EAP o entre los métodos EAP y los autenticadores.</span><span class="sxs-lookup"><span data-stu-id="d6740-105">Attributes are used to communicate information between EAP methods and supplicants or between EAP methods and authenticators.</span></span> <span data-ttu-id="d6740-106">Las implementaciones del mismo nivel y autenticador de un método EAP pueden intercambiar estos atributos a través de una red.</span><span class="sxs-lookup"><span data-stu-id="d6740-106">Peer and authenticator implementations of an EAP method may exchange these attributes over a network.</span></span>

<span data-ttu-id="d6740-107">En el tema [**\_ \_ tipo de atributo EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)se muestra una lista completa de los tipos de atributos admitidos.</span><span class="sxs-lookup"><span data-stu-id="d6740-107">A complete list of supported attribute types appears in the topic [**EAP\_ATTRIBUTE\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).</span></span>

## <a name="attributes-consumed-by-supplicants"></a><span data-ttu-id="d6740-108">Atributos utilizados por suplicantes</span><span class="sxs-lookup"><span data-stu-id="d6740-108">Attributes Consumed by Supplicants</span></span>

<span data-ttu-id="d6740-109">Los suplicantes de 802.1 X consumen los siguientes tipos de atributos.</span><span class="sxs-lookup"><span data-stu-id="d6740-109">The following attribute types are consumed by 802.1X supplicants.</span></span>

-   <span data-ttu-id="d6740-110">**eatVendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="d6740-110">**eatVendorSpecific**</span></span>

<span data-ttu-id="d6740-111">Los suplicantes de cliente PPP consumen los siguientes tipos de atributos.</span><span class="sxs-lookup"><span data-stu-id="d6740-111">The following attribute types are consumed by PPP client supplicants.</span></span>

-   <span data-ttu-id="d6740-112">**eatMinimum**</span><span class="sxs-lookup"><span data-stu-id="d6740-112">**eatMinimum**</span></span>
-   <span data-ttu-id="d6740-113">**eatEAPTLV**</span><span class="sxs-lookup"><span data-stu-id="d6740-113">**eatEAPTLV**</span></span>

<span data-ttu-id="d6740-114">Los suplicantes del servidor PPP consumen los siguientes tipos de atributos.</span><span class="sxs-lookup"><span data-stu-id="d6740-114">The following attribute types are consumed by PPP server supplicants.</span></span>

-   <span data-ttu-id="d6740-115">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="d6740-115">**eatUserName**</span></span>
-   <span data-ttu-id="d6740-116">**eatReplyMessage**</span><span class="sxs-lookup"><span data-stu-id="d6740-116">**eatReplyMessage**</span></span>
-   <span data-ttu-id="d6740-117">**eatState**</span><span class="sxs-lookup"><span data-stu-id="d6740-117">**eatState**</span></span>
-   <span data-ttu-id="d6740-118">**eatSessionTimeout**</span><span class="sxs-lookup"><span data-stu-id="d6740-118">**eatSessionTimeout**</span></span>
-   <span data-ttu-id="d6740-119">**eatEAPMessage**</span><span class="sxs-lookup"><span data-stu-id="d6740-119">**eatEAPMessage**</span></span>

## <a name="attributes-exported-by-methods"></a><span data-ttu-id="d6740-120">Atributos exportados por métodos</span><span class="sxs-lookup"><span data-stu-id="d6740-120">Attributes Exported by Methods</span></span>

<span data-ttu-id="d6740-121">Los métodos EAP pueden exportar los siguientes tipos de atributos.</span><span class="sxs-lookup"><span data-stu-id="d6740-121">The following attribute types could be exported by EAP methods.</span></span>

-   <span data-ttu-id="d6740-122">**eatClearTextPassword**</span><span class="sxs-lookup"><span data-stu-id="d6740-122">**eatClearTextPassword**</span></span>
-   <span data-ttu-id="d6740-123">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="d6740-123">**eatQuarantineSoH**</span></span>
-   <span data-ttu-id="d6740-124">**eatMethodId**</span><span class="sxs-lookup"><span data-stu-id="d6740-124">**eatMethodId**</span></span>

<span data-ttu-id="d6740-125">Los métodos de [seguridad de nivel de transporte (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) de EAP exportan el siguiente tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="d6740-125">The following attribute type is exported by EAP [Transport Level Security (TLS)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS) methods.</span></span>

-   <span data-ttu-id="d6740-126">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="d6740-126">**eatCertificateOID**</span></span>

<span data-ttu-id="d6740-127">Los siguientes tipos de atributo se exportan mediante los métodos de la versión 2,0 (MS-CHAPv2) del [Protocolo de autenticación por desafío mutuo de Microsoft](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d6740-127">The following attribute types are exported by [Microsoft Challenge Handshake Authentication Protocol version 2.0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2) methods.</span></span>

-   <span data-ttu-id="d6740-128">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="d6740-128">**eatUserName**</span></span>
-   <span data-ttu-id="d6740-129">**eatCredentialsChanged**</span><span class="sxs-lookup"><span data-stu-id="d6740-129">**eatCredentialsChanged**</span></span>

<span data-ttu-id="d6740-130">El tipo de atributo siguiente lo consume el servidor de directivas de redes (NPS).</span><span class="sxs-lookup"><span data-stu-id="d6740-130">The following attribute type is consumed by Network Policy Server (NPS).</span></span>

-   <span data-ttu-id="d6740-131">**eatCertificateOID**</span><span class="sxs-lookup"><span data-stu-id="d6740-131">**eatCertificateOID**</span></span>

<span data-ttu-id="d6740-132">Los métodos del [Protocolo de autenticación extensible protegido (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) exportan los siguientes tipos de atributos.</span><span class="sxs-lookup"><span data-stu-id="d6740-132">The following attribute types are exported by [Protected Extensible Authentication Protocol (PEAP)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) methods.</span></span>

-   <span data-ttu-id="d6740-133">**eatUserName**</span><span class="sxs-lookup"><span data-stu-id="d6740-133">**eatUserName**</span></span>
-   <span data-ttu-id="d6740-134">**eatPEAPEmbeddedEAPTypeId**</span><span class="sxs-lookup"><span data-stu-id="d6740-134">**eatPEAPEmbeddedEAPTypeId**</span></span>
-   <span data-ttu-id="d6740-135">**eatPEAPFastRoamedSession**</span><span class="sxs-lookup"><span data-stu-id="d6740-135">**eatPEAPFastRoamedSession**</span></span>
-   <span data-ttu-id="d6740-136">**eatQuarantineSoH**</span><span class="sxs-lookup"><span data-stu-id="d6740-136">**eatQuarantineSoH**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6740-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6740-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6740-138">**\_atributo EAP**</span><span class="sxs-lookup"><span data-stu-id="d6740-138">**EAP\_ATTRIBUTE**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[<span data-ttu-id="d6740-139">**\_tipo de atributo EAP \_**</span><span class="sxs-lookup"><span data-stu-id="d6740-139">**EAP\_ATTRIBUTE\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 