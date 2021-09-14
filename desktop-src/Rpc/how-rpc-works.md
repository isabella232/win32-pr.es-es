---
title: Funcionamiento de RPC
description: Las herramientas RPC hacen que parezca a los usuarios como si un cliente llamara directamente a un procedimiento ubicado en un programa de servidor remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259775"
---
# <a name="how-rpc-works"></a>Funcionamiento de RPC

Las herramientas RPC hacen que parezca a los usuarios como si un cliente llamara directamente a un procedimiento ubicado en un programa de servidor remoto. El cliente y el servidor tienen sus propios espacios de direcciones; es decir, cada uno tiene su propio recurso de memoria asignado a los datos utilizados por el procedimiento. En la ilustración siguiente se muestra la arquitectura RPC.

![arquitectura rpc](images/prog-a11.png)

Como se muestra en la ilustración, la aplicación cliente llama a un procedimiento de código auxiliar local en lugar del código real que implementa el procedimiento. Los códigos auxiliares se compilan y vinculan con la aplicación cliente. En lugar de contener el código real que implementa el procedimiento remoto, el código auxiliar del cliente:

-   Recupera los parámetros necesarios del espacio de direcciones del cliente.
-   Convierte los parámetros según sea necesario en un formato JPEG estándar para la transmisión a través de la red.
-   Llama a las funciones de la biblioteca en tiempo de ejecución del cliente RPC para enviar la solicitud y sus parámetros al servidor.

El servidor realiza los pasos siguientes para llamar al procedimiento remoto.

1.  Las funciones de la biblioteca en tiempo de ejecución RPC del servidor aceptan la solicitud y llaman al procedimiento de código auxiliar del servidor.
2.  El código auxiliar del servidor recupera los parámetros del búfer de red y los convierte del formato de transmisión de red al formato que necesita el servidor.
3.  El código auxiliar del servidor llama al procedimiento real en el servidor.

A continuación, se ejecuta el procedimiento remoto, posiblemente generando parámetros de salida y un valor devuelto. Una vez completado el procedimiento remoto, una secuencia similar de pasos devuelve los datos al cliente.

1.  El procedimiento remoto devuelve sus datos al código auxiliar del servidor.
2.  El código auxiliar del servidor convierte los parámetros de salida al formato necesario para la transmisión a través de la red y los devuelve a las funciones de la biblioteca en tiempo de ejecución de RPC.
3.  Las funciones de la biblioteca en tiempo de ejecución RPC del servidor transmiten los datos de la red al equipo cliente.

El cliente completa el proceso aceptando los datos a través de la red y devolviendo los datos a la función que realiza la llamada.

1.  La biblioteca en tiempo de ejecución rpc del cliente recibe los valores devueltos del procedimiento remoto y los devuelve al código auxiliar del cliente.
2.  El código auxiliar de cliente convierte los datos de su CONVERT al formato utilizado por el equipo cliente. El código auxiliar escribe datos en la memoria del cliente y devuelve el resultado al programa que realiza la llamada en el cliente.
3.  El procedimiento de llamada continúa como si se hubiera llamado al procedimiento en el mismo equipo.

Las bibliotecas en tiempo de ejecución se proporcionan en dos partes: una biblioteca de importación, que está vinculada a la aplicación y la biblioteca en tiempo de ejecución rpc, que se implementa como una biblioteca de vínculos dinámicos (DLL).

La aplicación de servidor contiene llamadas a las funciones de biblioteca en tiempo de ejecución del servidor que registran la interfaz del servidor y permiten al servidor aceptar llamadas a procedimiento remoto. La aplicación de servidor también contiene los procedimientos remotos específicos de la aplicación a los que llaman las aplicaciones cliente.

 

 




