---
description: El terminal CAudioRenderTerminal se deriva de CSingleFilterTerminal e implementa un terminal de representación de audio estático para dispositivos de onda mediante el filtro de DirectShow de onda. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1baaa4a2d1e5d7bbe3b72de19de8593be8976ed662e27595dccea4b7432daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869820"
---
# <a name="caudiorenderterminal"></a>CAudioRenderTerminal

El terminal **CAudioRenderTerminal** se deriva de [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminal de representación de audio estático para dispositivos de onda mediante el filtro de DirectShow de onda. La mayoría de los MSP no tendrán que invalidar la implementación de este terminal.

Se define en MSPtrmar.h.

## <a name="remarks"></a>Comentarios

Los [**\_ métodos put Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) y [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) de **CAudioRenderTerminal** no se implementan y devolverán E \_ NOTIMPL.

 

 



