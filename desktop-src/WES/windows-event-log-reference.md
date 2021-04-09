---
title: Referencia del registro de eventos de Windows
description: A continuación se muestran los elementos de programación que se usan para crear un manifiesto de instrumentación, crear recursos a partir del manifiesto que utiliza el proveedor, obtener metadatos de instrumentación en tiempo de ejecución y consultar eventos de canales y archivos de registro.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fef1af82cdab1ab92b4ea4768479541053fe65d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080129"
---
# <a name="windows-event-log-reference"></a><span data-ttu-id="480d2-103">Referencia del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-103">Windows Event Log Reference</span></span>

<span data-ttu-id="480d2-104">A continuación se muestran los elementos de programación que se usan para crear un manifiesto de instrumentación, crear recursos a partir del manifiesto que utiliza el proveedor, obtener metadatos de instrumentación en tiempo de ejecución y consultar eventos de los canales y archivos de registro:</span><span class="sxs-lookup"><span data-stu-id="480d2-104">The following are the programming elements that you use to create an instrumentation manifest, create resources from the manifest that your provider uses, get instrumentation metadata at run time, and query events from channels and log files:</span></span>

-   [<span data-ttu-id="480d2-105">Esquema EventManifest</span><span class="sxs-lookup"><span data-stu-id="480d2-105">EventManifest Schema</span></span>](eventmanifestschema-schema.md)
-   [<span data-ttu-id="480d2-106">Esquema de eventos</span><span class="sxs-lookup"><span data-stu-id="480d2-106">Event Schema</span></span>](eventschema-schema.md)
-   [<span data-ttu-id="480d2-107">Esquema de consulta</span><span class="sxs-lookup"><span data-stu-id="480d2-107">Query Schema</span></span>](queryschema-schema.md)
-   [<span data-ttu-id="480d2-108">Constantes del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-108">Windows Event Log Constants</span></span>](windows-event-log-constants.md)
-   [<span data-ttu-id="480d2-109">Tipos de datos del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-109">Windows Event Log Data Types</span></span>](windows-event-log-data-types.md)
-   [<span data-ttu-id="480d2-110">Enumeraciones de registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-110">Windows Event Log Enumerations</span></span>](windows-event-log-enumerations.md)
-   [<span data-ttu-id="480d2-111">Funciones de registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-111">Windows Event Log Functions</span></span>](windows-event-log-functions.md)
-   [<span data-ttu-id="480d2-112">Estructuras de registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-112">Windows Event Log Structures</span></span>](windows-event-log-structures.md)
-   [<span data-ttu-id="480d2-113">Herramientas del registro de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="480d2-113">Windows Event Log Tools</span></span>](windows-event-log-tools.md)

<span data-ttu-id="480d2-114">En el caso de las aplicaciones escritas con un lenguaje .NET, como C# o Visual Basic, vea los siguientes espacios de nombres:</span><span class="sxs-lookup"><span data-stu-id="480d2-114">For applications written using a .NET language, such as C# or Visual Basic, see the following namespaces:</span></span>

-   <span data-ttu-id="480d2-115">Para escribir eventos, utilice las clases y los métodos definidos en el espacio de nombres [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .</span><span class="sxs-lookup"><span data-stu-id="480d2-115">To write events, use the classes and methods defined in the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace.</span></span>
-   <span data-ttu-id="480d2-116">Para consumir eventos de un canal o registro de registro de eventos de Windows, use las clases y los métodos definidos en el espacio de nombres [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .</span><span class="sxs-lookup"><span data-stu-id="480d2-116">To consume events from a Windows Event Log channel or log, use the classes and methods defined in the [System.Diagnostics.Eventing.Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.</span></span>

<span data-ttu-id="480d2-117">Como alternativa al uso del espacio de nombres [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) para escribir eventos, puede usar el argumento **-CS** o **-CSS** para que el compilador de mensajes genere el código para escribir los eventos.</span><span class="sxs-lookup"><span data-stu-id="480d2-117">As an alternative to using the [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) namespace to write events, you can use the **-cs** or **-css** argument to have the message compiler generate the code to write the events.</span></span> <span data-ttu-id="480d2-118">Para obtener más información, vea [**compilador de mensajes**](message-compiler--mc-exe-.md).</span><span class="sxs-lookup"><span data-stu-id="480d2-118">For details, see [**Message Compiler**](message-compiler--mc-exe-.md).</span></span>
