---
title: Tutorial
description: Este tutorial le guiará por los pasos necesarios para crear una aplicación distribuida simple de un solo cliente y de un solo servidor a partir de una aplicación independiente existente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- RPC llamada a procedimiento remoto, tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076087"
---
# <a name="tutorial"></a>Tutorial

Este tutorial le guiará por los pasos necesarios para crear una aplicación distribuida simple de un solo cliente y de un solo servidor a partir de una aplicación independiente existente. Los pasos son los siguientes:

-   Crear definición de interfaz y archivos de configuración de la aplicación.
-   Utilice el compilador MIDL para generar el código auxiliar y los encabezados de cliente y servidor de lenguaje C a partir de esos archivos.
-   Escriba una aplicación cliente que administre su conexión con el servidor de.
-   Escriba una aplicación de servidor que contenga los procedimientos remotos reales.
-   Compile y vincule estos archivos a la biblioteca en tiempo de ejecución de RPC para generar la aplicación distribuida.

La aplicación cliente pasa una cadena de caracteres al servidor en una llamada a procedimiento remoto y el servidor imprime la cadena "Hello, World" en la salida estándar.

Los archivos de código fuente completos para esta aplicación de ejemplo, con código adicional para controlar la entrada de la línea de comandos y enviar varios mensajes de estado al usuario, se encuentran en el \\ Directorio de RPC Hola del kit de desarrollo de software (SDK) de la plataforma.

En esta sección se presenta su debate en los temas siguientes:

-   [Aplicación independiente](the-standalone-application.md)
-   [Definir la interfaz](defining-the-interface.md)
-   [Generar el UUID](generating-the-uuid.md)
-   [El archivo IDL](the-idl-file.md)
-   [El archivo ACF](the-acf-file.md)
-   [Generar archivos de código auxiliar](generating-the-stub-files.md)
-   [La aplicación cliente](the-client-application.md)
-   [La aplicación de servidor](the-server-application.md)
-   [Detener la aplicación de servidor](stopping-the-server-application.md)
-   [Compilar y vincular](compiling-and-linking.md)
-   [Ejecutar la aplicación](running-the-application.md)

 

 




