---
description: Una característica valiosa de la telefonía es el pequeño conjunto de funciones denominado Telefonía asistida.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Introducción a la telefonía asistida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86adba883e558419731405c5b1274e812816944295c5743e8a91d343b42082c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948854"
---
# <a name="assisted-telephony-overview"></a>Introducción a la telefonía asistida

Una característica valiosa de la telefonía es el pequeño conjunto de funciones denominado Telefonía asistida. La telefonía asistida está diseñada para hacer que el establecimiento de llamadas de voz y de llamadas multimedia esté disponible para cualquier aplicación, no solo las dedicadas a la funcionalidad telefónica. En otras palabras, la telefonía asistida permite a las aplicaciones realizar llamadas telefónicas sin necesidad de conocer los detalles de los servicios de la API de telefonía completa. Extiende la telefonía a aplicaciones de procesamiento de palabras, hojas de cálculo, bases de datos, administradores de información personal y otras aplicaciones que no son de telefonía.

Para obtener una lista de las funciones de telefonía asistida tapi 2.x de telefonía básica, consulte referencia de [funciones rápidas de TAPI.](./tapi-quick-function-reference.md) TAPI 3.x admite la telefonía asistida a través de la [**interfaz ITRequest.**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)

La utilidad de la telefonía asistida se puede ilustrar en el ejemplo siguiente. Una aplicación de hoja de cálculo puede incorporar funciones que marcan un número de teléfono para una llamada de voz. Siempre que la aplicación no necesite ningún control detallado de llamadas proporcionado por la API de telefonía completa, la telefonía asistida es la manera más fácil y eficaz de darle funcionalidad de telefonía.

![telefonía asistida con una aplicación de hoja de cálculo](images/assist4.png)

La telefonía asistida y la API de telefonía completa se usan e implementan de maneras diferentes, por lo que no se recomienda mezclar llamadas de función de telefonía asistida y llamadas de función de API de telefonía dentro de una sola aplicación.

## <a name="using-assisted-telephony"></a>Uso de telefonía asistida

Las aplicaciones que usan servicios de telefonía asistida solo inician solicitudes de llamada que TAPI pone temporalmente en cola. La aplicación de destinatario de la solicitud recupera estas solicitudes y las ejecuta en nombre de la aplicación de telefonía asistida. La [**función tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) solicita el establecimiento de una llamada de voz. La aplicación solicitante no controla la llamada.

TAPI permite al usuario establecer aplicaciones de destinatario de solicitudes diferentes o las mismas para cada uno de estos servicios. Una aplicación se convierte en un destinatario de la solicitud mediante el registro [**con lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), en el que se especifica **TRUE** como valor para el *parámetro bEnable*. (Si se **especifica FALSE,** se anula el registro de la aplicación como destinatario de la solicitud, lo que debe hacer cuando se haya determinado que sus tareas de destinatario han pasado por la sesión actual). La aplicación selecciona los servicios que desea controlar en el *parámetro dwRequestMode* **de lineRegisterRequestRecipient.** Un valor posible para una solicitud es LINEREQUESTMODE MAKECALL, para mostrar que la aplicación controlará \_ [**las solicitudes tapiRequestMakeCall.**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) Si varias aplicaciones se registran para los mismos servicios, se usa un esquema de prioridad para permitir al usuario seleccionar qué aplicación es la preferida para controlar las solicitudes. Este esquema de prioridad es idéntico al utilizado para la entrega de llamadas y el enrutamiento de llamadas entrantes en función de una lista de nombres de archivo en **HandoffPriorities** en el Registro.

## <a name="call-requests"></a>Solicitudes de llamada

La telefonía asistida proporciona a las aplicaciones habilitadas para telefonía un mecanismo fácil de usar para realizar llamadas telefónicas sin necesidad de que el desarrollador se convierta en un fabricante completo de telefonía.

La [**función tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) solicita una llamada de voz entre el usuario y una entidad remota especificada por su número de teléfono. La solicitud se realiza a TAPI, que la pasa a una aplicación registrada como destinatario de dichas solicitudes. Este destinatario es una aplicación de administrador de llamadas.

