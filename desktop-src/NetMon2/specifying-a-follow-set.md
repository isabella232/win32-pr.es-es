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
# <a name="specifying-a-follow-set"></a><span data-ttu-id="3b9d2-104">Especificar un conjunto de seguimiento</span><span class="sxs-lookup"><span data-stu-id="3b9d2-104">Specifying a Follow Set</span></span>

<span data-ttu-id="3b9d2-105">Un conjunto siguiente especifica los protocolos que siguen a un protocolo.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-105">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="3b9d2-106">Monitor de red usa un conjunto de seguimiento cuando el analizador no puede identificar el protocolo siguiente a partir de los datos de una instancia de protocolo.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-106">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="3b9d2-107">Por ejemplo, el analizador de NetBIOS especifica un conjunto de seguimiento, ya que los datos del protocolo NetBIOS no identifican el protocolo siguiente.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-107">For example, the NetBIOS parser specifies a follow set because the data in the NetBIOS protocol does not identify which protocol is next.</span></span> <span data-ttu-id="3b9d2-108">Como resultado, el analizador de NetBIOS debe crear un siguiente conjunto de todos los protocolos que puedan seguir.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-108">As a result the NetBIOS parser must create a follow set of all the protocols that may follow.</span></span>

<span data-ttu-id="3b9d2-109">En el ejemplo de código siguiente se identifica el conjunto de seguimiento de NetBIOS en el archivo de [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="3b9d2-109">The following code example identifies the NetBIOS follow set in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="3b9d2-110">El siguiente conjunto contiene los protocolos de bloque de mensajes del servidor (SMB) y llamada a procedimiento remoto de Microsoft (MSRPC).</span><span class="sxs-lookup"><span data-stu-id="3b9d2-110">The follow set contains server message block (SMB), and Microsoft remote procedure call (MSRPC) protocols.</span></span> <span data-ttu-id="3b9d2-111">Estos son los únicos protocolos que pueden seguir una instancia del protocolo NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-111">These are the only protocols that can follow an instance of the NetBIOS protocol.</span></span>

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

<span data-ttu-id="3b9d2-112">Un analizador especifica un conjunto de seguimiento durante la implementación de la función [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="3b9d2-112">A parser specifies a follow set during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="3b9d2-113">Un analizador puede especificar los protocolos precedidos y los protocolos siguientes.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-113">A parser can specify which protocols precede, and which protocols follow.</span></span> <span data-ttu-id="3b9d2-114">Cuando un analizador especifica los protocolos que preceden a, Monitor de red agrega el protocolo del analizador a los siguientes conjuntos de los protocolos especificados.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-114">When a parser specifies the protocols that precede, Network Monitor adds the parser protocol to the follow sets of the specified protocols.</span></span> <span data-ttu-id="3b9d2-115">Cuando un analizador especifica los protocolos siguientes, Monitor de red crea una nueva sección en el archivo de Parser.ini que incluye el siguiente conjunto de analizador.</span><span class="sxs-lookup"><span data-stu-id="3b9d2-115">When a parser specifies the protocols that follow, Network Monitor creates a new section in the Parser.ini file that includes the follow set of the parser.</span></span>

 

 



