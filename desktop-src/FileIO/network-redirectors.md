---
description: Describe la funcionalidad de un redirector de red.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirectores de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913533"
---
# <a name="network-redirectors"></a>Redirectores de red

Un redirector de red es un controlador del sistema de archivos (o FSD) que funciona de la siguiente manera:

-   Como cliente en una operación de e/s de red mediante el envío de solicitudes de e/s a los servidores y el procesamiento de las respuestas de los servidores.
-   Como servidor en una operación de e/s de red mediante la recepción de solicitudes de e/s de los servidores y el procesamiento de las solicitudes.

Realiza toda la interacción de bajo nivel con el servidor para resolver el nombre de archivo proporcionado por la aplicación con la ubicación del recurso en el servidor remoto. De esta manera, el redirector permite a la aplicación tener acceso a los recursos de los servidores remotos y manipularlos como si se encontraran en el equipo local.

Los redirectores funcionan completamente dentro del modo kernel. Esto proporciona las siguientes ventajas de rendimiento frente a las alternativas de modo de usuario:

-   Puede interactuar con FSDs en modo kernel que se ejecuta en el servidor, como el servidor FSD, sin necesidad de los cambios de contexto del modo de usuario a kernel y del modo de kernel a usuario.
-   Puede interactuar en modo kernel con el administrador de caché en el servidor para almacenar en caché los datos de e/s que el administrador de caché del servidor envía en el cliente.
-   Las funciones de API personalizadas para las solicitudes de e/s remotas y los cambios en las funciones de e/s de archivos estándar para proporcionar esta funcionalidad no son necesarios.

 

 



