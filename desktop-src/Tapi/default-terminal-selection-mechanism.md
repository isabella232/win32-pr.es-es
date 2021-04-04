---
description: El concepto de terminal multipista hace que sea más conveniente para TAPI proporcionar un método simplificado para seleccionar un terminal en una secuencia o en secuencias. El mecanismo de selección de terminal predeterminado está diseñado para solucionar este objetivo.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Mecanismo de selección de terminal predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907793"
---
# <a name="default-terminal-selection-mechanism"></a>Mecanismo de selección de terminal predeterminado

El concepto de [terminal multipista](multitrack-terminals.md) hace que sea más conveniente para TAPI proporcionar un método simplificado para seleccionar un terminal en una secuencia o en secuencias. El mecanismo de selección de terminal predeterminado está diseñado para solucionar este objetivo.

## <a name="selecting-a-terminal-on-a-call"></a>Selección de un terminal en una llamada

La característica selección de terminal predeterminada se proporciona a través de la capacidad de seleccionar un terminal en una llamada.

El [objeto Call](call-object.md) expone una nueva interfaz, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). La interfaz expone los mismos métodos que [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), además de tres nuevos métodos: [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)y [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).

**ITBasicCallControl2:: RequestTerminal** crea un terminal, dada la clase de terminal, la dirección y el tipo de medio. Examina las listas de los terminales estáticos y dinámicos compatibles para buscar y crear el terminal solicitado.

[**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) selecciona el terminal (o, en el caso de un terminal Multipista, enumera, crea si es necesario y selecciona el seguimiento de los terminales) en la secuencia (o secuencias) disponible en la llamada.

El algoritmo para hacer coincidir secuencias de llamadas con el terminal (o las pistas disponibles en el terminal) se describe en la documentación de [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

La llamada a [**ITBasicCallControl2:: UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) hace que se anule la selección de la llamada del terminal (una sola pista o Multipista). Consulte la documentación del método para obtener más detalles.

## <a name="selecting-a-terminal-on-itstream"></a>Selección de un terminal en ITStream

La selección de un terminal de una sola pista en [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (mediante una llamada a [**ITStream:: SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) selecciona el terminal en la secuencia. Este es el procedimiento habitual de selección de terminales de TAPI 3.

Solo se pueden seleccionar terminales de un solo seguimiento en una secuencia. La selección de un terminal multipista en una secuencia producirá un error, ya que la secuencia no reconocerá el tipo y la dirección del medio.

 

 
