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
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

El terminal **CAudioRenderTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de representación de audio estático para dispositivos de onda mediante el filtro de WaveOut de DirectShow. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.

Definido en MSPtrmar. h.

## <a name="remarks"></a>Observaciones

Los métodos [**Put \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) y [**Get \_ balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** no se implementan y devolverán e \_ NOTIMPL.

 

 



