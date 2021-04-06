---
description: Una valiosa característica de telefonía es el pequeño conjunto de funciones llamadas telefonía asistida.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Información general sobre telefonía asistida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6a8826fd0c273936204d9250fb91504333d807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002323"
---
# <a name="assisted-telephony-overview"></a>Información general sobre telefonía asistida

Una valiosa característica de telefonía es el pequeño conjunto de funciones llamadas telefonía asistida. La telefonía asistida está diseñada para que el establecimiento de llamadas de voz y de llamadas multimedia esté disponible para cualquier aplicación, no solo las dedicadas a la funcionalidad de telefonía. En otras palabras, la telefonía asistida permite a las aplicaciones realizar llamadas telefónicas sin necesidad de conocer los detalles de los servicios de la API de telefonía completa. Extiende la telefonía a aplicaciones de procesamiento de texto, hojas de cálculo, bases de datos, administradores de información personal y otras aplicaciones que no son de telefonía.

Para obtener una lista de las funciones de telefonía básicas de la telefonía básica de TAPI 2. x, consulte [referencia rápida](./tapi-quick-function-reference.md)de funciones de TAPI. TAPI 3. x admite la telefonía asistida a través de la interfaz [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) .

La utilidad de la telefonía asistida se puede ilustrar en el ejemplo siguiente. Una aplicación de hoja de cálculo puede incorporar funciones que marcan un número de teléfono para una llamada de voz. Siempre que la aplicación no necesite el control de llamadas detallado proporcionado por la API de telefonía completa, la telefonía asistida es la forma más sencilla y eficaz de proporcionarle funcionalidad de telefonía.

![telefonía asistida con una aplicación de hoja de cálculo](images/assist4.png)

La telefonía asistida y la API de telefonía completa se usan e implementan de maneras diferentes, por lo que no se recomienda mezclar llamadas a funciones de telefonía asistida y llamadas a funciones de API de telefonía en una sola aplicación.

## <a name="using-assisted-telephony"></a>Usar telefonía asistida

Las aplicaciones que utilizan servicios de telefonía asistidos solo inician solicitudes de llamadas que TAPI pone en cola temporalmente. La aplicación de destinatario de la solicitud recupera estas solicitudes y las ejecuta en nombre de la aplicación de telefonía asistida. La función [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) solicita el establecimiento de una llamada de voz. La aplicación que realiza la solicitud no controla la llamada.

TAPI permite al usuario establecer distintas aplicaciones del destinatario de la solicitud para cada uno de estos servicios. Una aplicación se convierte en un destinatario de la solicitud mediante el registro con [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), en el que **true** se especifica como el valor del parámetro *bEnable*. (Si se especifica **false** , se anula el registro de la aplicación como un destinatario de la solicitud, lo que debe hacer cuando se ha determinado que sus deberes de destinatario están a través de para la sesión actual). La aplicación selecciona los servicios que desea administrar en el parámetro *dwRequestMode* de **lineRegisterRequestRecipient**. Un valor posible para una solicitud es LINEREQUESTMODE \_ MAKECALL para mostrar que la aplicación controlará las solicitudes [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) . Si varias aplicaciones se registran para los mismos servicios, se usa un esquema de prioridad para permitir al usuario seleccionar qué aplicación es la preferida para controlar las solicitudes. Este esquema de prioridad es idéntico al que se usa para la entrega de llamadas y el enrutamiento de llamadas entrantes en función de una lista de nombres de archivo en **HandoffPriorities** en el registro.

## <a name="call-requests"></a>Solicitudes de llamadas

La telefonía asistida proporciona aplicaciones habilitadas para telefonía con un mecanismo fácil de usar para realizar llamadas telefónicas sin necesidad de que el desarrollador se convierta completamente en una telefonía.

La función [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) solicita una llamada de voz entre el usuario y una parte remota especificada por su número de teléfono. La solicitud se realiza a TAPI, que la pasa a una aplicación registrada como destinatario de dichas solicitudes. Este destinatario es una aplicación de administrador de llamadas.

