---
title: Estructuras de método del mismo nivel de EAPHost
description: Obtenga información sobre las estructuras de API de método del mismo nivel de EAPHost, como EapCertificateCredential y EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dab0d2bcd5bf1a6dc48ab01fa12c24785cd92a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695760"
---
# <a name="eaphost-peer-method-structures"></a><span data-ttu-id="d935c-103">Estructuras de método del mismo nivel de EAPHost</span><span class="sxs-lookup"><span data-stu-id="d935c-103">EAPHost Peer Method Structures</span></span>

<span data-ttu-id="d935c-104">Las estructuras de API del método del mismo nivel de EAPHost son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="d935c-104">The EAPHost Peer Method API structures are as follows.</span></span>



| <span data-ttu-id="d935c-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="d935c-105">Structure</span></span>                                                              | <span data-ttu-id="d935c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d935c-106">Description</span></span>                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d935c-107">**EapCertificateCredential**</span><span class="sxs-lookup"><span data-stu-id="d935c-107">**EapCertificateCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | <span data-ttu-id="d935c-108">Contiene información sobre el certificado que el método EAP utiliza para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d935c-108">Contains information about the certificate that the EAP method uses for authentication.</span></span>                                                                                                            |
| [<span data-ttu-id="d935c-109">**EapCredential**</span><span class="sxs-lookup"><span data-stu-id="d935c-109">**EapCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | <span data-ttu-id="d935c-110">Contiene información sobre el tipo de credenciales y las credenciales adecuadas.</span><span class="sxs-lookup"><span data-stu-id="d935c-110">Contains information about the credentials type and the appropriate credentials.</span></span> <span data-ttu-id="d935c-111">Esto se pasa como una entrada a la API de [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) .</span><span class="sxs-lookup"><span data-stu-id="d935c-111">This is passed as an input to the [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) API.</span></span> |
| [<span data-ttu-id="d935c-112">**\_ \_ rutinas de método EAP del mismo nivel \_**</span><span class="sxs-lookup"><span data-stu-id="d935c-112">**EAP\_PEER\_METHOD\_ROUTINES**</span></span>](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | <span data-ttu-id="d935c-113">Contiene un conjunto de punteros de función a las API de método del mismo nivel de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d935c-113">Contains a set of function pointers to the EAPHost Peer Method APIs.</span></span>                                                                                                                               |
| [<span data-ttu-id="d935c-114">**EapPeerMethodOutput**</span><span class="sxs-lookup"><span data-stu-id="d935c-114">**EapPeerMethodOutput**</span></span>](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | <span data-ttu-id="d935c-115">Contiene la información de la acción devuelta por un método EAP del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="d935c-115">Contains the action information returned by an EAP peer method.</span></span>                                                                                                                                    |
| [<span data-ttu-id="d935c-116">**EapPeerMethodResult**</span><span class="sxs-lookup"><span data-stu-id="d935c-116">**EapPeerMethodResult**</span></span>](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | <span data-ttu-id="d935c-117">Contiene los datos de resultado generados por un método EAP durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d935c-117">Contains result data generated by an EAP method during authentication.</span></span>                                                                                                                             |
| [<span data-ttu-id="d935c-118">**EapSimCredential**</span><span class="sxs-lookup"><span data-stu-id="d935c-118">**EapSimCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | <span data-ttu-id="d935c-119">Contiene información sobre la tarjeta SIM utilizada por el método EAP para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="d935c-119">Contains information about the SIM that is used by the EAP method for authentication.</span></span>                                                                                                              |
| [<span data-ttu-id="d935c-120">**EapUsernamePasswordCredential**</span><span class="sxs-lookup"><span data-stu-id="d935c-120">**EapUsernamePasswordCredential**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | <span data-ttu-id="d935c-121">Contiene el nombre de usuario y la contraseña que usa el método EAP para autenticar al usuario.</span><span class="sxs-lookup"><span data-stu-id="d935c-121">Contains the username and password that is used by the EAP method for authenticating the user.</span></span>                                                                                                     |



 

 

 




