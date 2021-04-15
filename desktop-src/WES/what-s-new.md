---
title: Novedades (registro de eventos de Windows)
description: En esta página se resumen las nuevas características que se agregaron a la API del registro de eventos de Windows para cada versión.
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652d82f67292316dd7aec599955d69dd70ab39a3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695846"
---
# <a name="whats-new-windows-event-log"></a>Novedades (registro de eventos de Windows)

En esta página se resumen las nuevas características que se agregaron a la API del registro de eventos de Windows para cada versión.

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 y Windows Server 2008 R2

A continuación se muestran los cambios realizados en el esquema [EventManifest](eventmanifestschema-schema.md) :

-   Se quitó el tipo complejo de [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) . Para proporcionar la misma funcionalidad, use códigos de tiempo específicos de la tarea (vea el elemento **OpCodes** del tipo complejo [**TaskType**](eventmanifestschema-tasktype-complextype.md) .
-   Se han agregado los tipos simples [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**filePath**](eventmanifestschema-filepath-simpletype.md)y [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) para restringir los valores asignados a los atributos de estos tipos.
-   Se ha agregado el atributo **Filters** al tipo complejo de [**ProviderType**](eventmanifestschema-providertype-complextype.md) . Los proveedores pueden usar filtros de la misma manera que los proveedores usan el nivel y las palabras clave para determinar si deben escribir un evento.
-   Se han agregado los siguientes tipos de salida que se pueden especificar para los elementos de datos definidos en una plantilla de datos de eventos:
    -   Win: DateTimeCultureInsensitive
    -   Win: HResult
    -   Win: NTSTATUS
-   Ahora se respetan los tipos de salida, mientras que antes se omitieron.

Los siguientes cambios se realizaron en la versión del [**compilador de mensajes**](message-compiler--mc-exe-.md) que se incluye con la versión de Windows 7 del Windows SDK:

-   Se han agregado argumentos para que el compilador genere código de registro basado en el manifiesto. También puede solicitar que el compilador genere código para registrar los eventos en los sistemas operativos anteriores a Windows Vista. Para obtener una lista de los argumentos, vea la sección "argumentos específicos de la generación de código usado para registrar eventos" del tema del [**compilador de mensajes**](message-compiler--mc-exe-.md) .
-   El compilador ahora aplica la validación sintáctica y semántica más estricta en el manifiesto. Esto puede hacer que algunos manifiestos compilados correctamente en versiones anteriores del compilador de mensajes requieran cambios para compilar correctamente con la versión más reciente.
