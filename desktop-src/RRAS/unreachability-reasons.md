---
title: Razones de inasequibilidad
description: En la tabla siguiente se muestran los valores constantes que indican por qué no se puede tener acceso a una interfaz.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078102"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="44965-103">Razones de inasequibilidad</span><span class="sxs-lookup"><span data-stu-id="44965-103">Unreachability Reasons</span></span>

<span data-ttu-id="44965-104">En la tabla siguiente se muestran los valores constantes que indican por qué no se puede tener acceso a una interfaz.</span><span class="sxs-lookup"><span data-stu-id="44965-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="44965-105">Value</span><span class="sxs-lookup"><span data-stu-id="44965-105">Value</span></span>                                       | <span data-ttu-id="44965-106">Significado</span><span class="sxs-lookup"><span data-stu-id="44965-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44965-107">Administrador de la interfaz de MPR \_ \_ \_ deshabilitado</span><span class="sxs-lookup"><span data-stu-id="44965-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="44965-108">El administrador ha deshabilitado la interfaz.</span><span class="sxs-lookup"><span data-stu-id="44965-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="44965-109">error de conexión de la interfaz de MPR \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="44965-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="44965-110">Error en el intento de conexión anterior.</span><span class="sxs-lookup"><span data-stu-id="44965-110">The previous connection attempt failed.</span></span> <span data-ttu-id="44965-111">Busque el miembro **dwLastError** para el código de error.</span><span class="sxs-lookup"><span data-stu-id="44965-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="44965-112">\_restricción de \_ horas de \_ inactividad \_ de la interfaz de MPR</span><span class="sxs-lookup"><span data-stu-id="44965-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="44965-113">No se permite el acceso telefónico en el momento actual.</span><span class="sxs-lookup"><span data-stu-id="44965-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="44965-114">\_interfaz \_ de MPR \_ sin \_ recursos</span><span class="sxs-lookup"><span data-stu-id="44965-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="44965-115">No hay puertos o dispositivos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="44965-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="44965-116">servicio de interfaz de MPR en \_ \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="44965-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="44965-117">El servicio está en pausa.</span><span class="sxs-lookup"><span data-stu-id="44965-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="44965-118">interfaz de MPR \_ \_ sin \_ detección de medios \_</span><span class="sxs-lookup"><span data-stu-id="44965-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="44965-119">El cable de red está desconectado de la tarjeta de red.</span><span class="sxs-lookup"><span data-stu-id="44965-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="44965-120">interfaz de MPR \_ \_ sin \_ dispositivo</span><span class="sxs-lookup"><span data-stu-id="44965-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="44965-121">La tarjeta de red se ha quitado de la máquina.</span><span class="sxs-lookup"><span data-stu-id="44965-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="44965-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="44965-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44965-123">**MPR ( \_ interfaz) \_ 0**</span><span class="sxs-lookup"><span data-stu-id="44965-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="44965-124">**Interfaz de MPR \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="44965-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="44965-125">**MIB \_ IFROW**</span><span class="sxs-lookup"><span data-stu-id="44965-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="44965-126">**MIB \_ IFSTATUS**</span><span class="sxs-lookup"><span data-stu-id="44965-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 