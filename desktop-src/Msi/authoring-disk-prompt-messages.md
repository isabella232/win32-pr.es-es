---
description: Utilice las siguientes directrices para crear una Windows Installer instalación que muestre un cuadro de mensaje que le pida al usuario que inserte un disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Creación de mensajes de solicitud de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652613"
---
# <a name="authoring-disk-prompt-messages"></a>Creación de mensajes de solicitud de disco

Utilice las siguientes directrices para crear una Windows Installer instalación que muestre un cuadro de mensaje que le pida al usuario que inserte un disco.

**Para mostrar un cuadro de mensaje que pide al usuario que inserte un disco**

1.  Use las capacidades de creación del instalador para establecer la cadena de la propiedad [**DiskPrompt**](diskprompt.md) en la tabla de [propiedades](property-table.md) . Esto debe incluir el nombre del producto que se va a instalar y un parámetro de marcador de posición dentro de la cadena para el título impreso en el disco. Por ejemplo, para Microsoft Publisher, la propiedad **DiskPrompt** podría ser "Microsoft Publisher: Disk \[ 1 \] ", donde \[ 1 \] es el marcador de posición del título del disco.
2.  Escriba los títulos de cada uno de los discos que se solicitan en filas independientes de la columna DiskPrompt de la tabla de [medios](media-table.md) . Por ejemplo, la primera y única entrada en la tabla de medios podría ser "1 – install".
3.  Durante la acción [InstallFiles](installfiles-action.md) , el valor de la columna DiskPrompt de la tabla de [medios](media-table.md) se sustituye por el marcador de posición en la cadena de la propiedad [**DiskPrompt**](diskprompt.md) .
4.  El mensaje que muestra el cuadro de mensaje se crea a partir de una cadena de plantilla integrada en la [tabla de errores](error-table.md). Se trata del error 1302 y la cadena de la plantilla es: "Inserte el disco: \[ 2 \] " y \[ 2 \] representa un marcador de posición para la propiedad [**DiskPrompt**](diskprompt.md) .

En el ejemplo se muestra el siguiente mensaje al usuario: "Inserte el disco: Microsoft Publisher: disco 1 – instalar".

Tenga en cuenta que los mensajes de petición de disco aparecen en todos los niveles de la [interfaz de usuario](user-interface-levels.md) , excepto ninguno.

 

 



