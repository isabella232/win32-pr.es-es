---
description: El tipo de medio (o modo) describe el tipo de información que se intercambia, como la voz interactiva. Una sesión de comunicaciones determinada puede incluir varios tipos de medios.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo de medio para una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547374"
---
# <a name="media-type-for-a-session"></a><span data-ttu-id="b7f20-104">Tipo de medio para una sesión</span><span class="sxs-lookup"><span data-stu-id="b7f20-104">Media Type for a Session</span></span>

<span data-ttu-id="b7f20-105">El tipo de medio (o modo) describe el tipo de información que se intercambia, como la voz interactiva.</span><span class="sxs-lookup"><span data-stu-id="b7f20-105">The media type (or mode) describes the type of information being exchanged, such as interactive voice.</span></span> <span data-ttu-id="b7f20-106">Una sesión de comunicaciones determinada puede incluir varios tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="b7f20-106">A given communications session may involve several media types.</span></span>

<span data-ttu-id="b7f20-107">Los proveedores de servicios exponen a TAPI y a las aplicaciones el tipo de medios o los tipos que admiten.</span><span class="sxs-lookup"><span data-stu-id="b7f20-107">Service providers expose to TAPI and to applications the media type or types they support.</span></span> <span data-ttu-id="b7f20-108">Consulte información general sobre el [tipo de medios](media-type-ovr.md) de dispositivo para obtener información sobre la adquisición de estos datos.</span><span class="sxs-lookup"><span data-stu-id="b7f20-108">See the device [media type](media-type-ovr.md) overview for information on acquiring this data.</span></span>

<span data-ttu-id="b7f20-109">**TAPI 2. x:** Consulte [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**line \_ MONITORMEDIA**](./line-monitormedia.md) Message, [LINEMEDIAMODE \_ constantes](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b7f20-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE\_MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="b7f20-110">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent:: get \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (devuelve [**CALLINFOCHANGE \_ causa**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) de un de **CIC \_**), [TAPIMEDIATYPE \_ constantes](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b7f20-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC\_MEDIATYPE**), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>

 

 
