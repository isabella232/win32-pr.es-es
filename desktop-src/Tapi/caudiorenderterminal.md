---
description: El terminal CAudioRenderTerminal se deriva de CSingleFilterTerminal e implementa un terminal de representación de audio estático para dispositivos de onda mediante el filtro de WaveOut de DirectShow. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687891"
---
# <a name="caudiorenderterminal"></a><span data-ttu-id="2b8b9-104">CAudioRenderTerminal</span><span class="sxs-lookup"><span data-stu-id="2b8b9-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="2b8b9-105">El terminal **CAudioRenderTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de representación de audio estático para dispositivos de onda mediante el filtro de WaveOut de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="2b8b9-106">La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="2b8b9-107">Definido en MSPtrmar. h.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b8b9-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b8b9-108">Remarks</span></span>

<span data-ttu-id="2b8b9-109">Los métodos [**Put \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) y [**Get \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** no se implementan y devolverán e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="2b8b9-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



