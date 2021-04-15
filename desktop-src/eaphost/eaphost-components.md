---
title: Componentes de EAPHost
description: Obtenga información sobre los tres componentes de la autenticación de EAPHost. Ver recursos adicionales disponibles para usar la autenticación de EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488294"
---
# <a name="components-of-eaphost"></a><span data-ttu-id="8b789-104">Componentes de EAPHost</span><span class="sxs-lookup"><span data-stu-id="8b789-104">Components of EAPHost</span></span>

<span data-ttu-id="8b789-105">En este tema se describen los tres componentes de la autenticación de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b789-105">This topic describes the three components of EAPHost authentication.</span></span>

## <a name="eaphost-components"></a><span data-ttu-id="8b789-106">Componentes de EAPHost</span><span class="sxs-lookup"><span data-stu-id="8b789-106">EAPHost Components</span></span>

<span data-ttu-id="8b789-107">La autenticación de EAPHost tiene los tres componentes siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b789-107">EAPHost authentication has the following three components.</span></span>

-   <span data-ttu-id="8b789-108">El suplicante, que realiza las solicitudes de autenticación.</span><span class="sxs-lookup"><span data-stu-id="8b789-108">The supplicant, which makes the authentication requests.</span></span>
-   <span data-ttu-id="8b789-109">Los métodos EAP del mismo nivel (o cliente), que implementan los métodos EAP específicos y administran la sesión de autenticación en el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="8b789-109">The peer (or client) EAP methods, which implement the specific EAP methods and manage the authentication session on the client side.</span></span>
-   <span data-ttu-id="8b789-110">Los métodos EAP de autenticador (o servidor), que implementan el lado servidor del protocolo EAP.</span><span class="sxs-lookup"><span data-stu-id="8b789-110">The authenticator (or server) EAP methods, which implement the server side of the EAP protocol.</span></span>

<span data-ttu-id="8b789-111">Las API de suplicante se llaman directamente desde una aplicación que desea autenticarse a través de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b789-111">The supplicant APIs are called directly from an application that wants to authenticate via EAPHost.</span></span> <span data-ttu-id="8b789-112">Sin embargo, las API del método del mismo nivel y del autenticador son prototipos de función que se deben implementar para un tipo de método de autenticación EAP específico, como la versión 2,0 del Protocolo de autenticación por desafío mutuo de Microsoft (MS-CHAPv2).</span><span class="sxs-lookup"><span data-stu-id="8b789-112">The peer method and authenticator method APIs, however, are function prototypes that must be implemented for a specific EAP authentication method type - such as the Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2).</span></span>

<span data-ttu-id="8b789-113">Si va a crear una aplicación que usará EAPHost para la autenticación, consulte la referencia de la [API de suplicante de EAPHost](eap-host-supplicant-api-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8b789-113">If you are authoring an application that will use EAPHost for authentication, please refer to the [EAPHost Supplicant API Reference](eap-host-supplicant-api-reference.md).</span></span>

<span data-ttu-id="8b789-114">Si va a crear un nuevo método de autenticación EAP para que lo administre EAPHost, consulte la [referencia de API de método del mismo nivel de EAPHost](eap-host-peer-method-api-reference.md) y las API del método de [autenticador de EAPHost](eaphost-authenticator-method-apis.md).</span><span class="sxs-lookup"><span data-stu-id="8b789-114">If you are authoring a new EAP authentication method to be managed by EAPHost, please refer to the [EAPHost Peer Method API Reference](eap-host-peer-method-api-reference.md) and the [EAPHost Authenticator Method APIs](eaphost-authenticator-method-apis.md).</span></span> <span data-ttu-id="8b789-115">Tenga en cuenta que creará implementaciones de estas API expuestas en un nuevo archivo DLL que EAPHost carga, en lugar de llamarlas directamente.</span><span class="sxs-lookup"><span data-stu-id="8b789-115">Note that you will be creating implementations of these APIs exposed in a new DLL that EAPHost loads, rather than calling them directly.</span></span>

 

 




