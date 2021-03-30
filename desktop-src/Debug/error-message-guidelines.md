---
description: Las instrucciones de este tema están destinadas a ayudarle a escribir mensajes de error claros que son fáciles de localizar y útiles para los clientes.
ms.assetid: 361833e4-b94f-4ef9-a8f5-adf543534a67
title: Instrucciones de mensajes de error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1787eabd43d660322577ac766880d76854c574e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806950"
---
# <a name="error-message-guidelines"></a>Instrucciones de mensajes de error

Un mensaje de error es el texto que se muestra para describir un problema que se ha producido y que impide que el usuario o el sistema complete una tarea. El problema podría provocar daños en los datos o perderlos. Otros tipos de mensajes incluyen las confirmaciones, las advertencias y las notificaciones. Las instrucciones de este tema están destinadas a ayudarle a escribir mensajes de error claros que son fáciles de localizar y útiles para los clientes.

Los mensajes de error mal escritos pueden ser una fuente de frustración para los usuarios y pueden aumentar los costos de soporte técnico. Un mensaje de error bien escrito proporciona la siguiente información al usuario:

-   ¿Qué sucedió y por qué?
-   ¿Cuál es el resultado final del usuario?
-   ¿Qué puede hacer el usuario para evitar que vuelva a ocurrir?

La longitud del texto no es un problema, siempre que el desarrollador controle correctamente los tamaños de búfer. Es importante que el usuario tenga toda la información necesaria para resolver el problema. Si un mensaje tiene varias audiencias, es posible que deba proporcionar texto independiente para los administradores, los usuarios finales y los desarrolladores.

## <a name="best-practices"></a>Prácticas recomendadas

Las siguientes son formas de mejorar los mensajes de error:

-   Evite las condiciones de error. Si puede predecir que se producirá un error cuando un usuario realice una acción específica, vuelva a escribir el código para que el usuario no pueda producir el error.
-   Escriba un mensaje de error independiente para cada causa conocida del error. No use un único mensaje genérico para explicar cada posible motivo del error, a menos que no pueda determinar la causa del error cuando se produce.
-   Indique claramente el problema y, si es útil para el usuario, explique la causa del problema. Siempre que sea posible, reemplace los mensajes genéricos de los recursos de tabla de mensajes del sistema por un mensaje detallado específico del problema.
-   Proporcione al usuario una solución al problema. Si la solución tiene más de un paso, consulte un tema de ayuda en el que se explica detalladamente la tarea.
-   Mostrar solo el nombre del producto, componente o asistente en la barra de título del mensaje. Esto ayuda al usuario a determinar dónde está el problema. No resuma el problema en la barra de título o incluya la palabra "error".
-   No use una jerga técnica y use la terminología que entienda su audiencia. No use jergas o abreviaturas.
-   Use los botones de comando adecuados, como aceptar, cancelar, sí, no y reintentar. Puede usar combinaciones de estos botones. Los botones sí y no deben usarse siempre en combinación y siempre deben ir precedidos de una pregunta.
    -   Para detener una operación y cerrar el cuadro de mensaje, use el botón **Cancelar** .
    -   Para cerrar un cuadro de mensaje, use el botón **cerrar** .
    -   Para proporcionar más información acerca de la causa del error, use el botón **detalles** .
    -   Para proporcionar más información sobre la solución al problema, use el botón **ayuda** .
    -   Si se incluye una acción del usuario en el mensaje, use el botón **Aceptar** para cerrar el cuadro de mensaje.
    -   Los botones **sí** y **no** deben usarse en combinación y siempre deben ir precedidos de una pregunta.
-   Si el error es crítico, escríbalo en el registro de [eventos](../eventlog/event-logging.md).

## <a name="style-considerations"></a>Consideraciones de estilo

-   Use oraciones completas pero simples.
-   Utilice el tiempo actual para describir las condiciones que causaron el problema o un estado que todavía existe. Puede usar el último pasado para describir un evento distinto que se produjo en el pasado.
-   Use la voz activa siempre que sea posible. Puede utilizar la voz pasiva para describir la condición de error.
-   Evite el texto en mayúsculas y los signos de exclamación.
-   No haga que el usuario se sienta en un error, incluso si el problema se debe a un error del usuario.
-   No anthropomorphize. No implique que los programas o el hardware puedan pensar o sentirse.
-   No use palabras o frases uso coloquial. No utilice términos que puedan ser ofensivos en determinadas referencias culturales.
-   No se compone de varios nombres sin agregar una preposición o una subcláusula para aclarar el significado. Por ejemplo, "servidor del directorio de servicio LDAP del servidor de sitio" debe cambiarse a "servidor de directorio para el servicio LDAP del servidor de sitio".
-   Inserte descriptores antes de un término para aclarar el significado de la frase. Por ejemplo, "especifique InfID cuando detect está establecido en no". se debe cambiar a "especifique el parámetro InfID cuando la opción de detección esté establecida en no".
-   Evite la palabra "Bad". Use términos más descriptivos para indicar al usuario lo que es incorrecto. Por ejemplo, evite mensajes como "tamaño incorrecto". En su lugar, indique al usuario qué criterios usar al especificar un tamaño.
-   Evite la palabra "por". Se puede interpretar para indicar que una acción necesaria es opcional.
-   Coloque palabras que estén en el índice y que sean relevantes para el significado central al principio de la cadena de mensaje.

 

 
