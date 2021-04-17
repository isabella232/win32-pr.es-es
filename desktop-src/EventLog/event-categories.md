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
# <a name="event-categories"></a><span data-ttu-id="e56ed-104">Categorías de eventos</span><span class="sxs-lookup"><span data-stu-id="e56ed-104">Event Categories</span></span>

<span data-ttu-id="e56ed-105">Las categorías ayudan a organizar los eventos para que Visor de eventos puedan filtrarlos.</span><span class="sxs-lookup"><span data-stu-id="e56ed-105">Categories help you organize events so Event Viewer can filter them.</span></span> <span data-ttu-id="e56ed-106">Cada [origen de eventos](event-sources.md) puede definir sus propias categorías numeradas y las cadenas de texto a las que se asignan.</span><span class="sxs-lookup"><span data-stu-id="e56ed-106">Each [event source](event-sources.md) can define its own numbered categories and the text strings to which they are mapped.</span></span>

<span data-ttu-id="e56ed-107">Las categorías se deben numerar consecutivamente, empezando por el número 1.</span><span class="sxs-lookup"><span data-stu-id="e56ed-107">The categories must be numbered consecutively, beginning with the number 1.</span></span> <span data-ttu-id="e56ed-108">Las categorías se definen en un archivo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e56ed-108">The categories themselves are defined in a message file.</span></span> <span data-ttu-id="e56ed-109">Por ejemplo, use la siguiente sintaxis para declarar tres categorías de eventos.</span><span class="sxs-lookup"><span data-stu-id="e56ed-109">For example, use the following syntax to declare three event categories.</span></span> <span data-ttu-id="e56ed-110">En Visor de eventos, los eventos que usan estas categorías tendrán la categoría 1, la categoría 2 o la categoría 3 en la columna **categoría** .</span><span class="sxs-lookup"><span data-stu-id="e56ed-110">In Event Viewer, the events that use these categories will have Category 1, Category 2, or Category 3 displayed in the **Category** column.</span></span>

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

<span data-ttu-id="e56ed-111">Las categorías se pueden almacenar en un archivo de mensaje independiente o en un archivo que contiene mensajes de otros tipos.</span><span class="sxs-lookup"><span data-stu-id="e56ed-111">Categories can be stored in a separate message file, or in a file that contains messages of other types.</span></span> <span data-ttu-id="e56ed-112">Si crea un solo archivo de mensaje, asegúrese de que las categorías son los primeros mensajes del archivo.</span><span class="sxs-lookup"><span data-stu-id="e56ed-112">If you create a single message file, be sure that the categories are the first messages in the file.</span></span> <span data-ttu-id="e56ed-113">Para obtener más información sobre la creación y el uso de archivos de mensajes, consulte [archivos de mensajes](message-files.md).</span><span class="sxs-lookup"><span data-stu-id="e56ed-113">For more information on creating and using message files, see [Message Files](message-files.md).</span></span>

<span data-ttu-id="e56ed-114">El número total de categorías se almacena en el valor **CategoryCount** para el origen del evento.</span><span class="sxs-lookup"><span data-stu-id="e56ed-114">The total number of categories is stored in the **CategoryCount** value for the event source.</span></span>

 

 



