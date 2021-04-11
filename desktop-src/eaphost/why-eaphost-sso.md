---
title: Información general sobre el escenario EAPHost de SSO
description: Contiene dos escenarios que muestran las ventajas de un suplicante habilitado para el inicio de sesión único (SSO).
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104149015"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="87f7f-103">Información general sobre el escenario EAPHost de SSO</span><span class="sxs-lookup"><span data-stu-id="87f7f-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="87f7f-104">El siguiente tema contiene dos escenarios que muestran las ventajas de un suplicante habilitado para el inicio de sesión único (SSO).</span><span class="sxs-lookup"><span data-stu-id="87f7f-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="87f7f-105">Acerca de los escenarios</span><span class="sxs-lookup"><span data-stu-id="87f7f-105">About the Scenarios</span></span>

<span data-ttu-id="87f7f-106">SSO proporciona funcionalidad para conservar la información adicional de credenciales de usuario que tradicionalmente se almacena en el BLOB de usuario de EAP.</span><span class="sxs-lookup"><span data-stu-id="87f7f-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="87f7f-107">A diferencia de otros procesos de credenciales, los suplicantes habilitados para SSO pueden resolver situaciones de inicio de sesión como itinerancia de AP y cambio de contraseña sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="87f7f-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="87f7f-108">Comportamiento de almacenamiento en caché de PIN EAP-TLS</span><span class="sxs-lookup"><span data-stu-id="87f7f-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="87f7f-109">Un suplicante puede intentar la autenticación de red mediante un método EAP basado en tarjeta inteligente, como la seguridad de la capa de transporte del Protocolo de autenticación extensible (EAP-TLS).</span><span class="sxs-lookup"><span data-stu-id="87f7f-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="87f7f-110">En este escenario y otros similares, el solicitante obtiene el PIN de la tarjeta inteligente del usuario y recupera un certificado de usuario para la autenticación de red seguido de una llamada a WinLogin en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="87f7f-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="87f7f-111">Después de la autenticación correcta, el solicitante almacena en caché el BLOB del usuario y no almacena la información del PIN del usuario.</span><span class="sxs-lookup"><span data-stu-id="87f7f-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="87f7f-112">Cuando el usuario se desplaza a una nueva sesión de ubicación, se debe reanudar y volver a realizar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="87f7f-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="87f7f-113">Dado que el certificado no se puede almacenar previamente, se producirá un error en la autenticación del usuario y el solicitante vaciará el BLOB del usuario.</span><span class="sxs-lookup"><span data-stu-id="87f7f-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="87f7f-114">En este momento, se necesita el PIN de usuario para recuperar el certificado de usuario de la tarjeta inteligente para la autenticación de red.</span><span class="sxs-lookup"><span data-stu-id="87f7f-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="87f7f-115">Dado que SSO almacena en caché el PIN, el certificado se puede recuperar sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="87f7f-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="87f7f-116">Sin SSO, EAP-TLS tendría que volver a generar una interfaz de usuario de colección de PIN.</span><span class="sxs-lookup"><span data-stu-id="87f7f-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="87f7f-117">Para obtener un enfoque paso a paso, consulte [comportamiento del almacenamiento en caché del PIN EAP-TLS de SSO](sso-eap-tls-pin-caching-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="87f7f-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="87f7f-118">Comportamiento de cambio de contraseña de SSO</span><span class="sxs-lookup"><span data-stu-id="87f7f-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="87f7f-119">Un suplicante puede intentar la autenticación de red mediante un método EAP basado en contraseña, como el protocolo de autenticación por desafío mutuo de Microsoft versión 2,0 (MS-CHAPv2), configurado para usar las credenciales de WinLogin.</span><span class="sxs-lookup"><span data-stu-id="87f7f-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="87f7f-120">En este escenario, el solicitante recopila las credenciales de usuario una vez y las proporciona a EAPHost para la autenticación de red.</span><span class="sxs-lookup"><span data-stu-id="87f7f-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="87f7f-121">Después de la autenticación de red correcta, el suplicante usa el mismo conjunto de credenciales para WinLogin.</span><span class="sxs-lookup"><span data-stu-id="87f7f-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="87f7f-122">Sin embargo, si se cambiaron credenciales como la contraseña de usuario durante la autenticación de red sin un suplicante habilitado para SSO, la siguiente llamada a WinLogin producirá un error.</span><span class="sxs-lookup"><span data-stu-id="87f7f-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="87f7f-123">SSO conserva las nuevas credenciales y permite un WinLogin correcto sin la intervención del usuario adicional.</span><span class="sxs-lookup"><span data-stu-id="87f7f-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="87f7f-124">Para obtener un enfoque paso a paso, consulte [comportamiento del cambio de contraseña de SSO](sso-password-change-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="87f7f-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87f7f-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="87f7f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87f7f-126">SSO y PLAP</span><span class="sxs-lookup"><span data-stu-id="87f7f-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




