---
description: Los analizadores llaman a las siguientes funciones auxiliares.
ms.assetid: 4e9a9314-8d64-46c0-ad98-bdb9dc4c225a
title: Funciones de analizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a502778247a3daad5f11dd8d0e2a3312d586d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153846"
---
# <a name="parser-functions"></a>Funciones de analizador

Los analizadores llaman a las siguientes funciones auxiliares.



| Función                                                 | Descripción                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [AddressToString](addresstostring.md)                   | Convierte una dirección en una cadena.                                                                               |
| [LookupByteSetString](lookupbytesetstring.md)           | Recupera la cadena correspondiente al valor especificado de un conjunto con etiqueta.                                    |
| [SetCCInstPtr](setccinstptr.md)                         | Captura un puntero de instancia de contexto.                                                                           |
| [StringToAddress](stringtoaddress.md)                   | Convierte una cadena en una dirección.                                                                               |
| [VarLenSmallIntToDword](varlensmallinttodword.md)       | Convierte un entero pequeño de longitud variable en un **valor DWORD**.                                                      |
| [LookupDwordSetString](lookupdwordsetstring.md)         | Recupera la cadena correspondiente al valor especificado de un conjunto con etiqueta.                                    |
| [LookupWordSetString](lookupwordsetstring.md)           | Recupera la cadena correspondiente al valor especificado de un conjunto etiquetado.                                      |
| [BERGetHeader](bergetheader.md)                         | Descodifica un encabezado Choice.                                                                                       |
| [BERGetInteger](bergetinteger.md)                       | Descodifica un entero con codificación BER.                                                                                 |
| [BERGetString](bergetstring.md)                         | Descodifica una cadena codificada en BER.                                                                                  |
| [CCHeapAlloc](ccheapalloc.md)                           | Asigna memoria en función de la captura.                                                                |
| [CCHeapFree](ccheapfree.md)                             | Libera la memoria asignada por la función **CCHeapAlloc** .                                                 |
| [CCHeapReAlloc](ccheaprealloc.md)                       | Reasigna la memoria asignada por la función **CCHeapAlloc** .                                                  |
| [CCHeapSize](ccheapsize.md)                             | Recupera el tamaño de la memoria asignada por la función **CCHeapAlloc** .                                    |
| [GetCCInstPtr](getccinstptr.md)                         | Recupera el puntero a los datos de instancia agregados al contexto de captura.                                       |
| [CreateProtocol](createprotocol.md)                     | Informa a la API de Monitor de red de que existe un analizador de protocolo específico.                                        |
| [DestroyProtocol](destroyprotocol.md)                   | Destruye el protocolo creado por la función **CreateProtocol** .                                              |
| [BuildINIPath](buildinipath.md)                         | Recupera una ruta de acceso completa al archivo de inicialización (INI) que corresponde a la información que especifique.   |
| [CreateHandoffTable](createhandofftable.md)             | Crea una tabla de entrega basada en la información de un archivo INI determinado.                                             |
| [DestroyHandoffTable](destroyhandofftable.md)           | Destruye una tabla de entrega creada con la función **CreateHandoffTable** .                                     |
| [GetProtocolFromTable](getprotocolfromtable.md)         | Recupera el protocolo de una tabla de entrega determinada.                                                               |
| [AddProperty](/previous-versions/bb251873(v=msdn.10))                           | Agrega una estructura **PROPERTYINFO** a la base de datos de propiedades.                                                    |
| [AttachPropertyInstance](attachpropertyinstance.md)     | Adjunta una instancia de propiedad a un marco.                                                                       |
| [AttachPropertyInstanceEx](attachpropertyinstanceex.md) | Adjunta una instancia de propiedad a un marco.                                                                       |
| [CreatePropertyDatabase](createpropertydatabase.md)     | Crea una base de datos de propiedades que describe las propiedades que utiliza el analizador para describir sus datos.               |
| [DestroyPropertyDatabase](destroypropertydatabase.md)   | Destruye una base de datos de propiedades creada mediante llamadas a las funciones **CreatePropertyDatabase** y **AddProperty** . |
| [FindNextFrame](findnextframe.md)                       | Busca el siguiente fotograma en el contexto de captura actual que coincide con un filtro determinado.                               |
| [FindPreviousFrame](findpreviousframe.md)               | Busca el fotograma anterior en el contexto de captura actual que coincide con un filtro determinado.                           |
| [FormatPropertyInstance](formatpropertyinstance.md)     | Da formato a la instancia de propiedad de forma genérica.                                                             |
| [GetFrameDestAddress](getframedestaddress.md)           | Recupera la dirección de destino de un marco.                                                                  |
| [GetFrameSourceAddress](getframesourceaddress.md)       | Recupera la dirección de origen de un marco.                                                                       |
| [GetProtocolStartOffset](getprotocolstartoffset.md)     | Recupera el desplazamiento a un protocolo determinado en el marco.                                                         |
| [ParserTemporaryLockFrame](parsertemporarylockframe.md) | Bloquea un marco cuando entra en un analizador y desbloquea el marco cuando se cierra.                                     |



 

Para obtener información sobre las funciones de exportación (funciones auxiliares a las que pueden llamar expertos y analizadores), estructuras y enumeraciones, vea los temas siguientes.



| Para información acerca de                                  | Vea                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------|
| Funciones que los analizadores exportan.                         | [Funciones de exportación de DLL de analizador](parser-dll-export-functions.md)               |
| Estructuras que usan las funciones de analizador.                  | [Estructuras de analizador](parser-structures.md)                                   |
| Funciones auxiliares comunes a las que llaman los analizadores y expertos. | [Funciones comunes de experto y analizador](expert-and-parser-common-functions.md) |



 

 

 
