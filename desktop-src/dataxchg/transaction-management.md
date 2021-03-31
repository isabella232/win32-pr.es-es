---
title: Administración de transacciones (intercambio de datos)
description: En este tema se describe cómo un cliente puede enviar transacciones para obtener datos y servicios del servidor.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), transacciones
- DDE (Intercambio dinámico de datos), transacciones
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), transacciones
- DDEML (biblioteca de administración de Intercambio dinámico de datos), transacciones
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Intercambio dinámico de datos (DDE), transacciones de solicitud
- DDE (Intercambio dinámico de datos), transacciones de solicitud
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), solicitudes de solicitud
- DDEML (biblioteca de administración de Intercambio dinámico de datos), transacciones de solicitud
- Intercambio dinámico de datos (DDE), transacciones de los
- DDE (Intercambio dinámico de datos), transacciones de los
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), transacciones de postarchivo
- DDEML (biblioteca de administración de Intercambio dinámico de datos), transacciones de los
- Intercambio dinámico de datos (DDE), transacciones de notificaciones
- DDE (Intercambio dinámico de datos), transacciones de notificaciones
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), transacciones de notificaciones
- DDEML (biblioteca de administración de Intercambio dinámico de datos), transacciones de notificaciones
- Intercambio dinámico de datos (DDE), ejecutar transacciones
- DDE (Intercambio dinámico de datos), ejecutar transacciones
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), ejecutar transacciones
- DDEML (biblioteca de administración de Intercambio dinámico de datos), ejecutar transacciones
- Intercambio dinámico de datos (DDE), transacciones sincrónicas
- DDE (Intercambio dinámico de datos), transacciones sincrónicas
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), transacciones sincrónicas
- DDEML (biblioteca de administración de Intercambio dinámico de datos), transacciones sincrónicas
- Intercambio dinámico de datos (DDE), transacciones asincrónicas
- DDE (Intercambio dinámico de datos), transacciones asincrónicas
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), transacciones asincrónicas
- DDEML (biblioteca de administración de Intercambio dinámico de datos), transacciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570aa48b4dcdbb31855b3e1b15a091908feb2ba4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077893"
---
# <a name="transaction-management-data-exchange"></a>Administración de transacciones (intercambio de datos)

Después de establecer una conversación con un servidor, un cliente puede enviar transacciones para obtener datos y servicios del servidor.

En los temas siguientes se describen los tipos de transacciones que los clientes pueden usar para interactuar con un servidor de.

