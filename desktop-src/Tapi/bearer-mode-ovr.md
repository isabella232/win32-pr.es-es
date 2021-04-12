---
description: El modo de portador corresponde a la calidad de la transmisión solicitada desde la red para establecer una llamada.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Modo de portador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276163"
---
# <a name="bearer-mode"></a><span data-ttu-id="dc0f8-103">Modo de portador</span><span class="sxs-lookup"><span data-stu-id="dc0f8-103">Bearer Mode</span></span>

<span data-ttu-id="dc0f8-104">El [**modo de portador**](./linebearermode--constants.md) corresponde a la calidad de la transmisión solicitada desde la red para establecer una llamada.</span><span class="sxs-lookup"><span data-stu-id="dc0f8-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="dc0f8-105">Es importante mantener el concepto de modo de portador independiente del [**tipo de medio**](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="dc0f8-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="dc0f8-106">Por ejemplo, la red de teléfono analógica (PSTN) solo proporciona un modo de portador de voz de 3,1 kHz, pero las llamadas que lo usan pueden admitir tipos de medios como voz, fax o módem de datos.</span><span class="sxs-lookup"><span data-stu-id="dc0f8-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="dc0f8-107">El modo de portador de una llamada se especifica cuando se configura la llamada o se proporciona cuando se ofrece la llamada.</span><span class="sxs-lookup"><span data-stu-id="dc0f8-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="dc0f8-108">Con los dispositivos de línea capaces de representar grupos de canales, es posible que un proveedor de servicios permita que las llamadas se establezcan con un ancho de banda mayor.</span><span class="sxs-lookup"><span data-stu-id="dc0f8-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="dc0f8-109">No todos los proveedores de servicios admiten el uso de esta información.</span><span class="sxs-lookup"><span data-stu-id="dc0f8-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="dc0f8-110">**TAPI 2. x:** Consulte [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="dc0f8-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="dc0f8-111">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ BEARERMODE** miembro de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="dc0f8-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="dc0f8-112">**TSPI:** Vea el mensaje [**line \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) con *dwParam1* establecido en LINECALLINFOSTATE \_ BEARERMODE.</span><span class="sxs-lookup"><span data-stu-id="dc0f8-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
