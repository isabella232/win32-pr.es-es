---
description: Las funciones de Monitor de red, que se enumeran en la tabla siguiente, se pueden usar para desarrollar analizadores o expertos.
ms.assetid: 26eb4f99-a8dc-43a2-abb9-9577518b6f2f
title: Funciones comunes de experto y analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6776260610c2decb0ecf91b6373d301937d899b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666305"
---
# <a name="expert-and-parser-common-functions"></a>Funciones comunes de experto y analizador

Las funciones de Monitor de red, que se enumeran en la tabla siguiente, se pueden usar para desarrollar [*analizadores*](p.md) o [*expertos*](e.md).



| Función                                                               | Descripción                                                                         |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [CompareAddresses](compareaddresses.md)                               | Compara dos direcciones dadas.                                                       |
| [CompareFrameDestAddress](compareframedestaddress.md)                 | Compara una dirección determinada con la dirección de destino de un marco.                     |
| [CompareFrameSourceAddress](compareframesourceaddress.md)             | Compara una dirección determinada con la dirección de origen de un marco.                          |
| [FilterAddObject](filteraddobject.md)                                 | Agrega un solo objeto a un filtro.                                                   |
| [FindPropertyInstance](findpropertyinstance.md)                       | Busca la primera instancia de una propiedad determinada.                                       |
| [FindPropertyInstanceRestart](findpropertyinstancerestart.md)         | Busca la siguiente instancia de una propiedad determinada.                                        |
| [GetCaptureComment](getcapturecomment.md)                             | Recupera el comentario de una captura.                                                 |
| [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)     | Recupera el comentario de una captura de su archivo de captura.                           |
| [GetCaptureMacType](getcapturemactype.md)                             | Recupera el tipo MAC de la captura.                                              |
| [GetCaptureTimeStamp](getcapturetimestamp.md)                         | Recupera la marca de tiempo de espera de la captura.                                                |
| [GetCaptureTotalFrames](getcapturetotalframes.md)                     | Recupera el total de tramas de la captura.                                          |
| [GetEnabledProtocols](getenabledprotocols.md)                         | Recupera una lista de todos los protocolos marcados como habilitados.                            |
| [GetFrame](getframe.md)                                               | Recupera un identificador de un fotograma determinado.                                                |
| [GetFrameCaptureHandle](getframecapturehandle.md)                     | Recupera un identificador de una captura determinada.                                              |
| [GetFrameDstAddressOffset](getframedstaddressoffset.md)               | Recupera el desplazamiento de la dirección de destino para un fotograma determinado.                         |
| [GetFrameFromFrameHandle](getframefromframehandle.md)                 | Recupera un marco para un identificador de marco determinado.                                         |
| [GetFrameLength](getframelength.md)                                   | Recupera la longitud de un fotograma determinado.                                              |
| [GetFrameMacHeaderLength](getframemacheaderlength.md)                 | Recupera la longitud del encabezado MAC para un fotograma determinado.                           |
| [GetFrameMacType](getframemactype.md)                                 | Recupera el tipo MAC para un fotograma determinado.                                           |
| [GetFrameNumber](getframenumber.md)                                   | Devuelve el número de un fotograma determinado.                                                |
| [GetFrameRecognizeData](getframerecognizedata.md)                     | Recupera los identificadores de protocolo (y sus desplazamientos) de todos los protocolos reconocidos. |
| [GetFrameSrcAddressOffset](getframesrcaddressoffset.md)               | Recupera el desplazamiento de la dirección de origen de un fotograma determinado.                        |
| [GetFrameStoredLength](getframestoredlength.md)                       | Recupera la longitud de un fotograma determinado.                                              |
| [GetFrameTimeStamp](getframetimestamp.md)                             | Recupera la marca de tiempo de un fotograma determinado.                                          |
| [GetPreviousProtocolOffsetByName](getpreviousprotocoloffsetbyname.md) | Recupera la instancia anterior de un protocolo determinado.                                |
| [GetProperty](getproperty.md)                                         | Recupera una propiedad con un nombre determinado.                                             |
| [GetPropertyInfo](getpropertyinfo.md)                                 | Recupera la información de una propiedad específica.                                   |
| [GetPropertyText](getpropertytext.md)                                 | Recupera el texto de una propiedad determinada.                                             |
| [GetProtocolFromName](getprotocolfromname.md)                         | Recupera un protocolo específico por nombre.                                              |
| [GetProtocolInfo](getprotocolinfo.md)                                 | Utiliza el identificador de protocolo para recuperar los datos relacionados con el protocolo.                        |
| [GetProtocolStartOffsetHandle](getprotocolstartoffsethandle.md)       | Recupera el desplazamiento de un protocolo determinado.                                           |
| [MacTypeToAddressType](mactypetoaddresstype.md)                       | Convierte un tipo MAC en un tipo de dirección.                                             |
| [ModifyFrame](modifyframe.md)                                         | Actualiza un marco existente con nuevos datos.                                            |



 

Para obtener más información sobre las funciones y estructuras que solo usan los expertos, y las funciones y estructuras que solo usan los analizadores, vea los temas que se muestran en la tabla siguiente.



| Para más información sobre                                          | Vea                                                                                                |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Funciones específicas del experto que se pueden usar para desarrollar archivos dll de expertos. | [Funciones, estructuras y enumeraciones de expertos](expert-functions-structures-and-enumerations.md) |
| Funciones específicas del analizador que puede usar para desarrollar archivos dll de analizador. | [Funciones y estructuras del analizador](parser-functions-and-structures.md)                             |



 

 

 



