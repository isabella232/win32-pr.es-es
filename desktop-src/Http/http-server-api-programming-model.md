---
title: Modelo de programación
description: El modelo de programación de la API del servidor HTTP incluye cinco grupos de actividades.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def54ac8a34d6c53ea4e2825ef39884f0141df99
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104571312"
---
# <a name="programming-model"></a>Modelo de programación

El modelo de programación de la API del servidor HTTP incluye cinco grupos de actividades:

-   [Configuración](setup-configuration.md)
-   [Configuración del entorno en tiempo de ejecución](run-time-configuration.md)
-   [Crear y enlazar a una cola de solicitudes](creating-and-binding-to-a-request-queue.md)
-   [Procesamiento de solicitudes](processing-requests.md)
-   [Apagado y limpieza](shutdown-and-cleanup.md)

![Diagrama que muestra el modelo de programación de H T t P A P I.](images/http-server-api-programming-model.png)

Para obtener una aplicación de ejemplo que muestra cómo administrar las acciones de solicitud GET y POST de HTTP y cómo enviar un error 503 (**no \_ implementado**) si las acciones están presentes en la solicitud que la aplicación no controla, vea [aplicación de ejemplo de servidor http](http-server-sample-application.md).

 

 




