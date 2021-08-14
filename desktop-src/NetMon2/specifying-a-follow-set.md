---
description: Un conjunto de seguimiento especifica los protocolos que siguen a un protocolo. Monitor de red un conjunto de seguimiento cuando el analizador no puede identificar el siguiente protocolo a partir de los datos de una instancia de protocolo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Especificar un conjunto de seguimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b11320872cc07d69f5796e344a1d5ed4dea4594e48f9697901126d915fd7b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363051"
---
# <a name="specifying-a-follow-set"></a>Especificar un conjunto de seguimiento

Un conjunto de seguimiento especifica los protocolos que siguen a un protocolo. Monitor de red un conjunto de seguimiento cuando el analizador no puede identificar el siguiente protocolo a partir de los datos de una instancia de protocolo.

Por ejemplo, el analizador netBIOS especifica un conjunto de seguimiento porque los datos del protocolo NetBIOS no identifican qué protocolo es el siguiente. Como resultado, el analizador netBIOS debe crear un conjunto de seguimiento de todos los protocolos que pueden seguirse.

En el ejemplo de código siguiente se identifica el conjunto de seguimiento de NetBIOS [*en*](p.md)Parser.iniarchivo. El siguiente conjunto contiene los protocolos bloque de mensajes de servidor (SMB) y llamada a procedimiento remoto de Microsoft (MSRPC). Estos son los únicos protocolos que pueden seguir una instancia del protocolo NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Un analizador especifica un conjunto de seguimiento durante la implementación de la [**función ParserAutoInstallInfo.**](parserautoinstallinfo.md) Un analizador puede especificar qué protocolos preceden y qué protocolos siguen. Cuando un analizador especifica los protocolos que preceden, Monitor de red el protocolo del analizador a los siguientes conjuntos de protocolos especificados. Cuando un analizador especifica los protocolos siguientes, Monitor de red crea una nueva sección en el archivo Parser.ini que incluye el siguiente conjunto del analizador.

 

 



