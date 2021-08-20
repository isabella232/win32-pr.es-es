---
description: En la arquitectura TAPI, todos los TSP se ejecutan en el contexto de TAPISRV, que se implementa como un proceso de servicio dentro de SVCHOST.
ms.assetid: f47662f9-2fca-4044-ab26-617e5b1f9eae
title: Arquitectura de MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cf5d95cf568e17b53c575f6c2f8963baa4b698cc69243ee1a23e9306ad6b31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002853"
---
# <a name="msp-architecture"></a>Arquitectura de MSP

En la arquitectura TAPI, todos los TSP se ejecutan en el contexto de TAPISRV, que se implementa como un proceso de servicio dentro de SVCHOST. Las aplicaciones TAPI se menten en su propio proceso. Las aplicaciones TAPI cargan Tapi3.dll y cualquier MSP necesario en su propio proceso, y el archivo DLL de TAPI se comunica con TAPISRV a través de una interfaz RPC privada. En el diagrama siguiente se muestra la interacción de estos componentes.

![interacciones entre tapisrv, aplicaciones tapi y msps](images/tsp-msp1.png)

Un proveedor de servicios multimedia (MSP) proporciona streaming multimedia mediante las abstracciones de terminales, Secuencias y substreams.

Un terminal es un receptor o origen de una secuencia multimedia. Puede ser un objeto físico, como un altavoz o un micrófono, o puede ser una abstracción de un dispositivo, como una ventana de vídeo. El [objeto terminal](terminal-object.md) expone la interfaz [**ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) La clase de terminal se describe mediante el [**GUID de la clase terminal.**](terminal-class.md) Un MSP puede definir sus propias clases de terminal.

Secuencias el medio de una llamada en [](tapimediatype--constants.md) función del tipo o [](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction)tipo de medio, la dirección del flujo y la dirección de destino del medio. Por ejemplo, una secuencia de audio entrante de un módem es un objeto de secuencia, una secuencia de vídeo saliente a una dirección IP y el puerto es un objeto de secuencia, las secuencias de vídeo procedentes de un grupo de multidifusión IP también se consideran un objeto de secuencia. El objeto Stream se representa mediante la [**interfaz ITStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)

Las substreams permiten un control más preciso sobre los medios. Por ejemplo, en el caso de multidifusión IP, el objeto de secuencia de vídeo entrante podría representar varias personas. Lo más probable es que la aplicación quiera que cada participante tenga un representador independiente. La secuencia de vídeo entrante se puede dividir en varias secuencias, una para cada persona. Una subsección correspondería a una persona y se puede configurar y controlar por separado. El objeto SubStream se representa mediante la [**interfaz ITSubStreamControl.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol)

Cuando una aplicación llama a [**ITAddress::CreateCall para**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) configurar una llamada, debe especificar el tipo de medio necesario. En una llamada saliente, simplemente indica a TAPI cuándo se crea la llamada. Por ejemplo:

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

Los tipos de medios pasados en indican los medios en los que la aplicación está interesada a lo largo de la duración de la llamada. Por ejemplo, la aplicación puede especificar audio y vídeo al crear la llamada, pero seleccionar solo terminales de audio al principio. El MSP comenzará a transmitir solo audio, pero no rechazará una solicitud de vídeo local o remota realizada más adelante en la duración de la llamada.

Cuando la aplicación llama a [**ITBasicCallControl::Conectar**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), TAPI 3 llama a la línea [**\_ TSPIMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) en el TSP. Una vez establecida una llamada, msp y TSP se pueden comunicar según sea necesario.

Cuando una llamada se desconecta, es el MSP y el TSP los que deben comunicarse sobre la desconexión de la llamada. Tapi3.dll llamará a [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) si la aplicación llama [**a Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
