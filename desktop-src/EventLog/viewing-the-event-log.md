---
description: Cuando el usuario inicia Visor de eventos para ver las entradas del registro de eventos, llama a la función ReadEventLog para obtener las estructuras EVENTLOGRECORD.
ms.assetid: 1d5b62cb-cf5b-4f4c-8521-1c783ae3afc7
title: Ver el registro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c566fef29cfb110883741ddc0e6c298d6a1255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276375"
---
# <a name="viewing-the-event-log"></a>Ver el registro de eventos

Cuando el usuario inicia Visor de eventos para ver las entradas del registro de eventos, llama a la función [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para obtener las estructuras [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . El Visor de eventos usa el origen del evento y el identificador de evento para obtener el texto del mensaje para cada evento del archivo de mensaje registrado (indicado por el valor del registro **EventMessageFile** para el origen). El Visor de eventos utiliza la función [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) para cargar el archivo de mensaje. A continuación, el Visor de eventos utiliza la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) para recuperar la cadena de Descripción base del módulo cargado. Por último, el Visor de eventos reemplaza los parámetros de inserción en la cadena de Descripción base para producir la cadena de mensaje final.

 

 
