---
description: El objeto Phone es la entidad que representa el dispositivo de teléfono real y todos sus controles.
ms.assetid: 5bc2f595-8e2b-4938-b813-1574a9390084
title: Interfaces de objetos de teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f39b163e895a512e7adc7be5c2fb848c5849361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688003"
---
# <a name="phone-object-interfaces"></a><span data-ttu-id="b8479-103">Interfaces de objetos de teléfono</span><span class="sxs-lookup"><span data-stu-id="b8479-103">Phone Object Interfaces</span></span>

<span data-ttu-id="b8479-104">El objeto Phone es la entidad que representa el dispositivo de teléfono real y todos sus controles.</span><span class="sxs-lookup"><span data-stu-id="b8479-104">The Phone object is the entity that represents the actual phone device and all of its controls.</span></span>

<span data-ttu-id="b8479-105">Las interfaces [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) y [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) no se exponen directamente en el objeto Phone, sino que están estrechamente relacionadas con ella y se enumeran aquí para facilitar la referencia.</span><span class="sxs-lookup"><span data-stu-id="b8479-105">The [**ITPhoneEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent) and [**IEnumPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone) interfaces are not directly exposed on the Phone object, but are tightly related to it and are listed here for convenience of reference.</span></span>



| <span data-ttu-id="b8479-106">Interfaz</span><span class="sxs-lookup"><span data-stu-id="b8479-106">Interface</span></span>                                                  | <span data-ttu-id="b8479-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8479-107">Description</span></span>                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8479-108">**ITPhone**</span><span class="sxs-lookup"><span data-stu-id="b8479-108">**ITPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphone)                                 | <span data-ttu-id="b8479-109">Permite el acceso al dispositivo telefónico en un nivel comparable al disponible en TAPI 2. *x* C API.</span><span class="sxs-lookup"><span data-stu-id="b8479-109">Allows access to the phone device at a level comparable to that available with the TAPI 2.*x* C API.</span></span>                                      |
| [<span data-ttu-id="b8479-110">**ITAutomatedPhoneControl**</span><span class="sxs-lookup"><span data-stu-id="b8479-110">**ITAutomatedPhoneControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) | <span data-ttu-id="b8479-111">Proporciona métodos para el control automatizado de tonos y anillos de un teléfono, y para el control automático de llamadas basado en el estado de conmutador de un teléfono.</span><span class="sxs-lookup"><span data-stu-id="b8479-111">Provides methods for automated control of a phone's tones and rings, and for automated call handling based on a phone's hookswitch state.</span></span> |
| [<span data-ttu-id="b8479-112">**ITPhoneEvent**</span><span class="sxs-lookup"><span data-stu-id="b8479-112">**ITPhoneEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itphoneevent)                       | <span data-ttu-id="b8479-113">Recupera la descripción de los eventos de teléfono.</span><span class="sxs-lookup"><span data-stu-id="b8479-113">Retrieves the description of phone events.</span></span>                                                                                                |
| [<span data-ttu-id="b8479-114">**IEnumPhone**</span><span class="sxs-lookup"><span data-stu-id="b8479-114">**IEnumPhone**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumphone)                           | <span data-ttu-id="b8479-115">Enumera [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span><span class="sxs-lookup"><span data-stu-id="b8479-115">Enumerates [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone).</span></span>                                                                                                    |



 

 

 



