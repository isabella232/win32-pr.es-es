---
description: Necesidades de rendimiento de usuarios y administradores con Windows sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Necesidades de rendimiento: Usuarios y administradores'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c74f4ec6f0a545a98a890f0bc8ff954fe43a3f79fc04fd2c2d92e68ea9f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097675"
---
# <a name="performance-needs-users-and-administrators"></a>Necesidades de rendimiento: Usuarios y administradores

Los usuarios juzguen el rendimiento de las aplicaciones por su experiencia:

-   ¿La aplicación responde rápidamente?
-   ¿Se muestra un icono de reloj de reloj mientras se realizan operaciones en segundo plano?
-   ¿La aplicación se inicia y se cierra rápidamente?
-   ¿Se controlan los errores de una manera comprensible?

En resumen, los usuarios quieren que las aplicaciones sean rápidas y predecibles.

Por el contrario, los administradores suelen tener en cuenta el rendimiento de una aplicación en cuanto a la eficacia con la que usa los recursos de red. Los administradores pueden preguntar:

-   ¿La aplicación tiene una sobrecarga baja y un uso eficaz de la red?
-   ¿Es el número mínimo de conexiones usadas, por lo que mi servidor puede usar tantos usuarios a la vez como sea posible?
-   ¿Estoy llamando constantemente al departamento de soporte técnico?

En resumen, los administradores quieren que las aplicaciones se escalen.

## <a name="best-practices-for-performance-needs"></a>Procedimientos recomendados para las necesidades de rendimiento

Al desarrollar una aplicación Windows Sockets, estos requisitos de rendimiento se traducen en reglas útiles.

-   Hacer que las aplicaciones de red se inicialicen rápidamente.

    La interfaz de usuario no debe tener que esperar respuestas de red. Algunas tareas se pueden realizar antes de que la red esté disponible o sin la red. Si la red no responde, es posible que el usuario necesite la interfaz de usuario para operaciones sencillas, como cerrar la aplicación.

-   No espere a que la red se apague.

    Las aplicaciones cliente-servidor correctamente escritas controlan correctamente las desconexiones abortivas. No inicie una operación potencialmente larga, como sincronizar archivos o carpetas con un servidor, que no se pueda interrumpir al apagar. Las redes no responden de forma coherente, por lo que incluso las operaciones pequeñas podrían llevar mucho tiempo. Proporcionar comentarios positivos para los usuarios, incluidas las indicaciones de progreso y los tiempos de finalización estimados.

-   Asegúrese de una interfaz de usuario con capacidad de respuesta.

    La capacidad de respuesta de la aplicación ayuda a eliminar llamadas innecesarias al departamento de soporte técnico. Una buena guía para la respuesta interactiva es de 500 milisegundos. Los usuarios perciben pausas superiores a 500 milisegundos como un retraso en el rendimiento. Las aplicaciones deben tener la capacidad de respuesta suficiente para proporcionar al usuario confianza sobre la aplicación.

-   Examinar los errores de red.

    No todos los errores de red son críticos. Por ejemplo, una aplicación que ha recibido o publicado todos sus datos probablemente puede omitir los errores al cerrar la conexión. No suponga que la red o el usuario están disponibles; controlar los errores sin intervención del usuario o omitirlos si los errores no son críticos.

-   Una aplicación debe definir sus propios tiempos de espera razonables.

    Por ejemplo, una solicitud Windows Sockets connect() puede bloquearse en algunas condiciones durante hasta 21 segundos. Es posible que las aplicaciones deban introducir sus propios tiempos de espera según corresponda para sus usuarios.

-   Minimice la sobrecarga del protocolo.

    La conservación del ancho de banda de red se trata parcialmente de minimizar la sobrecarga de protocolo en la que incurre la aplicación. También se trata de eliminar el tráfico de red innecesario. Los protocolos con una sobrecarga de encabezado inferior se pueden usar para transferir datos de la aplicación. Por ejemplo, al enviar cantidades más pequeñas de datos no críticos o repetibles, use UDP en lugar de TCP para reducir la sobrecarga asociada con el establecimiento y el mantenimiento de la conexión. Si los mismos datos deben enviarse a varios destinatarios, considere la posibilidad de multidifusión. Tenga en cuenta que las aplicaciones UDP no están controladas por el flujo, ya que insertar más allá del ancho de banda disponible puede provocar un error de red catastrófico. La utilidad Netstat se puede usar con sus **opciones -e** **y -s** para mostrar estadísticas para varios protocolos.

-   Conserve los recursos del sistema.

    Los recursos del sistema se pueden consumir rápidamente si no se usa la restricción adecuada. Por ejemplo, los sockets y las conexiones TCP consumen recursos. No use varias conexiones TCP por cliente donde una sirva para el propósito de la aplicación.

En el caso de las aplicaciones transaccionales, una buena experiencia del usuario y un uso reducido de la red no son objetivos en conflicto. La red es un cuello de botella. Las aplicaciones de uso intensivo de red dedican más tiempo a esperar y las aplicaciones de red bien escritas están diseñadas para minimizar el tiempo de espera innecesario, tanto para la interfaz de usuario como para las transmisiones de red.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de sockets Windows alto rendimiento](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensiones de rendimiento](performance-dimensions-2.md)
</dt> </dl>

 

 



