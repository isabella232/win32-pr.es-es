---
description: Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador utiliza un conjunto de entrega solo cuando el analizador puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Especificar un conjunto de entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686996"
---
# <a name="specifying-a-handoff-set"></a>Especificar un conjunto de entrega

Un conjunto de entrega especifica los protocolos que siguen a un protocolo. El analizador utiliza un conjunto de entrega solo cuando el analizador puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.

Por ejemplo, el protocolo TCP tiene una propiedad de puerto que identifica el protocolo que sigue al protocolo TCP. Un valor de propiedad de 20 indica que el protocolo siguiente es FTP. Un valor de propiedad de 53 indica que el protocolo siguiente es DNS. Dado que la propiedad Port identifica el protocolo que se muestra a continuación, el analizador de TCP puede utilizar el conjunto de entrega siguiente para obtener un identificador para el protocolo que especifica la propiedad Port.

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

Los conjuntos de entrega se almacenan en el archivo INI del analizador. Por ejemplo, el conjunto de entrega TCP anterior se encuentra en tcpip.ini archivo. Tenga en cuenta que si un archivo DLL de analizador admite varios protocolos, cada analizador que use un conjunto de entrega tendrá su propia ubicación en el archivo INI.

La información del conjunto de entrega se especifica durante la implementación de la función [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . El analizador puede especificar los protocolos que preceden al protocolo del analizador y los protocolos que siguen el protocolo del analizador. Monitor de red toma todos los protocolos que preceden y agrega el protocolo del analizador a las siguientes secciones Set del archivo INI del analizador, para cada protocolo anterior. Monitor de red almacena la lista de protocolos que se indican a continuación en la sección conjunto de entrega del archivo INI del analizador.

Monitor de red almacena la información del conjunto de entrega en el archivo INI del analizador, pero el analizador no accede a los archivos INI directamente. Para usar la información del conjunto de entrega, el analizador llama a la función [**CreateHandoffTable**](createhandofftable.md) para crear una tabla de entrega. Normalmente, la tabla de entrega se crea cuando el analizador registra el protocolo. Una vez registrado el protocolo, Monitor de red crea una tabla de conjunto de entrega que puede usar el analizador.

El analizador utiliza su conjunto de entrega al reconocer los datos. En primer lugar, el analizador lee el valor de la propiedad que identifica el protocolo siguiente. A continuación, el analizador llama a [**GetProtocolFromTable**](getprotocolfromtable.md) para obtener un identificador al siguiente protocolo. Por último, el analizador devuelve un puntero al identificador en el parámetro *phNextProtocol* de [**RecognizeFrame**](recognizeframe.md).

 

 



