---
description: Las categorías le ayudan a organizar los eventos para Visor de eventos pueda filtrarlos. Cada origen de evento puede definir sus propias categorías numeradas y las cadenas de texto a las que están asignadas.
ms.assetid: ddba8066-b6b9-42a6-b49f-cbae8f97ef6d
title: Categorías de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d68895c1043e12ab8e53e3d6db8cd385d17ccc0175c5610a487682fc1c92c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151646"
---
# <a name="event-categories"></a>Categorías de eventos

Las categorías le ayudan a organizar los eventos para Visor de eventos pueda filtrarlos. Cada [origen de](event-sources.md) evento puede definir sus propias categorías numeradas y las cadenas de texto a las que están asignadas.

Las categorías se deben numerar consecutivamente, empezando por el número 1. Las propias categorías se definen en un archivo de mensaje. Por ejemplo, use la sintaxis siguiente para declarar tres categorías de eventos. En Visor de eventos, los eventos que usan estas categorías tendrán categoría 1, categoría 2 o categoría 3 en la **columna** Categoría .

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

Las categorías se pueden almacenar en un archivo de mensaje independiente o en un archivo que contenga mensajes de otros tipos. Si crea un archivo de mensaje único, asegúrese de que las categorías son los primeros mensajes del archivo. Para obtener más información sobre cómo crear y usar archivos de mensaje, vea [Archivos de mensaje](message-files.md).

El número total de categorías se almacena en el **valor CategoryCount** del origen del evento.

 

 



