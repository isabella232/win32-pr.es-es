---
title: Tutorial
description: Este tutorial le guía por los pasos necesarios para crear una aplicación distribuida de un solo servidor de un solo cliente sencilla a partir de una aplicación independiente existente.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- Llamada a procedimiento remoto RPC , tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd7259e5f5f0b9d0d273ff99a7cd5b42d15d57beaa60300fadecb7045a96876
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011183"
---
# <a name="tutorial"></a>Tutorial

Este tutorial le guía por los pasos necesarios para crear una aplicación distribuida de un solo servidor de un solo cliente sencilla a partir de una aplicación independiente existente. Los pasos son los siguientes:

-   Cree archivos de definición de interfaz y de configuración de la aplicación.
-   Use el compilador MIDL para generar encabezados y códigos auxiliares de cliente y servidor en lenguaje C a partir de esos archivos.
-   Escriba una aplicación cliente que administre su conexión con el servidor.
-   Escriba una aplicación de servidor que contenga los procedimientos remotos reales.
-   Compile y vincule estos archivos a la biblioteca en tiempo de ejecución rpc para generar la aplicación distribuida.

La aplicación cliente pasa una cadena de caracteres al servidor en una llamada a procedimiento remoto y el servidor imprime la cadena "Hello, World" en su salida estándar.

Los archivos de código fuente completos de esta aplicación de ejemplo, con código adicional para controlar la entrada de la línea de comandos y para enviar varios mensajes de estado al usuario, se encuentran en el directorio RPC Hello del Kit de desarrollo de \\ software de plataforma (SDK).

En esta sección se presenta su explicación en los temas siguientes:

-   [La aplicación independiente](the-standalone-application.md)
-   [Definir la interfaz](defining-the-interface.md)
-   [Generación del UUID](generating-the-uuid.md)
-   [El archivo IDL](the-idl-file.md)
-   [El archivo ACF](the-acf-file.md)
-   [Generar los archivos de código auxiliar](generating-the-stub-files.md)
-   [La aplicación cliente](the-client-application.md)
-   [La aplicación de servidor](the-server-application.md)
-   [Detención de la aplicación de servidor](stopping-the-server-application.md)
-   [Compilación y vinculación](compiling-and-linking.md)
-   [Ejecución de la aplicación](running-the-application.md)

 

 




