---
title: Referencia de API de EAPHost
description: Obtenga información sobre las API de EAPHost y sus componentes. Consulte la información de referencia de varios temas de la API, como el esquema XML de EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421396"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="dac7d-104">Referencia de API de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-104">EAPHost API Reference</span></span>

<span data-ttu-id="dac7d-105">Las API de EAPHost están divididas en tres componentes: las API de suplicante, a las que se puede llamar directamente desde una aplicación habilitada para EAP; las API del método EAP del mismo nivel, que administran solicitudes de suplicante para un tipo de autenticación EAP específico y generan elementos interactivos en el cliente. y las API del autenticador de EAP, que realizan la autenticación del lado servidor de un suplicante.</span><span class="sxs-lookup"><span data-stu-id="dac7d-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="dac7d-106">Los dos últimos componentes de la API: el método EAP del mismo nivel y las API del método de autenticador EAP: requieren una implementación personalizada y compatible en los archivos DLL que los exponen al servicio EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="dac7d-107">No se pueden llamar directamente desde el código de la aplicación; en su lugar, lo llaman EAPHost (en el lado cliente para los métodos EAP peer y en el lado servidor para los métodos de autenticación EAP) si la implementación coincide con las firmas de API especificadas en la documentación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="dac7d-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="dac7d-108">La información específica de la implementación de la API se proporciona en cada página de referencia de funciones.</span><span class="sxs-lookup"><span data-stu-id="dac7d-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="dac7d-109">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="dac7d-110">Tema</span><span class="sxs-lookup"><span data-stu-id="dac7d-110">Topic</span></span>                                                      | <span data-ttu-id="dac7d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac7d-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="dac7d-112">Configuración del registro de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="dac7d-113">Describe las claves del registro utilizadas por EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="dac7d-114">Esquema XML de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="dac7d-115">Tema</span><span class="sxs-lookup"><span data-stu-id="dac7d-115">Topic</span></span>                                            | <span data-ttu-id="dac7d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac7d-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dac7d-117">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="dac7d-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="dac7d-118">Describe el esquema de EAPHost y el esquema heredado para crear el XML de configuración y el XML de credenciales.</span><span class="sxs-lookup"><span data-stu-id="dac7d-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="dac7d-119">Referencia común de API de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="dac7d-120">Tema</span><span class="sxs-lookup"><span data-stu-id="dac7d-120">Topic</span></span>                                                                   | <span data-ttu-id="dac7d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac7d-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="dac7d-122">Enumeraciones comunes de la API de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="dac7d-123">Enumera las constantes comunes a todas las API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="dac7d-124">Estructuras comunes de API de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="dac7d-125">Enumera las estructuras comunes a todas las API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="dac7d-126">Constantes de API de EAPHost comunes</span><span class="sxs-lookup"><span data-stu-id="dac7d-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="dac7d-127">Enumera las constantes comunes a todas las API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="dac7d-128">Referencia de API de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-128">EAPHost API Reference</span></span>



| <span data-ttu-id="dac7d-129">Tema</span><span class="sxs-lookup"><span data-stu-id="dac7d-129">Topic</span></span>                                                                       | <span data-ttu-id="dac7d-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="dac7d-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dac7d-131">Referencia de API suplicante de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="dac7d-132">Describe los elementos de API disponibles para habilitar las llamadas de suplicante a EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="dac7d-133">Referencia de API de método del mismo nivel de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="dac7d-134">Describe los elementos de la API que se deben implementar para crear un archivo DLL de método EAP del mismo nivel que un cliente EAPHost puede cargar y llamar.</span><span class="sxs-lookup"><span data-stu-id="dac7d-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="dac7d-135">API del método de autenticador de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="dac7d-136">Describe los elementos de la API que se deben implementar para crear un archivo DLL de método de autenticación de EAP que se pueda cargar y llamar mediante un servidor EAPHost.</span><span class="sxs-lookup"><span data-stu-id="dac7d-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dac7d-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dac7d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac7d-138">Acerca de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="dac7d-139">Uso de EAPHost</span><span class="sxs-lookup"><span data-stu-id="dac7d-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




