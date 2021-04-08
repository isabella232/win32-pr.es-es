---
title: S (API de UPnP)
description: Contiene términos relacionados con UPnP que comienzan por la letra S.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 94be0f7f-8263-40ad-9d48-35540eaa3a3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9386d7946c51bc02e78aa96c36063d22d75d61d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078718"
---
# <a name="s-upnp-apis"></a><span data-ttu-id="fb5a2-103">S (API de UPnP)</span><span class="sxs-lookup"><span data-stu-id="fb5a2-103">S (UPnP APIs)</span></span>

<span data-ttu-id="fb5a2-104">Contiene términos relacionados con UPnP que comienzan por la letra S.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-104">Contains UPnP-related terms that begin with the letter S.</span></span>

<span data-ttu-id="fb5a2-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) o [p](p-gly.md) Q [R](r-gly.md) s T [U](u-gly.md) V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="fb5a2-105">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](h-gly.md) I J K L M [N](n-gly.md) O [P](p-gly.md) Q [R](r-gly.md) S T [U](u-gly.md) V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="fb5a2-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**servicio**</span><span class="sxs-lookup"><span data-stu-id="fb5a2-106"><span id="upnp.s_1_gly"></span><span id="UPNP.S_1_GLY"></span>**service**</span></span>
</dt> <dd>

<span data-ttu-id="fb5a2-107">Un servicio es una unidad funcional lógica.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-107">A service is a logical functional unit.</span></span> <span data-ttu-id="fb5a2-108">Los servicios exponen acciones y modelan algunos o todos los Estados de un dispositivo físico mediante variables de estado.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-108">Services expose actions and model some or all of the states of a physical device using state variables.</span></span>

</dd> <dt>

<span data-ttu-id="fb5a2-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**Descripción del servicio**</span><span class="sxs-lookup"><span data-stu-id="fb5a2-109"><span id="upnp.s_2_gly"></span><span id="UPNP.S_2_GLY"></span>**service description**</span></span>
</dt> <dd>

<span data-ttu-id="fb5a2-110">Una descripción del servicio es una lista de las acciones que proporciona un servicio y las variables de estado asociadas a las acciones.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-110">A service description is a list of the actions a service provides, and the state variables associated with the actions.</span></span>

</dd> <dt>

<span data-ttu-id="fb5a2-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**objeto de servicio**</span><span class="sxs-lookup"><span data-stu-id="fb5a2-111"><span id="upnp.s_3_gly"></span><span id="UPNP.S_3_GLY"></span>**service object**</span></span>
</dt> <dd>

<span data-ttu-id="fb5a2-112">Un objeto de servicio es la representación de la API de punto de control de un servicio.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-112">A service object is the Control Point API representation of a service.</span></span> <span data-ttu-id="fb5a2-113">Un objeto de servicio implementa la interfaz [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) .</span><span class="sxs-lookup"><span data-stu-id="fb5a2-113">A service object implements the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) interface.</span></span>

</dd> <dt>

<span data-ttu-id="fb5a2-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**tipo de servicio**</span><span class="sxs-lookup"><span data-stu-id="fb5a2-114"><span id="upnp.s_4_gly"></span><span id="UPNP.S_4_GLY"></span>**service type**</span></span>
</dt> <dd>

<span data-ttu-id="fb5a2-115">Un tipo de servicio es un URN que identifica un servicio.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-115">A service type is a URN that identifies a service.</span></span> <span data-ttu-id="fb5a2-116">Hay una relación uno a uno entre una plantilla de servicio UPnP y un tipo de servicio.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-116">There is a one-to-one relationship between a UPnP service template and a service type.</span></span> <span data-ttu-id="fb5a2-117">Los comités de trabajo del Foro de UPnP definen varios tipos de servicio estándar.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-117">Several standard service types are defined by the UPnP Forum working committees.</span></span> <span data-ttu-id="fb5a2-118">Los tipos de servicio tienen el formato urn: schemas-UPnP-org: Service: serviceType: version.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-118">The service types are in the form urn:schemas-upnp-org:service:serviceType:version.</span></span> <span data-ttu-id="fb5a2-119">Por ejemplo, un tipo de servicio de analizador podría ser urn: schemas-UPnP-org: Service: Scanner: 1.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-119">For example, a scanner service type could be urn:schemas-upnp-org:service:scanner:1.</span></span>

<span data-ttu-id="fb5a2-120">Los proveedores UPnP pueden especificar servicios adicionales.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-120">UPnP vendors may specify additional services.</span></span> <span data-ttu-id="fb5a2-121">Estos servicios se indican mediante urn: Domain-Name: Service: serviceType: version, donde Domain-Name es un nombre de dominio registrado en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-121">Such services are denoted by urn:domain-name:service:serviceType:version where domain-name is a domain name that is registered to the vendor.</span></span>

</dd> <dt>

<span data-ttu-id="fb5a2-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**variable de estado**</span><span class="sxs-lookup"><span data-stu-id="fb5a2-122"><span id="upnp.s_5_gly"></span><span id="UPNP.S_5_GLY"></span>**state variable**</span></span>
</dt> <dd>

<span data-ttu-id="fb5a2-123">Una variable de estado es un fragmento de datos que describe parte del estado de un servicio.</span><span class="sxs-lookup"><span data-stu-id="fb5a2-123">A state variable is a piece of data that describes some part of a service's state.</span></span>

</dd> </dl>

 

 




