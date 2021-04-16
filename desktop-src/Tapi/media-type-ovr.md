---
description: El tipo de medio (o modo) de un dispositivo describe el tipo de información que se puede intercambiar, como la voz interactiva. Es posible que un dispositivo determinado solo pueda controlar un tipo de medio, o bien que pueda tratar con un intervalo de tipos.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo de soporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678631"
---
# <a name="media-type"></a><span data-ttu-id="a3fc4-104">Tipo de soporte</span><span class="sxs-lookup"><span data-stu-id="a3fc4-104">Media Type</span></span>

<span data-ttu-id="a3fc4-105">El *tipo de medio* (o modo) de un dispositivo describe el tipo de información que se puede intercambiar, como la voz interactiva.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="a3fc4-106">Es posible que un dispositivo determinado solo pueda controlar un tipo de medio, o bien que pueda tratar con un intervalo de tipos.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="a3fc4-107">Los proveedores de servicios exponen el tipo o los tipos de medios admitidos por los dispositivos que controlan.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="a3fc4-108">Las aplicaciones consultan el tipo de medio y, a continuación, usan esta información para seleccionar una dirección adecuada en la que iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="a3fc4-109">La respuesta de la aplicación a una sesión ofrecida también se puede predicar en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="a3fc4-110">Una sesión de comunicaciones determinada, o llamada, puede implicar varios tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="a3fc4-111">Para obtener más información, consulte tipo de medio para una sesión.</span><span class="sxs-lookup"><span data-stu-id="a3fc4-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="a3fc4-112">**TAPI 2. x:** Vea [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), miembro **dwAvailableMediaModes** de la estructura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) a la que apunta *lpAddressCaps*, [LINEMEDIAMODE \_ constantes](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="a3fc4-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="a3fc4-113">**TAPI 3. x:** Vea [**ITTerminal:: get \_ mediatype**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="a3fc4-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
