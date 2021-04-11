---
description: Define los elementos de configuración de 802.1 X.
ms.assetid: 4755356e-cb4b-4eed-a494-ca0d17f5184f
title: Esquema OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9df45ed7981c055e955afe72333a42db99ddb21a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276704"
---
# <a name="onex-schema"></a><span data-ttu-id="e408a-103">Esquema OneX</span><span class="sxs-lookup"><span data-stu-id="e408a-103">OneX Schema</span></span>

<span data-ttu-id="e408a-104">El esquema OneX define los elementos de configuración de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e408a-104">The OneX Schema defines 802.1X configuration elements.</span></span> <span data-ttu-id="e408a-105">Todos los elementos de esquema OneX se aplican tanto a los perfiles con cable como a los inalámbricos.</span><span class="sxs-lookup"><span data-stu-id="e408a-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="e408a-106">Para obtener una lista de los elementos definidos, consulte [elementos de esquema Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="e408a-106">For a list of defined elements, see [OneX Schema Elements](onexschema-elements.md).</span></span>

<span data-ttu-id="e408a-107">El elemento raíz de un perfil de 802.1 X es el elemento [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e408a-107">The root element of an 802.1X profile is the [**OneX**](onexschema-onex-element.md) element.</span></span> <span data-ttu-id="e408a-108">Cada perfil tendrá exactamente un elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="e408a-108">Each profile will have exactly one root element.</span></span> <span data-ttu-id="e408a-109">El elemento **Onex** está en el `https://www.microsoft.com/networking/OneX/v1` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="e408a-109">The **OneX** element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="e408a-110">Para ver los perfiles de ejemplo para redes inalámbricas que incluyen elementos de configuración de 802.1 X, consulte los siguientes ejemplos de perfil:</span><span class="sxs-lookup"><span data-stu-id="e408a-110">To view sample profiles for wireless networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="e408a-111">Ejemplo de Perfil de bootstrap</span><span class="sxs-lookup"><span data-stu-id="e408a-111">Bootstrap Profile Sample</span></span>](bootstrap-profile-sample.md)
-   [<span data-ttu-id="e408a-112">Ejemplo de Perfil de FIPS</span><span class="sxs-lookup"><span data-stu-id="e408a-112">FIPS Profile Sample</span></span>](fips-profile-sample.md)
-   [<span data-ttu-id="e408a-113">Ejemplo de Perfil de un solo Sign-On</span><span class="sxs-lookup"><span data-stu-id="e408a-113">Single Sign-On Profile Sample</span></span>](single-sign-on-profile-sample.md)
-   [<span data-ttu-id="e408a-114">Ejemplo de Perfil de WPA-Enterprise con PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="e408a-114">WPA-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="e408a-115">Ejemplo de Perfil de WPA-Enterprise con TLS</span><span class="sxs-lookup"><span data-stu-id="e408a-115">WPA-Enterprise with TLS Profile Sample</span></span>](wpa-enterprise-with-tls-profile-sample.md)
-   [<span data-ttu-id="e408a-116">Ejemplo de perfil WPA2-Enterprise con PEAP-MSCHAPv2</span><span class="sxs-lookup"><span data-stu-id="e408a-116">WPA2-Enterprise with PEAP-MSCHAPv2 Profile Sample</span></span>](wpa2-enterprise-with-peap-mschapv2-profile-sample.md)
-   [<span data-ttu-id="e408a-117">Ejemplo de perfil WPA2-Enterprise con TLS</span><span class="sxs-lookup"><span data-stu-id="e408a-117">WPA2-Enterprise with TLS Profile Sample</span></span>](wpa2-enterprise-with-tls-profile-sample.md)

<span data-ttu-id="e408a-118">Para ver los perfiles de ejemplo de redes cableadas que incluyen elementos de configuración de 802.1 X, consulte los siguientes ejemplos de perfil:</span><span class="sxs-lookup"><span data-stu-id="e408a-118">To view sample profiles for wired networks that include 802.1X configuration elements, see the following profile samples:</span></span>

-   [<span data-ttu-id="e408a-119">Ejemplo de Perfil de certificado de equipo</span><span class="sxs-lookup"><span data-stu-id="e408a-119">Machine Certificate Profile Sample</span></span>](machine-certificate-profile-sample.md)
-   [<span data-ttu-id="e408a-120">Ejemplo de perfil PEAP</span><span class="sxs-lookup"><span data-stu-id="e408a-120">PEAP Profile Sample</span></span>](peap-profile-sample.md)
-   [<span data-ttu-id="e408a-121">Perfil de ejemplo de certificado de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e408a-121">Smart Card Certificate Sample Profile</span></span>](smart-card-certificate-profile-sample.md)

 

 