Una vez que la aplicación ha realizado la solicitud, la llamada se controla completamente desde la aplicación del administrador de llamadas, porque las aplicaciones de telefonía asistidas no pueden administrar las llamadas. Dado que la aplicación del administrador de llamadas controla los aspectos más complejos de la telefonía y todas las operaciones de la interfaz de usuario, las aplicaciones habilitadas para telefonía no deben modificarse de ninguna manera sustancial. De hecho, es posible que las aplicaciones que permiten invocar esta operación desde su lenguaje de script integrado no tengan que modificarse en absoluto.

La función [**tapiGetLocationInfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) devuelve a la aplicación el código de país o región y el código de ciudad (área) que el usuario ha establecido en los parámetros de ubicación actuales en el panel de control de telefonía. La aplicación puede usar esta información para ayudar al usuario a formar números de teléfono canónicos correctos, por ejemplo, si los ofrece como valores predeterminados cuando se introducen nuevos números en una entrada de la libreta de teléfonos o en un registro de base de datos.

## <a name="request-recipients"></a>Solicitar destinatarios

Se necesitan dos tipos de aplicaciones para ejecutar la telefonía asistida. *Los clientes* de telefonía asistidos son aplicaciones que usan telefonía asistida llamando a las funciones que tienen el prefijo "TAPI". Un ejemplo de este tipo de aplicación cliente sería una hoja de cálculo a la que se agrega un comando de menú de **marcado** o un botón de barra de herramientas.

*Los servidores* de telefonía asistidos son aplicaciones que pueden ejecutar funciones de la API de telefonía que se derivan de la llamada de otra aplicación a una función con prefijo "TAPI". Para que sea conocido como un servidor de telefonía asistido, una aplicación de este tipo se registra como una mediante la función [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) .

Las funciones de telefonía asistida (que comienzan por el prefijo "TAPI") se conocen como *funciones de solicitud*. Las aplicaciones de telefonía asistida que procesan estas solicitudes (servidores de telefonía asistidos) se denominan *destinatarios* de la solicitud.

## <a name="processing-assisted-telephony-requests"></a>Procesamiento de solicitudes de telefonía asistida

El proceso con el que se entregan y se realizan los servicios de las solicitudes es el siguiente:

1.  Cuando TAPI recibe una solicitud de telefonía asistida, busca un destinatario de la solicitud, es decir, una aplicación registrada actualmente para procesar ese tipo de solicitud. Si hay un destinatario de la solicitud, la solicitud se pone en cola y se envía un mensaje de [**\_ solicitud de línea**](./line-request.md) a la aplicación de prioridad más alta que se ha registrado para el servicio de esa solicitud. El mensaje notifica al destinatario de la solicitud que ha llegado una solicitud nueva y lleva una indicación del modo de la solicitud.
2.  Si TAPI no encuentra una aplicación actualmente en ejecución para procesar dicha solicitud, intenta iniciar una aplicación que se ha registrado como capaz de hacerlo. Esta información de registro se registra en **HandoffPriorities** en el registro. TAPI intenta iniciar aplicaciones en el orden en el que aparecen en la sección **HandoffPriorities** . (Consulte el paso siguiente).

    Si no hay ninguna aplicación registrada actualmente, TAPI examinará la lista de aplicaciones de procesamiento de solicitudes en la entrada asociada en **HandoffPriorities**. Si falta la línea asociada en el archivo, si no hay ninguna aplicación enumerada, o si no se puede iniciar ninguna de las aplicaciones de la lista, la solicitud se rechaza con el error TAPIERR \_ NOREQUESTRECIPIENT.

    Cuando se inicia un destinatario de la solicitud (tanto si TAPI lo inició como si no), es su deber llamar a [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) durante el proceso de inicio y registrarse como destinatario de la solicitud.

