---
description: El terminal CAudioCaptureTerminal se deriva de CSingleFilterTerminal e implementa un terminal de captura de audio estático para dispositivos de onda mediante el DirectShow wavein. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.
ms.assetid: 2860bf22-46ae-484a-a47b-0d7057b900a1
title: CAudioCaptureTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308af17ce7a7cb4d2d4cadebb43b06437ec14abc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068778"
---
# <a name="caudiocaptureterminal"></a>CAudioCaptureTerminal

El terminal **CAudioCaptureTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de captura de audio estático para dispositivos de onda mediante el DirectShow wavein. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.

Se define en MSPtmac.h.

## <a name="remarks"></a>Observaciones

Los [**\_ métodos put Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) y [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioCaptureTerminal** no se implementan y devolverán E \_ NOTIMPL.

 

 



