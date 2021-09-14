---
description: Use las siguientes directrices para crear una instalación Windows Installer que muestra un cuadro de mensaje en el que se solicita al usuario que inserte un disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Creación de mensajes de solicitud de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159048"
---
# <a name="authoring-disk-prompt-messages"></a>Creación de mensajes de solicitud de disco

Use las siguientes directrices para crear una instalación Windows Installer que muestra un cuadro de mensaje en el que se solicita al usuario que inserte un disco.

**Para mostrar un cuadro de mensaje en el que se solicita al usuario que inserte un disco**

1.  Use las funcionalidades de creación del instalador para establecer la cadena [**de propiedad DiskPrompt**](diskprompt.md) en la [tabla Property.](property-table.md) Debe incluir el nombre del producto que se va a instalar y un parámetro de marcador de posición dentro de la cadena del título impreso en el disco. Por ejemplo, Microsoft Publisher propiedad **DiskPrompt** podría ser "Microsoft Publisher: Disco \[ 1", donde 1 es el marcador de posición para el título \] del \[ \] disco.
2.  Escriba los títulos de cada uno de los discos que se solicitan en filas independientes de la columna DiskPrompt de la [tabla Media.](media-table.md) Por ejemplo, la primera y única entrada de la tabla Media podría ser "1–Install".
3.  Durante la [acción InstallFiles,](installfiles-action.md) el valor de la columna DiskPrompt de la tabla [Media](media-table.md) se sustituye por el marcador de posición en la cadena de la [**propiedad DiskPrompt.**](diskprompt.md)
4.  El mensaje que muestra el cuadro de mensaje se crea a partir de una cadena de plantilla integrada en la [tabla Error](error-table.md). Este es el error 1302 y la cadena de plantilla es: "Inserte el disco: 2", y el 2 representa un marcador de posición para la \[ \] propiedad \[ \] [**DiskPrompt.**](diskprompt.md)

En el ejemplo se muestra el siguiente mensaje al usuario: "Inserte el disco: Microsoft Publisher: Disco 1 – Instalar".

Tenga en cuenta que todos los niveles de Interfaz de usuario, excepto Ninguno, muestran los mensajes [de](user-interface-levels.md) solicitud de disco.

 

 



