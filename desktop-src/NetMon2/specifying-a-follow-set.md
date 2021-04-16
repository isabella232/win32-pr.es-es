---
description: Un conjunto siguiente especifica los protocolos que siguen a un protocolo. Monitor de red usa un conjunto de seguimiento cuando el analizador no puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Especificar un conjunto de seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677422"
---
# <a name="specifying-a-follow-set"></a>Especificar un conjunto de seguimiento

Un conjunto siguiente especifica los protocolos que siguen a un protocolo. Monitor de red usa un conjunto de seguimiento cuando el analizador no puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.

Por ejemplo, el analizador de NetBIOS especifica un conjunto de seguimiento, ya que los datos del protocolo NetBIOS no identifican el protocolo siguiente. Como resultado, el analizador de NetBIOS debe crear un siguiente conjunto de todos los protocolos que puedan seguir.

En el ejemplo de código siguiente se identifica el conjunto de seguimiento de NetBIOS en el archivo de [*Parser.ini*](p.md) . El siguiente conjunto contiene los protocolos de bloque de mensajes del servidor (SMB) y llamada a procedimiento remoto de Microsoft (MSRPC). Estos son los únicos protocolos que pueden seguir una instancia del protocolo NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Un analizador especifica un conjunto de seguimiento durante la implementación de la función [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . Un analizador puede especificar los protocolos precedidos y los protocolos siguientes. Cuando un analizador especifica los protocolos que preceden a, Monitor de red agrega el protocolo del analizador a los siguientes conjuntos de los protocolos especificados. Cuando un analizador especifica los protocolos siguientes, Monitor de red crea una nueva sección en el archivo de Parser.ini que incluye el siguiente conjunto de analizador.

 

 



