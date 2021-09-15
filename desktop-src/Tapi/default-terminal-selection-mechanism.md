---
description: El concepto de terminal multipista hace que sea aún más deseable que TAPI proporcione un método simplificado para seleccionar un terminal en un flujo o secuencias. El mecanismo de selección de terminal predeterminado está diseñado para solucionar este problema.
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: Mecanismo de selección de terminal predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270508"
---
# <a name="default-terminal-selection-mechanism"></a>Mecanismo de selección de terminal predeterminado

El concepto de [terminal multipista](multitrack-terminals.md) hace aún más conveniente que TAPI proporcione un método simplificado para seleccionar un terminal en un flujo o secuencias. El mecanismo de selección de terminal predeterminado está diseñado para solucionar este problema.

## <a name="selecting-a-terminal-on-a-call"></a>Selección de un terminal en una llamada

La característica Selección de terminal predeterminada se proporciona a través de la capacidad de seleccionar un terminal en una llamada.

El [objeto de](call-object.md) llamada expone una nueva interfaz, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2). La interfaz expone los mismos métodos que [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), además de tres métodos nuevos: [**RequestTerminal,**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal) [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)y [**UnselectTerminalOnCall.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall)

**ITBasicCallControl2::RequestTerminal** crea un terminal, dada la clase de terminal, la dirección y el tipo de medio. Examina las listas de terminales estáticos y dinámicos admitidos para buscar y crear el terminal solicitado.

[**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) selecciona el terminal (o, en el caso de un terminal multipista, enumera, crea si es necesario y selecciona los terminales de seguimiento) en la secuencia (o secuencias) disponible en la llamada.

El algoritmo para hacer coincidir secuencias de llamada al terminal (o pistas disponibles en el terminal) se describe en la documentación de [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).

Al llamar a [**ITBasicCallControl2::UnselectTerminalOnCall,**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) se anula la selección del terminal (de un solo seguimiento o de varios seguimientos) de la llamada. Consulte la documentación del método para obtener más detalles.

## <a name="selecting-a-terminal-on-itstream"></a>Selección de un terminal en ITStream

Al seleccionar un terminal de un solo seguimiento en [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (mediante una llamada a [**ITStream::SelectTerminal),**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)se selecciona el terminal en la secuencia. Este es el procedimiento habitual de selección del terminal TAPI 3.

Solo se pueden seleccionar terminales de un solo seguimiento en una secuencia. Se producirá un error al seleccionar un terminal multipista en una secuencia, ya que la secuencia no reconocerá el tipo de medio ni la dirección.

 

 
