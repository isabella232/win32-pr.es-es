---
title: Windows Referencia del registro de eventos
description: Estos son los elementos de programación que se usan para crear un manifiesto de instrumentación, crear recursos a partir del manifiesto que usa el proveedor, obtener metadatos de instrumentación en tiempo de ejecución y consultar eventos de canales y archivos de registro.
ms.assetid: 7af07a43-62f6-412f-9f67-46ad08922daf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6ce52f3756b8f33ac710e189677de053dc538339d0a0cdeb335410dd76a171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957795"
---
# <a name="windows-event-log-reference"></a>Windows Referencia del registro de eventos

Estos son los elementos de programación que se usan para crear un manifiesto de instrumentación, crear recursos a partir del manifiesto que usa el proveedor, obtener metadatos de instrumentación en tiempo de ejecución y consultar eventos de canales y archivos de registro:

-   [Esquema EventManifest](eventmanifestschema-schema.md)
-   [Esquema de eventos](eventschema-schema.md)
-   [Esquema de consulta](queryschema-schema.md)
-   [Windows Constantes del registro de eventos](windows-event-log-constants.md)
-   [Windows Tipos de datos del registro de eventos](windows-event-log-data-types.md)
-   [Windows Enumeraciones del registro de eventos](windows-event-log-enumerations.md)
-   [Windows Funciones del registro de eventos](windows-event-log-functions.md)
-   [Windows Estructuras del registro de eventos](windows-event-log-structures.md)
-   [Windows Herramientas del registro de eventos](windows-event-log-tools.md)

Para las aplicaciones escritas con un lenguaje .NET, como C# o Visual Basic, consulte los siguientes espacios de nombres:

-   Para escribir eventos, use las clases y métodos definidos en el espacio de nombres [System.Diagnostics.Eventing.](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8)
-   Para consumir eventos de un canal Windows registro de eventos, use las clases y métodos definidos en el espacio de nombres [System.Diagnostics.Eventing.Reader.](/dotnet/api/system.diagnostics.eventing.reader?view=dotnet-plat-ext-3.1&preserve-view=true)

Como alternativa al uso del espacio de nombres [System.Diagnostics.Eventing](/dotnet/api/system.diagnostics.eventing?view=netframework-4.8) para escribir eventos, puede usar el **argumento -cs** o **-css** para que el compilador del mensaje genere el código para escribir los eventos. Para obtener más información, vea [**Compilador de mensajes.**](message-compiler--mc-exe-.md)
