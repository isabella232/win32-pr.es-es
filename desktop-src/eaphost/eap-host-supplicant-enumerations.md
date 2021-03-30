---
title: Enumeraciones del suplicante de EAPHost
description: Obtenga información sobre las enumeraciones de la API suplicante de EAPHost, como EapHostPeerMethodResultReason y el estado de aislamiento \_ .
ms.assetid: ba4d5a7f-3a5d-4ca3-975e-1ffa182b9014
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e214682a9b94c98db5981a0df8c2b8619814f1e5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904815"
---
# <a name="eaphost-supplicant-enumerations"></a><span data-ttu-id="5634e-103">Enumeraciones del suplicante de EAPHost</span><span class="sxs-lookup"><span data-stu-id="5634e-103">EAPHost Supplicant Enumerations</span></span>

<span data-ttu-id="5634e-104">Las enumeraciones de la API suplicante de EAPHost son las siguientes.</span><span class="sxs-lookup"><span data-stu-id="5634e-104">The EAPHost Supplicant API enumerations are as follows.</span></span>



| <span data-ttu-id="5634e-105">Enumeración</span><span class="sxs-lookup"><span data-stu-id="5634e-105">Enumeration</span></span>                                                                  | <span data-ttu-id="5634e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5634e-106">Description</span></span>                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5634e-107">**tipo de datos de interfaz de \_ usuario interactiva de EAP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5634e-107">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)     | <span data-ttu-id="5634e-108">Especifica el conjunto de tipos de datos de contexto de la interfaz de usuario interactiva suministrados a ciertas llamadas API de suplicante.</span><span class="sxs-lookup"><span data-stu-id="5634e-108">Specifies the set of types of interactive user interface context data supplied to certain supplicant API calls.</span></span>    |
| [<span data-ttu-id="5634e-109">**\_tipo de \_ propiedad de método EAP \_**</span><span class="sxs-lookup"><span data-stu-id="5634e-109">**EAP\_METHOD\_PROPERTY\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_type)              | <span data-ttu-id="5634e-110">Windows 7 o posterior: especifica el tipo de propiedad de método.</span><span class="sxs-lookup"><span data-stu-id="5634e-110">Windows 7 or later: Specifies the method property type.</span></span>                                                            |
| [<span data-ttu-id="5634e-111">**\_tipo de \_ valor de propiedad de método EAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5634e-111">**EAP\_METHOD\_PROPERTY\_VALUE\_TYPE**</span></span>](/windows/desktop/api/EapTypes/ne-eaptypes-eap_method_property_value_type) | <span data-ttu-id="5634e-112">Windows 7 o posterior: especifica el tipo de datos de un valor de propiedad de método.</span><span class="sxs-lookup"><span data-stu-id="5634e-112">Windows 7 or later: Specifies the data type of a method property value.</span></span>                                            |
| [<span data-ttu-id="5634e-113">**\_Estado de autenticación de EAPHOST \_**</span><span class="sxs-lookup"><span data-stu-id="5634e-113">**EAPHOST\_AUTH\_STATUS**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-eaphost_auth_status)                         | <span data-ttu-id="5634e-114">Define el conjunto de posibles valores de estado de la sesión de autenticación EAP.</span><span class="sxs-lookup"><span data-stu-id="5634e-114">Defines the set of possible EAP authentication session status values.</span></span>                                              |
| [<span data-ttu-id="5634e-115">**EapHostPeerAuthParams**</span><span class="sxs-lookup"><span data-stu-id="5634e-115">**EapHostPeerAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)                       | <span data-ttu-id="5634e-116">Define el conjunto de posibles valores de parámetro de autenticación.</span><span class="sxs-lookup"><span data-stu-id="5634e-116">Defines the set of possible authentication parameter values.</span></span>                                                       |
| [<span data-ttu-id="5634e-117">**EapHostPeerMethodResultReason**</span><span class="sxs-lookup"><span data-stu-id="5634e-117">**EapHostPeerMethodResultReason**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeermethodresultreason)       | <span data-ttu-id="5634e-118">Define el conjunto de posibles razones que describen los resultados devueltos por un método EAP a un suplicante.</span><span class="sxs-lookup"><span data-stu-id="5634e-118">Defines the set of possible reasons that describe the results returned by an EAP method to a supplicant.</span></span>           |
| [<span data-ttu-id="5634e-119">**EapHostPeerResponseAction**</span><span class="sxs-lookup"><span data-stu-id="5634e-119">**EapHostPeerResponseAction**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction)               | <span data-ttu-id="5634e-120">Define el conjunto de acciones que un autenticador o método del mismo nivel de EAP puede indicar a un suplicante durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="5634e-120">Defines the set of actions an EAP authenticator or peer method can indicate to a supplicant during authentication.</span></span> |
| [<span data-ttu-id="5634e-121">**Estado de aislamiento \_**</span><span class="sxs-lookup"><span data-stu-id="5634e-121">**ISOLATION\_STATE**</span></span>](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state)                                  | <span data-ttu-id="5634e-122">Define el conjunto de posibles valores de estado de aislamiento de un equipo.</span><span class="sxs-lookup"><span data-stu-id="5634e-122">Defines the set of possible isolation status values of a machine.</span></span>                                                  |



 

 

 




