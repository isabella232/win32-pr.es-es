---
description: La función phoneDevSpecific y su \_ mensaje DEVSPECIFIC de teléfono asociado permiten a una aplicación tener acceso a características telefónicas específicas del dispositivo que no están disponibles a través de los servicios de telefonía comunes para teléfonos.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funciones y mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001929"
---
# <a name="functions-and-messages"></a><span data-ttu-id="a2ec2-103">Funciones y mensajes</span><span class="sxs-lookup"><span data-stu-id="a2ec2-103">Functions and Messages</span></span>

<span data-ttu-id="a2ec2-104">La función [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) y su mensaje [**\_ DEVSPECIFIC de teléfono**](phone-devspecific.md) asociado permiten a una aplicación tener acceso a características telefónicas específicas del dispositivo que no están disponibles a través de los servicios de telefonía comunes para teléfonos.</span><span class="sxs-lookup"><span data-stu-id="a2ec2-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="a2ec2-105">En otras palabras, **phoneDevSpecific** es la función de escape específica del dispositivo que permite extensiones dependientes del proveedor y teléfono \_ DEVSPECIFIC es el mensaje específico del dispositivo que se envía a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a2ec2-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="a2ec2-106">El perfil de parámetro de la función [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) es genérico, ya que la interpretación de los parámetros la realiza TAPI.</span><span class="sxs-lookup"><span data-stu-id="a2ec2-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="a2ec2-107">En su lugar, la interpretación de los parámetros se define mediante el proveedor de servicios y debe ser entendida por una aplicación que los utiliza.</span><span class="sxs-lookup"><span data-stu-id="a2ec2-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="a2ec2-108">Los parámetros se pasan simplemente por TAPI desde la aplicación al proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="a2ec2-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="a2ec2-109">Normalmente, una aplicación que se basa en extensiones específicas del dispositivo no funcionará con otros proveedores de servicios, pero las aplicaciones escritas en los servicios del teléfono de telefonía común funcionarán con el proveedor de servicios extendidos.</span><span class="sxs-lookup"><span data-stu-id="a2ec2-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