3.  Si una o varias aplicaciones se enumeran en la entrada, TAPI comienza con la primera aplicación de la lista (prioridad más alta) e intenta iniciarla con la función [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Si se produce un error al intentar iniciar la aplicación, TAPI intenta iniciar la siguiente aplicación de la lista. Cuando una aplicación se inicia correctamente, TAPI simplemente pone en cola la solicitud y devuelve una indicación de éxito a la aplicación aunque la solicitud todavía no se haya señalado al destinatario de la solicitud.

    Una vez iniciada la aplicación de destinatario de la solicitud, llama a [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), que hace que se envíe un mensaje de [**\_ solicitud de línea**](./line-request.md) , señalando que la solicitud está en cola. Si, por alguna razón, la aplicación iniciada no se registra nunca, la solicitud permanece en cola y permanece en la cola indefinidamente hasta que una aplicación se registra para ese tipo de solicitud.

4.  Si TAPI encuentra una aplicación registrada que ya se está ejecutando o inicia una correctamente, pone en cola la solicitud, envía un mensaje de solicitud de línea \_ a la aplicación de servidor y devuelve una indicación de éxito para la llamada de función a la aplicación de telefonía asistida. Este mensaje de operación correcta solo indica que la solicitud se ha aceptado y puesto en cola, no que se ha ejecutado correctamente.

Cuando la aplicación de servidor está lista para procesar una solicitud, llama a la función [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) . Esto le permite recibir toda la información que necesita, como una dirección para marcar. A continuación, procesa la solicitud mediante las funciones TAPI (como [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) y [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop)) que, de lo contrario, se utilizaría para realizar la llamada. Al invocar **lineGetRequest** se quita la solicitud de TAPI y los parámetros de la solicitud se copian en un búfer de solicitud asignado por la aplicación. El tamaño y la interpretación del contenido del búfer dependen del modo de solicitud.

El servidor debe asegurarse de que usa los parámetros correctos al ejecutar las solicitudes. Al hacerlo, se siguen estos pasos:

1.  El destinatario de la solicitud recibe primero un mensaje de [**\_ solicitud de línea**](./line-request.md) que le informa de que pueden existir solicitudes en la cola de solicitudes. Esto indica a la aplicación que llame a [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) y siga llamándolo hasta que se vacíe la cola (si la solicitud es para realizar una nueva llamada) o para quitar una llamada existente. Este mensaje no contiene los parámetros de la solicitud, excepto en el caso de una solicitud para quitar una llamada existente.
2.  Si la solicitud es crear una nueva llamada, el servidor de telefonía asistido utiliza la función [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) para recuperar la solicitud completa, que incluye los parámetros de la solicitud. El servidor ahora tiene toda la información que necesita, como el número que se debe marcar o la identificación del creador de la solicitud. En primer lugar, sin embargo, el servidor debe asignar la memoria necesaria para almacenar esta información.
3.  Por último, el servidor ejecuta la solicitud mediante la invocación de la función o el conjunto de funciones TAPI adecuado.

Si TAPI no puede iniciar una aplicación capaz de servir como destinatario de la solicitud, se produce un error en la llamada de telefonía asistida y se devuelve el error TAPIERR \_ NOREQUESTRECIPIENT.

## <a name="notes-on-request-recipient-operations"></a>Notas sobre las operaciones del destinatario de la solicitud

La siguiente información se refiere a los sistemas en los que se procesan las solicitudes de telefonía asistidas:

-   El registro predeterminado debe mostrar una aplicación de administrador de llamadas en la lista de prioridades de [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall). Sería útil, pero no esencial, que la aplicación del administrador de llamadas tenga una opción de menú que permita a los usuarios establecerla en la prioridad más alta.
-   Cuando TAPI inicia automáticamente una aplicación de destinatario de telefonía asistida y se trata de la única aplicación TAPI del sistema, esta acción inicializa TAPI. Si la aplicación de destinatario de telefonía asistida se inicializa y cierra el dispositivo de línea antes de registrarse para las solicitudes de telefonía asistida, TAPI también se apaga y se pierde la solicitud de telefonía asistida. También es posible que se pierdan solicitudes de telefonía asistidas cuando otra aplicación TAPI iniciada realiza una inicialización y cierre.

 

 
