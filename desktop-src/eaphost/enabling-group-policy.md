---
title: Habilitar directiva de grupo
description: Obtenga información acerca de cómo configurar el suplicante habilitando la Directiva de grupo. Vea Consideraciones para suplicantes y ver recursos adicionales disponibles.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421432"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="d1214-104">Habilitar directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d1214-104">Enabling Group Policy</span></span>

<span data-ttu-id="d1214-105">En este tema se explica cómo configurar el suplicante habilitando la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="d1214-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="d1214-106">Los suplicantes de EAPHost pueden participar en la Directiva de grupo para permitir que un administrador de red configure de forma centralizada sus equipos de red.</span><span class="sxs-lookup"><span data-stu-id="d1214-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="d1214-107">El método y el mecanismo precisos que elige el solicitante para participar en la Directiva de grupo es el solicitante.</span><span class="sxs-lookup"><span data-stu-id="d1214-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="d1214-108">Entre los ejemplos de mecanismos para la participación de directivas de grupo se incluyen extensiones de cliente/servidor, plantilla administrativa, etc.</span><span class="sxs-lookup"><span data-stu-id="d1214-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="d1214-109">Consideraciones al habilitar directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="d1214-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="d1214-110">Estas son las consideraciones para los suplicantes con respecto a la Directiva de grupo y EAP.</span><span class="sxs-lookup"><span data-stu-id="d1214-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="d1214-111">La configuración de EAP siempre se debe almacenar como XML siempre que sea posible y no en formato binario.</span><span class="sxs-lookup"><span data-stu-id="d1214-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="d1214-112">La Directiva de grupo se puede aplicar a cualquier equipo del dominio, y no se garantiza que los datos de usuario y la configuración del método EAP sean portátiles entre las arquitecturas de procesador de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d1214-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="d1214-113">XML resuelve los problemas de los límites de la arquitectura del procesador, ya que el suplicante convierte localmente el XML independiente de la arquitectura del procesador en la representación binaria de la configuración en el momento de la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d1214-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="d1214-114">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="d1214-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="d1214-115">Preguntas frecuentes generales</span><span class="sxs-lookup"><span data-stu-id="d1214-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="d1214-116">[Preguntas más frecuentes sobre el método EAP](eap-method-frequently-asked-questions.md).</span><span class="sxs-lookup"><span data-stu-id="d1214-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="d1214-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="d1214-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="d1214-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="d1214-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="d1214-119">Si se usa una extensión de servidor de directiva de grupo, la extensión llamará a [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) normalmente para determinar los métodos disponibles y para generar la configuración de EAP adecuada para esa Directiva.</span><span class="sxs-lookup"><span data-stu-id="d1214-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="d1214-120">A continuación, la Directiva se envía a los clientes de red adecuados donde se aplica la Directiva.</span><span class="sxs-lookup"><span data-stu-id="d1214-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1214-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1214-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1214-122">Configuración de la interfaz de usuario del método EAP</span><span class="sxs-lookup"><span data-stu-id="d1214-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="d1214-123">Implementación de la compatibilidad de In-Band NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="d1214-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="d1214-124">Implementación de la compatibilidad de NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="d1214-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d1214-125">Transferencia de datos entre el suplicante y los métodos EAP</span><span class="sxs-lookup"><span data-stu-id="d1214-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d1214-126">Suplicantes de EAPHost</span><span class="sxs-lookup"><span data-stu-id="d1214-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




