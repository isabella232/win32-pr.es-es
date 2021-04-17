---
description: El terminal CAudioCaptureTerminal se deriva de CSingleFilterTerminal e implementa un terminal de captura de audio estático para dispositivos de onda mediante el filtro de onda de DirectShow. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678117"
---
# <a name="caudiocaptureterminal"></a><span data-ttu-id="aba18-104">CAudioCaptureTerminal</span><span class="sxs-lookup"><span data-stu-id="aba18-104">CAudioCaptureTerminal</span></span>

<span data-ttu-id="aba18-105">El terminal **CAudioCaptureTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de audio estático para dispositivos de onda mediante el filtro de onda de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="aba18-105">The **CAudioCaptureTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio capture terminal for wave devices using the DirectShow wavein filter.</span></span> <span data-ttu-id="aba18-106">La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.</span><span class="sxs-lookup"><span data-stu-id="aba18-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="aba18-107">Definido en MSPtmac. h.</span><span class="sxs-lookup"><span data-stu-id="aba18-107">Defined in MSPtmac.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="aba18-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aba18-108">Remarks</span></span>

<span data-ttu-id="aba18-109">Los métodos [**Put \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) y [**Get \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioCaptureTerminal** no se implementan y devolverán e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="aba18-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioCaptureTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