Una vez que la aplicación ha realizado la solicitud, la llamada se controla completamente desde la aplicación del administrador de llamadas porque las aplicaciones de telefonía asistida no pueden administrar llamadas. Dado que los aspectos más complejos de la telefonía y todas las operaciones de interfaz de usuario se controlan mediante la aplicación del administrador de llamadas, las aplicaciones habilitadas para telefonía no deben modificarse de ninguna manera sustancial. De hecho, es posible que no sea necesario modificar las aplicaciones que permiten invocar esta operación desde su lenguaje de scripts integrado.

La [**función tapiGetLocationInfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) devuelve a la aplicación el código de país o región y el código de ciudad (área) que el usuario ha establecido en los parámetros de ubicación actuales en la Panel de control. La aplicación puede usar esta información para ayudar al usuario a formar números de teléfono canónicos adecuados, por ejemplo, ofreciéndoles como valores predeterminados cuando se introducen nuevos números en una entrada de la libreta de teléfonos o un registro de base de datos.

## <a name="request-recipients"></a>Destinatarios de la solicitud

Se necesitan dos tipos de aplicaciones para ejecutar la telefonía asistida. Los clientes de *telefonía* asistida son aplicaciones que usan la telefonía asistida llamando a las funciones que tienen el prefijo "tapi". Un ejemplo de este tipo de aplicación cliente sería una hoja de cálculo a la que se agrega **un comando de** menú Dial o un botón de barra de herramientas.

Los servidores de *telefonía* asistida son aplicaciones que pueden ejecutar funciones de API de telefonía que resultan de la llamada de otra aplicación a una función con prefijo "tapi". Para que se conozca como servidor de telefonía asistida, dicha aplicación se registra como una mediante la [**función lineRegisterRequestRecipient.**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient)

Las funciones de telefonía asistida (que comienzan con el prefijo "tapi") se conocen como funciones *de solicitud*. Las aplicaciones de telefonía asistida que procesan estas solicitudes(servidores de telefonía asistida) se denominan *destinatarios de solicitudes.*

## <a name="processing-assisted-telephony-requests"></a>Procesamiento de solicitudes de telefonía asistida

El proceso con el que se entregan y atendidas las solicitudes es el siguiente:

1.  Cuando TAPI recibe una solicitud de telefonía asistida, comprueba si hay un destinatario de la solicitud, es decir, una aplicación registrada actualmente para procesar ese tipo de solicitud. Si hay un destinatario de la solicitud, la solicitud se pone en cola y la aplicación de prioridad más alta que se ha registrado para el servicio de esa solicitud se envía un [**mensaje DE SOLICITUD \_ DE LÍNEA.**](./line-request.md) El mensaje notifica al destinatario de la solicitud que ha llegado una nueva solicitud y lleva una indicación del modo de la solicitud.
2.  Si TAPI no encuentra una aplicación actualmente en ejecución para procesar dicha solicitud, intenta iniciar una aplicación que se ha registrado como capaz de hacerlo. Esta información de registro se registra **en HandoffPriorities** en el registro. TAPI intenta iniciar aplicaciones en el orden en que aparecen en la **sección HandoffPriorities.** (Consulte el paso siguiente).

    Si no hay ninguna aplicación registrada actualmente, TAPI examina la lista de aplicaciones de procesamiento de solicitudes en la entrada asociada en **HandoffPriorities**. Si falta la línea asociada del archivo, si no hay ninguna aplicación en él o si no se puede iniciar ninguna de las aplicaciones de la lista, la solicitud se rechaza con el error TAPIERR \_ NOREQUESTRECIPIENT.

    Cuando se inicia un destinatario de la solicitud (independientemente de si tapi lo ha iniciado o no), es su obligación llamar a [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) durante el proceso de inicio y registrarse como destinatario de la solicitud.

