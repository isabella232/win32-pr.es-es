---
description: Necesidades de rendimiento de los usuarios y administradores con aplicaciones de Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Necesidades de rendimiento: usuarios y administradores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082112"
---
# <a name="performance-needs-users-and-administrators"></a>Necesidades de rendimiento: usuarios y administradores

Los usuarios juzgan el rendimiento de la aplicación por su experiencia:

-   ¿La aplicación debe responder rápidamente?
-   ¿Se muestra un icono de reloj de arena mientras se realizan las operaciones en segundo plano?
-   ¿La aplicación se inicia y se cierra rápidamente?
-   ¿Los errores se controlan de forma comprensible?

En Resumen, los usuarios quieren que las aplicaciones sean rápidas y predecibles.

Por el contrario, los administradores suelen juzgar el rendimiento de una aplicación en la eficacia con la que usan los recursos de red. Los administradores pueden solicitar:

-   ¿La aplicación tiene poca sobrecarga y un uso eficaz de la red?
-   ¿Es el número mínimo de conexiones usadas, por lo que mi servidor puede atender tantos usuarios como sea posible?
-   ¿Estoy llamando constantemente al Departamento de soporte técnico?

En Resumen, los administradores quieren escalar las aplicaciones.

## <a name="best-practices-for-performance-needs"></a>Prácticas recomendadas para las necesidades de rendimiento

Al desarrollar una aplicación de Windows Sockets, estos requisitos de rendimiento se traducen en reglas útiles.

-   Hacer que las aplicaciones de red se inicialicen rápidamente.

    La interfaz de usuario no debe esperar las respuestas de red. Se pueden realizar algunas tareas antes de que la red esté disponible o sin la red. Si la red no responde, es posible que el usuario necesite la interfaz de usuario para operaciones sencillas, como cerrar la aplicación.

-   No espere a que se cierre la red.

    Las aplicaciones cliente y servidor escritas correctamente administran las desconexiones anuladas correctamente. No inicie una operación potencialmente larga, como la sincronización de archivos o carpetas con un servidor, que no se puede interrumpir al apagar. Las redes no responden de forma coherente, por lo que incluso las pequeñas operaciones podrían demostrar un tiempo prolongado. Proporcionar comentarios positivos para los usuarios, incluidas las indicaciones de progreso y los tiempos de finalización estimados.

-   Asegúrese de que haya una interfaz de usuario con capacidad de respuesta.

    La capacidad de respuesta de las aplicaciones ayuda a eliminar llamadas innecesarias al Departamento Una buena directriz para la respuesta interactiva es de 500 milisegundos. Los usuarios perciben pausas de más de 500 milisegundos como un retraso en el rendimiento. Las aplicaciones deben responder lo suficiente para proporcionar al usuario confianza sobre la aplicación.

-   Examine los errores de red.

    No todos los errores de red son críticos. Por ejemplo, una aplicación que ha recibido o enviado todos sus datos puede omitir los errores al cerrar la conexión. No asuma que la red o el usuario están disponibles; controla los errores sin la intervención del usuario o los omite si los errores no son críticos.

-   Una aplicación debe definir sus propios tiempos de espera razonables.

    Por ejemplo, una solicitud de Windows Sockets Connect () puede bloquearse en algunas condiciones durante un máximo de 21 segundos. Es posible que las aplicaciones necesiten introducir sus propios tiempos de espera según sea necesario para sus usuarios.

-   Minimice la sobrecarga del protocolo.

    El uso del ancho de banda de red es parcialmente mayor que la sobrecarga del protocolo que incurre en la aplicación. También se trata de la eliminación del tráfico de red innecesario. Los protocolos con una sobrecarga de encabezado inferior se pueden usar para transferir datos de aplicaciones. Por ejemplo, al enviar cantidades más pequeñas de datos no críticos o repetibles, use UDP en lugar de TCP para reducir la sobrecarga asociada con el establecimiento y el mantenimiento de la conexión. Si los mismos datos se deben enviar a varios destinatarios, tenga en cuenta la multidifusión. Tenga en cuenta que las aplicaciones UDP no están controladas por flujo. Si se inserta más allá del ancho de banda disponible, se puede producir un error catastrófico en la red. La utilidad Netstat se puede usar con las opciones **-e** y **-s** para mostrar las estadísticas de diversos protocolos.

-   Conservar recursos del sistema.

    Los recursos del sistema se pueden consumir rápidamente si no se usa la sujeción adecuada. Por ejemplo, los sockets y las conexiones TCP consumen recursos. No use varias conexiones TCP por cliente, donde una servirá para el propósito de la aplicación.

En el caso de las aplicaciones transaccionales, la buena experiencia del usuario y la utilización de poca red no son objetivos en conflicto. La red es un cuello de botella. Las aplicaciones con un uso intensivo de la red dedican más tiempo a esperar y las aplicaciones de red bien escritas están diseñadas para minimizar el tiempo de espera innecesario, tanto para la interfaz de usuario como para las transmisiones de red.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de Windows Sockets de alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensiones de rendimiento](performance-dimensions-2.md)
</dt> </dl>

 

 



