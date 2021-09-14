---
description: Las Monitor de red, enumeradas en la tabla siguiente, se pueden usar para desarrollar analizadores o expertos.
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: Funciones comunes de expertos y analizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260412"
---
# <a name="expert-and-parser-common-functions"></a>Funciones comunes de expertos y analizadores

Las Monitor de red, enumeradas en la tabla siguiente, se pueden usar para desarrollar [*analizadores*](p.md) o [*expertos.*](e.md)



| Función                                                               | Descripción                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [CompareAddresses](compareaddresses.md)                               | Compara dos direcciones determinadas.                                                       |
| [CompareFrameDestAddress](compareframedestaddress.md)                 | Compara una dirección determinada con la dirección de destino de un marco.                     |
| [CompareFrameSourceAddress](compareframesourceaddress.md)             | Compara una dirección determinada con la dirección de origen de un marco.                          |
| [FilterAddObject](filteraddobject.md)                                 | Agrega un único objeto a un filtro.                                                   |
| [FindPropertyInstance](findpropertyinstance.md)                       | Busca la primera instancia de una propiedad determinada.                                       |
| [FindPropertyInstanceRestart](findpropertyinstancerestart.md)         | Busca la siguiente instancia de una propiedad determinada.                                        |
| [GetCaptureComment](getcapturecomment.md)                             | Recupera el comentario de una captura.                                                 |
| [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)     | Recupera el comentario de una captura de su archivo de captura.                           |
| [GetCaptureMacType](getcapturemactype.md)                             | Recupera el tipo MAC de la captura.                                              |
| [GetCaptureTimeStamp](getcapturetimestamp.md)                         | Recupera la marca de tiempo de espera de captura.                                                |
| [GetCaptureTotalFrames](getcapturetotalframes.md)                     | Recupera los fotogramas totales de la captura.                                          |
| [GetEnabledProtocols](getenabledprotocols.md)                         | Recupera una lista de todos los protocolos marcados como habilitados.                            |
| [GetFrame](getframe.md)                                               | Recupera un identificador de un fotograma determinado.                                                |
| [GetFrameCaptureHandle](getframecapturehandle.md)                     | Recupera un identificador para una captura determinada.                                              |
| [GetFrameDstAddressOffset](getframedstaddressoffset.md)               | Recupera el desplazamiento de dirección de destino para un fotograma determinado.                         |
| [GetFrameFromFrameHandle](getframefromframehandle.md)                 | Recupera un marco para un identificador de marco determinado.                                         |
| [GetFrameLength](getframelength.md)                                   | Recupera la longitud de un fotograma determinado.                                              |
| [GetFrameMacHeaderLength](getframemacheaderlength.md)                 | Recupera la longitud del encabezado MAC para un fotograma determinado.                           |
| [GetFrameMacType](getframemactype.md)                                 | Recupera el tipo mac de un fotograma determinado.                                           |
| [GetFrameNumber](getframenumber.md)                                   | Devuelve el número de un fotograma determinado.                                                |
| [GetFrameRecognizeData](getframerecognizedata.md)                     | Recupera los identificadores de protocolo (y sus desplazamientos) de todos los protocolos reconocidos. |
| [GetFrameSrcAddressOffset](getframesrcaddressoffset.md)               | Recupera el desplazamiento a la dirección de origen de un fotograma determinado.                        |
| [GetFrameStoredLength](getframestoredlength.md)                       | Recupera la longitud de un fotograma determinado.                                              |
| [GetFrameTimeStamp](getframetimestamp.md)                             | Recupera la marca de tiempo de un fotograma determinado.                                          |
| [GetPreviousProtocolOffsetByName](getpreviousprotocoloffsetbyname.md) | Recupera la instancia anterior de un protocolo determinado.                                |
| [Getproperty](getproperty.md)                                         | Recupera una propiedad con un nombre determinado.                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | Recupera la información de una propiedad específica.                                   |
| [GetPropertyText](getpropertytext.md)                                 | Recupera el texto de una propiedad determinada.                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | Recupera un protocolo específico por nombre.                                              |
| [GetProtocolInfo](getprotocolinfo.md)                                 | Usa el identificador de protocolo para recuperar datos relacionados con el protocolo.                        |
| [GetProtocolStartOffsetHandle](getprotocolstartoffsethandle.md)       | Recupera el desplazamiento de un protocolo determinado.                                           |
| [MacTypeToAddressType](mactypetoaddresstype.md)                       | Convierte un tipo MAC en un tipo de dirección.                                             |
| [ModifyFrame](modifyframe.md)                                         | Actualiza un marco existente con datos nuevos.                                            |



 

Para obtener más información sobre las funciones y estructuras que solo usan los expertos, y las funciones y estructuras que solo usan los analizadores, vea los temas que se enumeran en la tabla siguiente.



| Para más información sobre                                          | Vea                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Funciones específicas de expertos que puede usar para desarrollar archivos DLL expertos. | [Funciones, estructuras y enumeraciones de expertos](expert-functions-structures-and-enumerations.md) |
| Funciones específicas del analizador que puede usar para desarrollar archivos DLL de analizador. | [Funciones y estructuras del analizador](parser-functions-and-structures.md)                             |



 

 

 



