---
title: Novedades (Windows de eventos)
description: En esta página se resumen las nuevas características que se agregaron a la API Windows event log para cada versión.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f80af15d6f8b6d95533fff296ee22ea3c82d2add5f21964a7863ac3d676f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904125"
---
# <a name="whats-new-windows-event-log"></a>Novedades (Windows de eventos)

En esta página se resumen las nuevas características que se agregaron a la API Windows event log para cada versión.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

Estos son los cambios realizados en el esquema [EventManifest:](eventmanifestschema-schema.md)

-   Se ha quitado [**el tipo complejo TaskEventDefinitionType.**](eventmanifestschema-taskeventdefinitiontype-complextype.md) Para proporcionar la misma funcionalidad, use códigos de operación específicos de la tarea (vea el **elemento opcodes** del [**tipo complejo TaskType.**](eventmanifestschema-tasktype-complextype.md)
-   Se han agregado los [**tipos simples CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**filePath**](eventmanifestschema-filepath-simpletype.md)y [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) para restringir los valores asignados a los atributos de estos tipos.
-   Se ha agregado **el atributo filters** al tipo complejo [**ProviderType.**](eventmanifestschema-providertype-complextype.md) Los proveedores pueden usar filtros de la misma manera que los proveedores usan el nivel y las palabras clave para determinar si deben escribir un evento.
-   Se han agregado los siguientes tipos de salida que puede especificar para los elementos de datos definidos en una plantilla de datos de eventos:
    -   win:DateTimeCultureInsensitive
    -   win:HResult
    -   win:NTSTATUS
-   Ahora se respetan los tipos de salida, mientras que antes se omitían.

Se realizaron los siguientes cambios [](message-compiler--mc-exe-.md) en la versión del compilador de mensajes que se incluye con la versión Windows 7 del SDK de Windows:

-   Se han agregado argumentos para que el compilador genere código de registro basado en el manifiesto. También puede solicitar que el compilador genere código para registrar eventos en sistemas operativos antes de Windows Vista. Para obtener una lista de los argumentos, vea la sección "Argumentos específicos de la generación de código usado para registrar eventos" del tema [**Compilador de**](message-compiler--mc-exe-.md) mensajes.
-   El compilador ahora aplica una validación sintáctica y semántica más estricta en el manifiesto. Esto puede hacer que algunos manifiestos que se compilaron correctamente en versiones anteriores del compilador de mensajes requieran cambios para compilar correctamente con la versión más reciente.
