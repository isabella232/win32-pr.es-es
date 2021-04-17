---
description: Las categorías ayudan a organizar los eventos para que Visor de eventos puedan filtrarlos. Cada origen de eventos puede definir sus propias categorías numeradas y las cadenas de texto a las que se asignan.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorías de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd84a095754bd51499edf5a21ebea0ade042d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687050"
---
# <a name="event-categories"></a>Categorías de eventos

Las categorías ayudan a organizar los eventos para que Visor de eventos puedan filtrarlos. Cada [origen de eventos](event-sources.md) puede definir sus propias categorías numeradas y las cadenas de texto a las que se asignan.

Las categorías se deben numerar consecutivamente, empezando por el número 1. Las categorías se definen en un archivo de mensaje. Por ejemplo, use la siguiente sintaxis para declarar tres categorías de eventos. En Visor de eventos, los eventos que usan estas categorías tendrán la categoría 1, la categoría 2 o la categoría 3 en la columna **categoría** .

``` syntax
MessageId=0x1
SymbolicName=CATEGORY_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CATEGORY_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CATEGORY_3
Language=English
Category 3
.
```

Las categorías se pueden almacenar en un archivo de mensaje independiente o en un archivo que contiene mensajes de otros tipos. Si crea un solo archivo de mensaje, asegúrese de que las categorías son los primeros mensajes del archivo. Para obtener más información sobre la creación y el uso de archivos de mensajes, consulte [archivos de mensajes](message-files.md).

El número total de categorías se almacena en el valor **CategoryCount** para el origen del evento.

 

 



