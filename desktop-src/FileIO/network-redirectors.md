---
description: Describe la funcionalidad de un redirector de red.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Redirectors de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069895"
---
# <a name="network-redirectors"></a>Redirectors de red

Un redirector de red es un controlador del sistema de archivos (o FSD) que funciona de la siguiente manera:

-   Como cliente en una operación de E/S de red mediante el envío de solicitudes de E/S a los servidores y el procesamiento de las respuestas de los servidores.
-   Como servidor en una operación de E/S de red mediante la recepción de solicitudes de E/S de los servidores y el procesamiento de las solicitudes.

Realiza toda la interacción de bajo nivel con el servidor para resolver el nombre de archivo proporcionado por la aplicación con la ubicación del recurso en el servidor remoto. De esta manera, el redirector permite que la aplicación acceda y manipule recursos en servidores remotos como si estuvieran ubicados en el equipo local.

Los redirectors funcionan completamente en modo kernel. Esto proporciona las siguientes ventajas de rendimiento con respecto a las alternativas del modo de usuario:

-   Puede interactuar con los FSD en modo kernel que se ejecutan en el servidor, como el FSD del servidor, sin necesidad de cambiar el modo de usuario a kernel y el modo kernel a usuario.
-   Puede interactuar en modo kernel con el administrador de caché en el servidor para almacenar en caché los datos de E/S que el administrador de caché del servidor envía en el cliente.
-   Las funciones de API personalizadas para las solicitudes de E/S remotas y los cambios en las funciones de E/S de archivo estándar para proporcionar esta funcionalidad no son necesarios.

 

 



