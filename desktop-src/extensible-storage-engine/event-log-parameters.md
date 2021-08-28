---
description: 'Más información sobre: Parámetros del registro de eventos'
title: Parámetros del registro de eventos
TOCTitle: Event Log Parameters
ms:assetid: c660f555-2627-4d25-8f1c-8c1dc8a3a381
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294086(v=EXCHG.10)
ms:contentKeyID: 32765701
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1c127f538ae80e8bec3dc5a34d5924b838b51ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465882"
---
# <a name="event-log-parameters"></a>Parámetros del registro de eventos


_**Se aplica a:** Windows | Windows Servidor_

## <a name="event-log-parameters"></a>Parámetros del registro de eventos

Este tema contiene parámetros que se usan para el registro de eventos.

JET_paramEventLogCache  
Este parámetro controla el tamaño (en bytes) de una caché de mensajes de registro de eventos que contendrán los mensajes de registro de eventos emitidos por el motor de base de datos mientras se detiene el servicio eventlog. Estos mensajes almacenados en caché se vaciarán en el registro de eventos cuando el servicio entre en funcionamiento. Se descartarán los mensajes que desbordan la memoria caché.


| | | <p>Valor predeterminado:</p> | <p>0</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Ámbito:</p> | <p>Global</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>No</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>Sí</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramEventLoggingLevel*  
  
Este parámetro configura el nivel de detalle de los mensajes de registro de eventos que el motor de base de datos emite al registro de eventos. Los números más altos darán como resultado mensajes de registro de eventos más detallados.


| | | <p>Valor predeterminado:</p> | <p>JET_EventLoggingLevelMax</p> | | <p>Escriba:</p> | <p>Entero</p> | | <p>Intervalo válido:</p> | <p>JET_EventLoggingDisable: JET_EventLoggingLevelMax</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Windows XP y versiones posteriores</p> | 



*JET_paramEventSource*  
4  

Este parámetro proporciona una cadena específica de la aplicación que se agregará a los mensajes del registro de eventos emitidos por el motor de base de datos. Esto permite una correlación sencilla de los mensajes del registro de eventos con la aplicación de origen. Si se especifica una cadena vacía (como es el valor predeterminado), se usará el nombre ejecutable de la aplicación host.


| | | <p>Valor predeterminado:</p> | <p>""</p> | | <p>Escriba:</p> | <p>Cadena</p> | | <p>Intervalo válido:</p> | <p>De 0 a 259 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramEventSourceKey*  
49  

Este parámetro se puede usar para controlar qué registro de eventos usa el motor de base de datos para sus mensajes de registro de eventos. De forma predeterminada, todos los mensajes del registro de eventos irán al registro de eventos de la aplicación. Si el nombre de la clave del Registro para otro registro de eventos está configurado, los mensajes del registro de eventos irán allí en su lugar.


| | | <p>Valor predeterminado:</p> | <p>""</p> | | <p>Escriba:</p> | <p>Cadena</p> | | <p>Intervalo válido:</p> | <p>De 0 a 259 caracteres</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



*JET_paramNoInformationEvent*  
50  

Cuando este parámetro es true, se suprimirán los mensajes del registro de eventos informativos que normalmente generaría el motor de base de datos.


| | | <p>Valor predeterminado:</p> | <p>Falso</p> | | <p>Escriba:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Ámbito:</p> | <p>Instancia</p> | | <p>Establezca después <a href="gg269354(v=exchg.10).md">de JetCreateInstance</a>:</p> | <p>Sí</p> | | <p>Establezca después <a href="gg294068(v=exchg.10).md">de JetInit</a>:</p> | <p>No</p> | | <p>Afecta al diseño físico:</p> | <p>No</p> | | <p>Afecta a la confiabilidad:</p> | <p>No</p> | | <p>Afecta al rendimiento:</p> | <p>No</p> | | <p>Afecta a los recursos:</p> | <p>No</p> | | <p>Disponibilidad:</p> | <p>Todo</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | | <p><strong>Header</strong></p> | <p>Declarado en Esent.h.</p> | 



### <a name="see-also"></a>Consulte también

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
