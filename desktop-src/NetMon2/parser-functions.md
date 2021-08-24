---
description: Los analizadores llaman a las siguientes funciones auxiliares.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Funciones del analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d70c3ad44ad809a323af8acde732af3b142759d3686d78c496f47e92cb8e209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676845"
---
# <a name="parser-functions"></a>Funciones del analizador

Los analizadores llaman a las siguientes funciones auxiliares.



| Función                                                 | Descripción                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Convierte una dirección en una cadena.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Recupera la cadena correspondiente al valor especificado de un conjunto etiquetado.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Captura un puntero de instancia de contexto.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Convierte una cadena en una dirección.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Convierte un entero pequeño de longitud variable en **DWORD.**                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Recupera la cadena correspondiente al valor especificado de un conjunto etiquetado.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Recupera la cadena correspondiente al valor especificado de un conjunto etiquetado.                                      |
| [BERGetHeader](bergetheader.md)                         | Descodifica un encabezado de elección.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Descodifica un entero codificado en BER.                                                                                 |
| [BERGetString](bergetstring.md)                         | Descodifica una cadena codificada en BER.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Asigna memoria en función de la captura por captura.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Libera la memoria asignada por la **función CCHeapAlloc.**                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Reasigna la memoria asignada por la **función CCHeapAlloc.**                                                  |
| [CCHeapSize](ccheapsize.md)                             | Recupera el tamaño de la memoria asignada por la **función CCHeapAlloc.**                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Recupera el puntero a los datos de instancia agregados al contexto de captura.                                       |
| [CreateProtocol](createprotocol.md)                     | Informa a Monitor de red API de que existe un analizador de protocolo específico.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Destruye el protocolo creado por la **función CreateProtocol.**                                              |
| [BuildINIPath](buildinipath.md)                         | Recupera una ruta de acceso completa al archivo de inicialización (INI) que corresponde a la información que especifique.   |
| [CreateHandoffTable](createhandofftable.md)             | Crea una tabla de entrega basada en la información de un archivo INI determinado.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Destruye una tabla de entrega creada con la **función CreateHandoffTable.**                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Recupera el protocolo de una tabla de entrega determinada.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Agrega una **estructura PROPERTYINFO** a la base de datos de propiedades.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Asocia una instancia de propiedad a un marco.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Asocia una instancia de propiedad a un marco.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Crea una base de datos de propiedades que describe las propiedades que usa el analizador para describir sus datos.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Destruye una base de datos de propiedades creada por llamadas a las **funciones CreatePropertyDatabase** **y AddProperty.** |
| [FindNextFrame](findnextframe.md)                       | Busca el fotograma siguiente en el contexto de captura actual que coincide con un filtro determinado.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Busca el marco anterior en el contexto de captura actual que coincide con un filtro determinado.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Da formato a la instancia de propiedad de forma genérica.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Recupera la dirección de destino de un marco.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Recupera la dirección de origen de un marco.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Recupera el desplazamiento a un protocolo determinado en el marco.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Bloquea un fotograma cuando entra en un analizador y desbloquea el marco cuando se cierra.                                     |



 

Para obtener información sobre las funciones de exportación (funciones auxiliares a las que pueden llamar expertos y analizadores), estructuras y enumeraciones, vea los temas siguientes.



| Para información acerca de                                  | Vea                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones que exportan los analizadores.                         | [Funciones de exportación de DLL del analizador](parser-dll-export-functions.md)               |
| Estructuras que usan las funciones del analizador.                  | [Estructuras del analizador](parser-structures.md)                                   |
| Funciones auxiliares comunes a las que llaman los analizadores y expertos. | [Funciones comunes de expertos y analizadores](expert-and-parser-common-functions.md) |



 

 

 
