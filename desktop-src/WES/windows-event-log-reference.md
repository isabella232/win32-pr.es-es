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
# <a name="windows-event-log-reference"></a>Referencia del registro de eventos de Windows

A continuación se muestran los elementos de programación que se usan para crear un manifiesto de instrumentación, crear recursos a partir del manifiesto que utiliza el proveedor, obtener metadatos de instrumentación en tiempo de ejecución y consultar eventos de los canales y archivos de registro:

-   [Esquema EventManifest](eventmanifestschema-schema.md)
-   [Esquema de eventos](eventschema-schema.md)
-   [Esquema de consulta](queryschema-schema.md)
-   [Constantes del registro de eventos de Windows](windows-event-log-constants.md)
-   [Tipos de datos del registro de eventos de Windows](windows-event-log-data-types.md)
-   [Enumeraciones de registro de eventos de Windows](windows-event-log-enumerations.md)
-   [Funciones de registro de eventos de Windows](windows-event-log-functions.md)
-   [Estructuras de registro de eventos de Windows](windows-event-log-structures.md)
-   [Herramientas del registro de eventos de Windows](windows-event-log-tools.md)

En el caso de las aplicaciones escritas con un lenguaje .NET, como C# o Visual Basic, vea los siguientes espacios de nombres:

-   Para escribir eventos, utilice las clases y los métodos definidos en el espacio de nombres [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) .
-   Para consumir eventos de un canal o registro de registro de eventos de Windows, use las clases y los métodos definidos en el espacio de nombres [System. Diagnostics. Eventing. Reader](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true) .

Como alternativa al uso del espacio de nombres [System. Diagnostics. Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) para escribir eventos, puede usar el argumento **-CS** o **-CSS** para que el compilador de mensajes genere el código para escribir los eventos. Para obtener más información, vea [**compilador de mensajes**](message-compiler--mc-exe-.md).
