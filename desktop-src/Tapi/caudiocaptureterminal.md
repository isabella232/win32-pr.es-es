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
# <a name="caudiocaptureterminal"></a>CAudioCaptureTerminal

El terminal **CAudioCaptureTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de audio estático para dispositivos de onda mediante el filtro de onda de DirectShow. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.

Definido en MSPtmac. h.

## <a name="remarks"></a>Observaciones

Los métodos [**Put \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) y [**Get \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioCaptureTerminal** no se implementan y devolverán e \_ NOTIMPL.

 

 