-   [Transacción de solicitud](#request-transaction)
-   [Escribir transacción](#poke-transaction)
-   [Avisar transacción](#advise-transaction)
-   [Ejecutar transacción](#execute-transaction)
-   [Transacciones sincrónicas y asincrónicas](#synchronous-and-asynchronous-transactions)
-   [Control de transacciones](#transaction-control)
-   [Clases de transacción](#transaction-classes)
-   [Tipos de transacción](#transaction-types)

## <a name="request-transaction"></a>Transacción de solicitud

Una aplicación cliente puede utilizar la transacción de [**\_ solicitud XTYP**](xtyp-request.md) para solicitar un elemento de datos de una aplicación de servidor. El cliente llama a la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , especificando la **\_ solicitud XTYP** como el tipo de transacción y especificando el elemento de datos que necesita la aplicación.

La biblioteca de administración de Intercambio dinámico de datos (DDEML) pasa la transacción de [**\_ solicitud XTYP**](xtyp-request.md) al servidor, especificando el nombre del tema, el nombre del elemento y el formato de datos solicitado por el cliente. Si el servidor admite el tema, el elemento y el formato solicitados, el servidor debe devolver un identificador de datos que identifique el valor actual del elemento. DDEML pasa este identificador al cliente como el valor devuelto de [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). El servidor debe devolver **null** si no admite el tema, el elemento o el formato solicitado.

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) usa el parámetro *lpdwResult* para devolver una marca de estado de transacción al cliente. Si el servidor no procesa la transacción [**de \_ solicitud XTYP**](xtyp-request.md) , **DdeClientTransaction** devuelve **null** y *LPDWRESULT* apunta a la marca DDE \_ FNOTPROCESSED o DDE \_ FBUSY. Si \_ se devuelve la marca DDE FNOTPROCESSED, el cliente no puede determinar por qué el servidor no ha procesado la transacción.

Si un servidor no admite la transacción [**de \_ solicitud XTYP**](xtyp-request.md) , debe especificar la marca de \_ filtro CBF FAIL \_ requests en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Esta marca evita que DDEML envíe la transacción al servidor.

## <a name="poke-transaction"></a>Escribir transacción

Un cliente puede enviar datos no solicitados a un servidor mediante el uso de [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) para enviar una transacción de [**XTYP \_**](xtyp-poke.md) a la función de devolución de llamada de un servidor.

La aplicación cliente crea primero un búfer que contiene los datos que se van a enviar al servidor y, a continuación, pasa un puntero al búfer como un parámetro a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Como alternativa, el cliente puede usar la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para obtener un identificador de datos que identifique los datos y, a continuación, pasar el identificador a **DdeClientTransaction**. En cualquier caso, el cliente también especifica el nombre del tema, el nombre del elemento y el formato de los datos cuando llama a **DdeClientTransaction**.

El objeto DDEML pasa [**la \_ transacción de XTYP**](xtyp-poke.md) de datos al servidor, especificando el nombre del tema, el nombre del elemento y el formato de datos que el cliente solicitó. Para aceptar el elemento de datos y el formato, el servidor debe devolver el \_ Fack DDE. Para rechazar los datos, el servidor debe devolver \_ FNOTPROCESSED DDE. Si el servidor está demasiado ocupado para aceptar los datos, el servidor debe devolver el \_ FBUSY DDE.

Cuando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) devuelve, el cliente puede usar el parámetro *lpdwResult* para tener acceso a la marca Transaction-status. Si la marca es DDE \_ FBUSY, el cliente debe enviar la transacción de nuevo más tarde.

Si un servidor no admite la transacción [**XTYP \_**](xtyp-poke.md) , debe especificar la marca del filtro CBF \_ FAIL-fails \_ en [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Esta marca evita que DDEML envíe esta transacción al servidor.

## <a name="advise-transaction"></a>Avisar transacción

Una aplicación cliente puede usar DDEML para establecer uno o varios vínculos a los elementos de una aplicación de servidor. Cuando se ha establecido un vínculo de este tipo, el servidor envía actualizaciones periódicas sobre el elemento vinculado al cliente (normalmente, siempre que cambia el valor del elemento asociado a la aplicación de servidor). La vinculación establece un bucle de notificación entre las dos aplicaciones que permanecen en su lugar hasta que el cliente la finaliza.

Hay dos tipos de bucles de notificación: "activo" y "cálido". En un bucle de aviso activo, el servidor envía inmediatamente un identificador de datos que identifica el valor modificado. En un bucle de aviso cálido, el servidor notifica al cliente que el valor del elemento ha cambiado pero no envía el identificador de datos hasta que el cliente lo solicita.

Un cliente puede solicitar un bucle de aviso activo con un servidor especificando el tipo de transacción [**XTYP \_ ADVSTART**](xtyp-advstart.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Para solicitar un bucle de aviso cálido, el cliente debe combinar la \_ marca XTYPF NoData con el tipo de transacción **\_ ADVSTART de XTYP** . En cualquiera de los dos eventos, DDEML pasa la transacción **XTYP \_ ADVSTART** a la función de devolución de llamada de intercambio dinámico de datos (DDE) del servidor. La función de devolución de llamada DDE del servidor debe examinar los parámetros que acompañan a la transacción **XTYP \_ ADVSTART** (incluido el formato solicitado, el nombre del tema y el nombre del elemento) y, a continuación, devolver **true** para permitir el bucle de notificación o **false** para denegarlo.

Una vez establecido un bucle de notificaciones, la aplicación de servidor debe llamar a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) siempre que cambie el valor del elemento asociado al nombre de elemento solicitado. Esta llamada produce una transacción [**XTYP \_ ADVREQ**](xtyp-advreq.md) que se envía a la función de devolución de llamada DDE del servidor. La función de devolución de llamada DDE del servidor debe devolver un identificador de datos que identifique el nuevo valor del elemento de datos. A continuación, DDEML notifica al cliente que el elemento especificado ha cambiado mediante el envío de la transacción [**XTYP \_ ADVDATA**](xtyp-advdata.md) a la función de devolución de llamada DDE del cliente.

Si el cliente solicitó un bucle de aviso activo, el DDEML pasa el identificador de datos al elemento cambiado al cliente durante la transacción de [**\_ ADVDATA de XTYP**](xtyp-advdata.md) . De lo contrario, el cliente puede enviar una transacción de [**\_ solicitud XTYP**](xtyp-request.md) para obtener el identificador de datos.

Es posible que un servidor envíe actualizaciones más rápido de lo que un cliente puede procesar los nuevos datos. La velocidad de las actualizaciones puede ser un problema para un cliente que debe realizar operaciones de procesamiento prolongadas en los datos. En este caso, el cliente debe especificar la \_ marca XTYPF ACKREQ cuando solicita un bucle de notificación. Esta marca hace que el servidor espere a que el cliente confirme que ha recibido y procesado un elemento de datos antes de que el servidor envíe el siguiente elemento de datos. Los bucles de aviso que se establecen con la \_ marca XTYPF ACKREQ son más sólidos con servidores rápidos, pero ocasionalmente pueden faltar actualizaciones. Se garantiza que los bucles de aviso establecidos sin la \_ marca ACKREQ de XTYPF no se pierdan las actualizaciones siempre y cuando el cliente siga con el servidor.

Un cliente puede finalizar un bucle de notificación especificando el tipo de transacción [**XTYP \_ ADVSTOP**](xtyp-advstop.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).

Si un servidor no admite bucles de notificación, debe especificar la marca de \_ filtro CBF FAIL \_ asesorator en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Esta marca evita que DDEML envíe las transacciones [**XTYP \_ ADVSTART**](xtyp-advstart.md) y [**XTYP \_ ADVSTOP**](xtyp-advstop.md) al servidor.

## <a name="execute-transaction"></a>Ejecutar transacción

Un cliente puede usar la transacción de [**\_ ejecución XTYP**](xtyp-execute.md) para hacer que un servidor ejecute un comando o una serie de comandos.

Para ejecutar un comando de servidor, el cliente crea primero un búfer que contiene una cadena de comando para que el servidor se ejecute y, a continuación, pasa un puntero al búfer o un identificador de datos que identifica el búfer cuando llama a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Otros parámetros necesarios incluyen el identificador de conversación, el identificador de cadena del nombre del elemento, la especificación de formato y el tipo de transacción [**XTYP \_ Execute**](xtyp-execute.md) . Una aplicación que crea un identificador de datos para pasar datos de ejecución debe especificar **null** para el parámetro *hszItem* de la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) y cero para el parámetro *uFmt* .

El DDEML pasa la transacción de [**\_ ejecución XTYP**](xtyp-execute.md) a la función de devolución de llamada DDE del servidor y especifica el nombre de formato, el identificador de conversación, el nombre del tema y el identificador de datos que identifica la cadena de comando. Si el servidor admite el comando, debe usar la función [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obtener un puntero a la cadena de comandos, ejecutar el comando y, a continuación, devolver el valor de Fack de DDE \_ . Si el servidor no admite el comando o no puede completar la transacción, debe devolver DDE \_ FNOTPROCESSED. El servidor debe devolver \_ FBUSY DDE si está demasiado ocupado para completar la transacción.

En general, la función de devolución de llamada de un servidor debe procesar la transacción de [**\_ ejecución XTYP**](xtyp-execute.md) antes de volver con las excepciones siguientes:

1.  Cuando el comando que se pasa con la transacción de [**\_ ejecución XTYP**](xtyp-execute.md) solicita al servidor que finalice, el servidor no debe finalizar hasta que su función de devolución de llamada vuelva del procesamiento **XTYP \_ Execute**.
2.  Si el servidor debe realizar una operación, como el procesamiento de un cuadro de diálogo o una transacción DDE que pueda causar problemas de recursividad de DDEML, el servidor debe devolver el \_ código de retorno del bloque CBR para bloquear la transacción de ejecución, realizar la operación y, a continuación, reanudar el procesamiento de la transacción de ejecución.

Cuando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) devuelve, el cliente puede usar el parámetro *lpdwResult* para tener acceso a la marca de estado de la transacción. Si la marca es DDE \_ FBUSY, el cliente debe enviar la transacción de nuevo más tarde.

Si un servidor no admite la transacción [**de \_ ejecución XTYP**](xtyp-execute.md) , debe especificar la marca de \_ filtro CBF FAIL \_ executes en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Al hacerlo, se impide que DDEML envíe la transacción al servidor.

## <a name="synchronous-and-asynchronous-transactions"></a>Transacciones sincrónicas y asincrónicas

Un cliente puede enviar transacciones sincrónicas o asincrónicas. En una transacción sincrónica, el cliente especifica un valor de tiempo de espera que indica la cantidad máxima de tiempo que esperará a que el servidor procese la transacción. [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) no vuelve hasta que el servidor procesa la transacción, se produce un error en la transacción o el valor de tiempo de espera expira. El cliente especifica el valor de tiempo de espera cuando llama a **DdeClientTransaction**.

Durante una transacción sincrónica, el cliente entra en un bucle modal mientras espera a que se procese la transacción. El cliente todavía puede procesar la entrada del usuario, pero no puede enviar otra transacción sincrónica hasta que [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) devuelve.

Un cliente envía una transacción asincrónica especificando la \_ marca Async de tiempo de espera en [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). La función devuelve una vez iniciada la transacción, pasando un identificador de transacción al cliente. Cuando el servidor finaliza el procesamiento de la transacción asincrónica, el DDEML envía una transacción [**XTYP \_ Xact \_ Complete**](xtyp-xact-complete.md) al cliente. Uno de los parámetros que DDEML pasa al cliente durante la transacción **XTYP \_ Xact \_ Complete** es el identificador de la transacción. Al comparar este identificador de transacción con el identificador devuelto por **DdeClientTransaction**, el cliente identifica qué transacción asincrónica ha finalizado el procesamiento del servidor.

Un cliente puede utilizar la función [**DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) como ayuda para procesar una transacción asincrónica. Esta función permite a un cliente asociar un valor definido por la aplicación con un identificador de conversación y un identificador de transacción. El cliente puede usar la función [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante la transacción de transacciones [**\_ \_ completadas de XTYP**](xtyp-xact-complete.md) para obtener el valor definido por la aplicación. Debido a esta función, una aplicación no necesita mantener una lista de identificadores de transacciones activos.

Cuando un cliente completa correctamente una solicitud de datos mediante una transacción sincrónica, DDEML no tiene ninguna manera de saber cuándo el cliente ha terminado de usar los datos recibidos. La aplicación cliente debe pasar el identificador de datos recibido a la función [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) , notificando a ddeml que el identificador ya no se usará. Los identificadores de datos devueltos por las transacciones sincrónicas son propiedad del cliente.

Si un servidor no procesa una transacción asincrónica de manera oportuna, el cliente puede abandonar la transacción llamando a la función [**DdeAbandonTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) . DDEML libera todos los recursos asociados a la transacción y descarta los resultados de la transacción cuando el servidor finaliza su procesamiento. Un tiempo de espera durante una transacción sincrónica cancela la transacción de forma efectiva.

El método de transacción asincrónica se proporciona para las aplicaciones que deben enviar un gran volumen de transacciones DDE al mismo tiempo que realiza una cantidad considerable de procesamiento, como la realización de cálculos. El método asincrónico también es útil en las aplicaciones que deben detener el procesamiento de transacciones DDE temporalmente para que puedan realizar otras tareas sin interrupción. En la mayoría de las demás situaciones, una aplicación debe utilizar el método sincrónico.

Las transacciones sincrónicas son más fáciles de mantener y son más rápidas que las transacciones asincrónicas. Sin embargo, solo se puede realizar una transacción sincrónica a la vez, mientras que muchas transacciones asincrónicas se pueden realizar simultáneamente. Con las transacciones sincrónicas, un servidor lento puede hacer que un cliente permanezca inactivo mientras está esperando una respuesta. Además, las transacciones sincrónicas hacen que el cliente entre en un bucle modal que podría omitir el filtrado de mensajes en el bucle de mensajes propio de la aplicación.

Si el cliente ha instalado un procedimiento de enlace para filtrar los mensajes (es decir, especifica el \_ tipo de enlace qu MSGFILTER en una llamada a la función [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) ), una transacción sincrónica no hará que el sistema omita el procedimiento de enlace. Cuando se produce un evento de entrada mientras el cliente está esperando a que finalice una transacción sincrónica, el procedimiento de enlace recibe un código de enlace de DDEMGR de MSGF \_ . El principal peligro del uso de un bucle modal de transacciones sincrónicas es que un bucle modal creado por un cuadro de diálogo puede interferir con su operación. Las transacciones asincrónicas siempre se deben usar cuando un archivo DLL usa DDEML.

## <a name="transaction-control"></a>Control de transacciones

Una aplicación puede suspender las transacciones a su función de devolución de llamada DDE, tanto las transacciones asociadas a un identificador de conversación específico como todas las transacciones, independientemente del identificador de conversación. Esta capacidad resulta útil cuando una aplicación recibe una transacción que requiere un procesamiento prolongado. En tal caso, la aplicación puede devolver el código de \_ retorno del bloque CBR para suspender las transacciones futuras asociadas al identificador de conversación de la transacción, de modo que la aplicación pueda procesar otras conversaciones de forma gratuita.

Cuando se ha completado el procesamiento, la aplicación llama a la función [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) para reanudar las transacciones asociadas a la conversación suspendida. La llamada a **DdeEnableCallback** hace que ddeml Reenvíe la transacción que dio lugar a la suspensión de la conversación en la aplicación. Por lo tanto, la aplicación debe almacenar el resultado de la transacción de manera que pueda obtener y devolver el resultado sin volver a procesar la transacción.

Una aplicación puede suspender todas las transacciones asociadas a un identificador de conversación específico especificando el identificador y la \_ marca de deshabilitación de EC en una llamada a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Al especificar un identificador **nulo** , una aplicación puede suspender todas las transacciones de todas las conversaciones.

Cuando una conversación se ha suspendido, DDEML guarda las transacciones de la conversación en una cola de transacciones. Cuando la aplicación vuelva a habilitar la conversación, DDEML quitará las transacciones guardadas de la cola y pasará cada transacción a la función de devolución de llamada adecuada. La capacidad de la cola de transacciones es grande, pero una aplicación debe volver a habilitar una conversación suspendida tan pronto como sea posible para evitar la pérdida de transacciones.

Una aplicación puede reanudar el procesamiento de transacciones habitual especificando la \_ marca ENABLEALL de EC en [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Para una reanudación más controlada del procesamiento de transacciones, la aplicación puede especificar la \_ marca ENABLEONE de EC. Esta marca quita una transacción de la cola de transacciones y la pasa a la función de devolución de llamada adecuada; una vez procesada la transacción, se deshabilitan de nuevo las conversaciones.

Si la \_ marca ENABLEONE y un identificador de conversación se especifican en la llamada a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback), solo se bloqueará esa conversación una vez que se haya procesado la transacción. Si se especifica un identificador de conversación **null** , todas las conversaciones se bloquean después de que una transacción se haya procesado en cualquier conversación.

## <a name="transaction-classes"></a>Clases de transacción

DDEML tiene cuatro clases de transacciones. Cada clase se identifica mediante una constante que comienza con el \_ prefijo XCLASS. Las clases se definen en el archivo de encabezado DDEML. El valor de clase se combina con el valor de tipo de transacción y se pasa a la función de devolución de llamada DDE de la aplicación receptora.

La clase de una transacción determina el valor devuelto que se espera que devuelva una función de devolución de llamada si procesa la transacción. Los siguientes valores devueltos y tipos de transacción se asocian a cada una de las cuatro clases de transacción.



| Clase                | Valor devuelto                                                     | Transacción                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ bool         | **True** o **false**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**conexión de XTYP \_**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| datos de XCLASS \_         | Un identificador de datos, el \_ código de retorno del bloque CBR o **null**           | [**XTYP \_ ADVREQ**](xtyp-advreq.md)<br/> [**solicitud de XTYP \_**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| marcas de XCLASS \_        | Una marca de transacción: DDE \_ Fack, DDE \_ FBUSY o DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**\_Ejecutar XTYP**](xtyp-execute.md)<br/> [**XTYP \_**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| \_notificación XCLASS | None                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**\_confirmación de conexión de XTYP \_**](xtyp-connect-confirm.md)<br/> [**desconexión de XTYP \_**](xtyp-disconnect.md)<br/> [**\_error XTYP**](xtyp-error.md)<br/> [**registro de XTYP \_**](xtyp-register.md)<br/> [**XTYP \_ anular registro**](xtyp-unregister.md)<br/> [**\_transacción XTYP \_ completada**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Tipos de transacción

Cada tipo de transacción DDE tiene un receptor y una actividad asociada que hace que DDEML genere cada tipo.



| Tipo de transacción                                       | Receptor                   | Causa                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | Remoto                     | Un servidor respondió a una transacción de [**\_ ADVREQ de XTYP**](xtyp-advreq.md) devolviendo un identificador de datos.                                                                          |
| [**XTYP \_ ADVREQ**](xtyp-advreq.md)                    | Servidor                     | Un servidor llamado a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) , que indica que el valor de un elemento de datos en un bucle de notificación ha cambiado.                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | Servidor                     | Un cliente especificó el tipo de transacción [**XTYP \_ ADVSTART**](xtyp-advstart.md) en una llamada a la función [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) .               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | Servidor                     | Un cliente especificó el tipo de transacción [**XTYP \_ ADVSTOP**](xtyp-advstop.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**conexión de XTYP \_**](xtyp-connect.md)                  | Servidor                     | Un cliente llamó a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) y especificó un nombre de servicio y un nombre de tema admitidos por el servidor.                                            |
| [**\_confirmación de conexión de XTYP \_**](xtyp-connect-confirm.md) | Servidor                     | El servidor devolvió **true** como respuesta a una transacción [**XTYP \_ Connect**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) .                            |
| [**desconexión de XTYP \_**](xtyp-disconnect.md)            | Cliente/servidor              | Un asociado en una conversación denominada función [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) , que hace que ambos asociados reciban esta transacción.                                    |
| [**\_error XTYP**](xtyp-error.md)                      | Cliente/servidor              | Se ha producido un error crítico. No es posible que el DDEML tenga suficientes recursos para continuar.                                                                                       |
| [**\_Ejecutar XTYP**](xtyp-execute.md)                  | Servidor                     | Un cliente especificó el tipo de transacción [**XTYP \_ Execute**](xtyp-execute.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**MONITOR de XTYP \_**](xtyp-monitor.md)                  | Aplicación de supervisión DDE | Se produjo un evento DDE en el sistema. Para obtener más información acerca de las aplicaciones de supervisión de DDE, consulte [supervisión de aplicaciones](monitoring-applications.md).                       |
| [**XTYP \_**](xtyp-poke.md)                        | Servidor                     | Un cliente especificó el tipo de transacción [**XTYP \_**](xtyp-poke.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                                    |
| [**registro de XTYP \_**](xtyp-register.md)                | Cliente/servidor              | Una aplicación de servidor usó la función [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar un nombre de servicio.                                                                   |
| [**solicitud de XTYP \_**](xtyp-request.md)                  | Servidor                     | Un cliente especificó el tipo de transacción de [**\_ solicitud XTYP**](xtyp-request.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**XTYP \_ anular registro**](xtyp-unregister.md)            | Cliente/servidor              | Una aplicación de servidor usó [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para anular el registro de un nombre de servicio.                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | Servidor                     | Un cliente llamó a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) , especificando **null** para el nombre del servicio, el nombre del tema o ambos. |
| [**\_transacción XTYP \_ completada**](xtyp-xact-complete.md)     | Remoto                     | Una transacción asincrónica, enviada cuando el cliente especificó la \_ marca Async de tiempo de espera en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction), ha concluido.         |



 

 