3.  Si una o varias aplicaciones aparecen en la entrada, TAPI comienza con la primera aplicación enumerada (prioridad más alta) e intenta iniciarla mediante la [**función CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) Si se produce un error en el intento de iniciar la aplicación, TAPI intenta iniciar la siguiente aplicación en la lista. Cuando una aplicación se inicia correctamente, TAPI simplemente pone en cola la solicitud y devuelve una indicación de éxito a la aplicación, aunque la solicitud aún no se haya señalado al destinatario de la solicitud.

    Una vez iniciada la aplicación de destinatario de la solicitud, llama a [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), lo que hace que se envíe un mensaje [**LINE \_ REQUEST,**](./line-request.md) que indica que la solicitud está en cola. Si por algún motivo la aplicación iniciada nunca se registra, la solicitud permanece en cola y permanece en la cola indefinidamente hasta que una aplicación se registra para ese tipo de solicitud.

4.  Si TAPI encuentra que dicha aplicación registrada ya se está ejecutando o inicia correctamente una, pone en cola la solicitud, envía un mensaje LINE REQUEST a la aplicación de servidor y devuelve una indicación de éxito para la llamada de función a la aplicación de telefonía \_ asistida. Este mensaje de operación correcta solo indica que la solicitud se ha aceptado y puesto en cola, no que se ha ejecutado correctamente.

Cuando la aplicación de servidor está lista para procesar una solicitud, llama a la [**función lineGetRequest.**](/windows/win32/api/tapi/nf-tapi-linegetrequest) Esto le permite recibir cualquier información que necesite, como una dirección para marcar. A continuación, procesa la solicitud mediante las funciones TAPI (como [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) y [**lineDrop)**](/windows/win32/api/tapi/nf-tapi-linedrop)que, de lo contrario, se usarían para realizar la llamada. Al invocar **lineGetRequest** se quita la solicitud de TAPI y los parámetros de solicitud se copian en un búfer de solicitudes asignado por la aplicación. El tamaño y la interpretación del contenido del búfer dependen del modo de solicitud.

El servidor debe asegurarse de que usa los parámetros correctos al ejecutar solicitudes. Al hacerlo, se siguen estos pasos:

1.  El destinatario de la solicitud recibe primero un [**mensaje LINE \_ REQUEST**](./line-request.md) que le informa de que las solicitudes pueden existir para él en la cola de solicitudes. Esto indica a la aplicación que llame a [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) y que la siga llamando hasta que se agote la cola (si la solicitud es para realizar una nueva llamada) o para quitar una llamada existente. Este mensaje no contiene los parámetros de la solicitud, excepto en el caso de una solicitud para quitar una llamada existente.
2.  Si la solicitud va a realizar una nueva llamada, el servidor de telefonía asistida usa la función [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) para recuperar la solicitud completa, que incluye los parámetros de la solicitud. El servidor ahora tiene toda la información que necesita, como el número que se va a marcar o la identificación del creador de la solicitud. En primer lugar, sin embargo, el servidor debe asignar la memoria necesaria para almacenar esta información.
3.  Por último, el servidor ejecuta la solicitud invocando la función TAPI adecuada o el conjunto de funciones.

Si TAPI no puede iniciar una aplicación capaz de servir como destinatario de la solicitud, se produce un error en la llamada de telefonía asistida y devuelve el error TAPIERR \_ NOREQUESTRECIPIENT.

## <a name="notes-on-request-recipient-operations"></a>Notas sobre las operaciones del destinatario de la solicitud

La siguiente información se refiere a los sistemas en los que se procesan las solicitudes de telefonía asistida:

-   El Registro predeterminado debe enumerar una aplicación del administrador de llamadas en la lista de prioridad de [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall). Sería útil, pero no esencial, que la aplicación del administrador de llamadas tenga una opción de menú que permita a los usuarios establecerla en la prioridad más alta.
-   Cuando TAPI inicia automáticamente una aplicación de destinatario de telefonía asistida y es la única aplicación TAPI del sistema, esta acción inicializa TAPI. Si la aplicación destinatario de telefonía asistida inicializa y apaga el dispositivo de línea antes de registrarse para las solicitudes de telefonía asistida, TAPI también se apaga y se pierde la solicitud de telefonía asistida. Las solicitudes de telefonía asistida también pueden perderse cuando otra aplicación TAPI que se inicia realiza una inicialización y un apagado.

 

 
