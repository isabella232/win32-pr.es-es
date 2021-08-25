---
description: Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador usa un conjunto de entrega solo cuando el analizador puede identificar el siguiente protocolo a partir de los datos de una instancia de protocolo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Especificar un conjunto de entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f3f7d559c83e3c56bc6ea202b3a0e339dbc1b76d93fc2af1b73f5a2c60c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778355"
---
# <a name="specifying-a-handoff-set"></a>Especificar un conjunto de entrega

Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador usa un conjunto de entrega solo cuando el analizador puede identificar el siguiente protocolo a partir de los datos de una instancia de protocolo.

Por ejemplo, el protocolo TCP tiene una propiedad de puerto que identifica el protocolo que sigue al protocolo TCP. Un valor de propiedad de 20 indica que el protocolo siguiente es FTP. Un valor de propiedad de 53 indica que el protocolo siguiente es DNS. Dado que la propiedad port identifica el protocolo siguiente, el analizador TCP puede usar el siguiente conjunto de entregas para obtener un identificador para el protocolo especificado por la propiedad port.

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

Los conjuntos de entrega se almacenan en el archivo INI del analizador. Por ejemplo, el conjunto de entrega TCP anterior se encuentra en tcpip.ini archivo. Tenga en cuenta que si un archivo DLL de analizador admite varios protocolos, cada analizador que use un conjunto de entregas tiene su propia ubicación en el archivo INI.

La información del conjunto de entrega se especifica durante la implementación de la [**función ParserAutoInstallInfo.**](parserautoinstallinfo.md) El analizador puede especificar los protocolos que preceden al protocolo del analizador y los protocolos que siguen al protocolo del analizador. Monitor de red toma todos los protocolos que preceden y agrega el protocolo de analizador a las siguientes secciones de conjunto del archivo INI del analizador, para cada protocolo anterior. Monitor de red almacena la lista de protocolos siguientes en la sección de conjunto de entregas del archivo INI del analizador.

Monitor de red la información del conjunto de entregas en el archivo INI del analizador, pero el analizador no accede directamente a los archivos INI. Para usar la información del conjunto de entrega, el analizador llama a la [**función CreateHandoffTable**](createhandofftable.md) para crear una tabla de entrega. Normalmente, la tabla de entrega se crea cuando el analizador registra el protocolo. Una vez registrado el protocolo, Monitor de red una tabla de conjunto de entrega que el analizador puede usar.

El analizador usa su conjunto de entrega al reconocer datos. En primer lugar, el analizador lee el valor de la propiedad que identifica el protocolo siguiente. A continuación, el analizador llama a [**GetProtocolFromTable**](getprotocolfromtable.md) para obtener un identificador para el protocolo siguiente. Por último, el analizador devuelve un puntero al identificador del parámetro *phNextProtocol* [**de RecognizeFrame.**](recognizeframe.md)

 

 



