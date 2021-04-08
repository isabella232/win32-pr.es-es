---
description: Un solo teléfono puede sonar con distintos modos de anillo.
ms.assetid: c5ddcb3c-183c-4f97-9429-977d5cc32668
title: En anillo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671aac6ead1938ff5b35ecb4996e4bc072a66d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001925"
---
# <a name="ring"></a><span data-ttu-id="2ff7d-103">En anillo</span><span class="sxs-lookup"><span data-stu-id="2ff7d-103">Ring</span></span>

<span data-ttu-id="2ff7d-104">Un solo teléfono puede sonar con distintos modos de anillo.</span><span class="sxs-lookup"><span data-stu-id="2ff7d-104">A single phone may be able to ring with different ring modes.</span></span> <span data-ttu-id="2ff7d-105">Dada la amplia variedad de modos de anillo disponibles, los modos de anillo se identifican por medio de su número de modo de anillo.</span><span class="sxs-lookup"><span data-stu-id="2ff7d-105">Given the wide variety of ring modes available, ring modes are identified by means of their ring mode number.</span></span> <span data-ttu-id="2ff7d-106">Un número de modo de anillo oscila entre cero y el número de modos de anillo disponibles menos uno.</span><span class="sxs-lookup"><span data-stu-id="2ff7d-106">A ring mode number ranges from zero to the number of available ring modes minus one.</span></span>

<span data-ttu-id="2ff7d-107">Las funciones que utiliza una aplicación para controlar los modos de anillo de un dispositivo telefónico son [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), que suena un dispositivo telefónico abierto según un modo de anillo determinado y [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), que devuelve el modo de anillo actual de un dispositivo telefónico abierto.</span><span class="sxs-lookup"><span data-stu-id="2ff7d-107">The functions an application would use to control a phone device's ring modes are [**phoneSetRing**](/windows/desktop/api/Tapi/nf-tapi-phonesetring), which rings an open phone device according to a given ring mode, and [**phoneGetRing**](/windows/desktop/api/Tapi/nf-tapi-phonegetring), which returns the current ring mode of an opened phone device.</span></span>

<span data-ttu-id="2ff7d-108">Cuando se cambia el modo de anillo de un dispositivo telefónico, se envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) a la aplicación para notificar a la aplicación sobre el cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="2ff7d-108">When the ring mode of a phone device is changed, a [**PHONE\_STATE**](phone-state.md) message is sent to the application to notify the application about the state change.</span></span> <span data-ttu-id="2ff7d-109">Los parámetros de este mensaje proporcionan una indicación del cambio.</span><span class="sxs-lookup"><span data-stu-id="2ff7d-109">Parameters to this message provide an indication of the change.</span></span>

 

 



