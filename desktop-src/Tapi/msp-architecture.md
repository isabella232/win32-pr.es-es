---
description: En la arquitectura de TAPI, todas las profesionales se ejecutan en el contexto de TAPISRV, que se implementa como un proceso de servicio en SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Arquitectura MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c1229ddce90f79c122c47572b4567d230b0b4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423603"
---
# <a name="msp-architecture"></a>Arquitectura MSP

En la arquitectura de TAPI, todas las profesionales se ejecutan en el contexto de TAPISRV, que se implementa como un proceso de servicio en SVCHOST. Las aplicaciones TAPI viven en su propio proceso. Las aplicaciones TAPI cargan Tapi3.dll y los MSP necesarios en su propio proceso, y el archivo DLL de TAPI se comunica con TAPISRV a través de una interfaz RPC privada. En el diagrama siguiente se muestra la interacción de estos componentes.

![interacciones entre tapisrv, aplicaciones TAPI y MSP](images/tsp-msp1.png)

Un proveedor de servicios multimedia (MSP) proporciona streaming multimedia mediante las abstracciones de terminales, secuencias y subsecuencias.

Un terminal es un receptor u origen para una secuencia de medios. Puede tratarse de un objeto físico, como un altavoz o un micrófono, o puede ser una abstracción de un dispositivo, como una ventana de vídeo. El [objeto terminal](terminal-object.md) expone la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . La clase de terminal se describe mediante el GUID de la [**clase de terminal**](terminal-class.md) . Un MSP puede definir sus propias clases de terminal.

Las secuencias dividen el medio de una llamada en función del tipo o tipo de [**medio**](tapimediatype--constants.md) , la [**Dirección**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)de la secuencia y la dirección de destino del medio. Por ejemplo, una secuencia de audio entrante desde un módem es un objeto de flujo, una secuencia de vídeo saliente a una dirección IP y un puerto es un objeto de flujo, las secuencias de vídeo procedentes de un grupo de multidifusión IP también se consideran un objeto de flujo. El objeto de secuencia se representa mediante la interfaz [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) .

Las subsecuencias permiten un mayor control sobre los medios. Por ejemplo, en el caso de multidifusión IP, el objeto de flujo de vídeo entrante podría representar varias personas. Lo más probable es que la aplicación desee que cada participante tenga un representador independiente. El flujo de vídeo entrante puede dividirse en varios subflujos, uno para cada persona. Una subsecuencia se corresponderá con una persona y se puede configurar y controlar por separado. El objeto de subsecuencia se representa mediante la interfaz [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) .

Cuando una aplicación llama a [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) para configurar una llamada, debe especificar el tipo de medio necesario. En una llamada de salida, simplemente indica a TAPI cuando se crea la llamada. Por ejemplo:

``` syntax
HRESULT hr = pAddress->CreateCall( 
       pszDestAddress, 
       lAddressType, 
       TAPIMEDIATYPE_AUDIO | TAPIMEDIATYPE_VIDEO, 
       &pCall 
       ); 
// If (hr != S_OK ) process the error here
```

En este caso, la aplicación está creando una llamada de audio y vídeo saliente.

Los tipos de medios que se pasan en indican el medio en el que está interesado la aplicación a lo largo de la duración de la llamada. Por ejemplo, la aplicación puede especificar audio y vídeo al crear la llamada, pero seleccionar solo los terminales de audio al principio. El MSP iniciará el streaming solo de audio, pero no rechazará una solicitud de vídeo local o remota realizada más tarde en la duración de la llamada.

Cuando la aplicación llama a [**ITBasicCallControl:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 llama a [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) en el TSP. Después de establecer una llamada, MSP y TSP pueden comunicarse según sea necesario.

Cuando se está desconectando una llamada, el MSP y el TSP se comunican a través de la interrupción de la llamada. Tapi3.dll llamará a [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) si la aplicación llama a [**Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
