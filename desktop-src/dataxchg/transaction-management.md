---
title: Administración de transacciones (data Exchange)
description: En este tema se describe cómo un cliente puede enviar transacciones para obtener datos y servicios del servidor.
ms.assetid: 2d08ffa3-cbd7-4806-b94f-979938322c38
keywords:
- Windows Interfaz de usuario,datos dinámicos Exchange (DDE)
- datos dinámicos Exchange (DDE), transacciones
- DDE (datos dinámicos Exchange), transacciones
- intercambio de datos, datos dinámicos Exchange (DDE)
- Windows Interfaz de usuario,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange Management Library (DDEML),transactions
- DDEML (datos dinámicos Exchange management library),transactions
- intercambio de datos,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange (DDE), solicitar transacciones
- DDE (datos dinámicos Exchange), solicitar transacciones
- datos dinámicos Exchange Management Library (DDEML), solicitar transacciones
- DDEML (datos dinámicos Exchange Management Library), solicitar transacciones
- datos dinámicos Exchange (DDE), transacciones de transacción
- DDE (datos dinámicos Exchange), transacciones más rápidas
- datos dinámicos Exchange Management Library (DDEML), transacciones de transacciones
- DDEML (datos dinámicos Exchange management library), transacciones de transacciones
- datos dinámicos Exchange (DDE), aconsejar transacciones
- DDE (datos dinámicos Exchange), aconsejar transacciones
- datos dinámicos Exchange Management Library (DDEML), aconsejar transacciones
- DDEML (datos dinámicos Exchange Management Library), aconsejar transacciones
- datos dinámicos Exchange (DDE), ejecutar transacciones
- DDE (datos dinámicos Exchange), ejecutar transacciones
- datos dinámicos Exchange Management Library (DDEML), ejecutar transacciones
- DDEML (datos dinámicos Exchange Management Library), ejecutar transacciones
- datos dinámicos Exchange (DDE), transacciones sincrónicas
- DDE (datos dinámicos Exchange), transacciones sincrónicas
- datos dinámicos Exchange Management Library (DDEML), transacciones sincrónicas
- DDEML (datos dinámicos Exchange management library), transacciones sincrónicas
- datos dinámicos Exchange (DDE), transacciones asincrónicas
- DDE (datos dinámicos Exchange), transacciones asincrónicas
- datos dinámicos Exchange Management Library (DDEML), transacciones asincrónicas
- DDEML (datos dinámicos Exchange management library), transacciones asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5065c9e909a4589cd7d2d157fc1151c2efd42a4ddfc3c29d84fd26f0ea184dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128586"
---
# <a name="transaction-management-data-exchange"></a>Administración de transacciones (data Exchange)

Después de establecer una conversación con un servidor, un cliente puede enviar transacciones para obtener datos y servicios del servidor.

En los temas siguientes se describen los tipos de transacciones que los clientes pueden usar para interactuar con un servidor.

-   [Transacción de solicitud](#request-transaction)
-   [Transacción de traslación](#poke-transaction)
-   [Aconsejar transacción](#advise-transaction)
-   [Ejecutar transacción](#execute-transaction)
-   [Transacciones sincrónicas y asincrónicas](#synchronous-and-asynchronous-transactions)
-   [Control de transacciones](#transaction-control)
-   [Clases de transacción](#transaction-classes)
-   [Tipos de transacción](#transaction-types)

## <a name="request-transaction"></a>Transacción de solicitud

Una aplicación cliente puede usar la [**transacción XTYP \_ REQUEST**](xtyp-request.md) para solicitar un elemento de datos de una aplicación de servidor. El cliente llama a la [**función DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) **especificando XTYP \_ REQUEST** como tipo de transacción y especificando el elemento de datos que la aplicación necesita.

La datos dinámicos Exchange Management Library (DDEML) pasa la transacción [**XTYP \_ REQUEST**](xtyp-request.md) al servidor, especificando el nombre del tema, el nombre del elemento y el formato de datos solicitados por el cliente. Si el servidor admite el tema, el elemento y el formato solicitados, el servidor debe devolver un identificador de datos que identifique el valor actual del elemento. DDEML pasa este identificador al cliente como el valor devuelto de [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) El servidor debe devolver **NULL** si no admite el tema, el elemento o el formato solicitados.

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) usa el *parámetro lpdwResult* para devolver una marca de estado de transacción al cliente. Si el servidor no procesa la transacción [**XTYP \_ REQUEST,**](xtyp-request.md) **DdeClientTransaction** devuelve **NULL** y *lpdwResult* apunta a la marca \_ FNOTPROCESSED o \_ DDE FBUSY de DDE. Si se devuelve la marca FNOTPROCESSED de DDE, el cliente no puede determinar por qué el servidor \_ no procesó la transacción.

Si un servidor no admite la transacción [**XTYP \_ REQUEST,**](xtyp-request.md) debe especificar la marca de filtro CBF FAIL REQUESTS en la \_ función \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Esta marca impide que DDEML envíe la transacción al servidor.

## <a name="poke-transaction"></a>Transacción de traslación

Un cliente puede enviar datos no solicitados a un servidor mediante [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) para enviar una transacción [**\_ XTYP DHCPE**](xtyp-poke.md) a la función de devolución de llamada de un servidor.

La aplicación cliente crea primero un búfer que contiene los datos que se envían al servidor y, a continuación, pasa un puntero al búfer como parámetro a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Como alternativa, el cliente puede usar la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) para obtener un identificador de datos que identifique los datos y, a continuación, pasar el identificador a **DdeClientTransaction**. En cualquier caso, el cliente también especifica el nombre del tema, el nombre del elemento y el formato de datos cuando llama a **DdeClientTransaction**.

DDEML pasa la transacción [**XTYP \_ TFTPE**](xtyp-poke.md) al servidor, especificando el nombre del tema, el nombre del elemento y el formato de datos que solicitó el cliente. Para aceptar el formato y el elemento de datos, el servidor debe devolver DDE \_ FACK. Para rechazar los datos, el servidor debe devolver DDE \_ FNOTPROCESSED. Si el servidor está demasiado ocupado para aceptar los datos, el servidor debe devolver DDE \_ FBUSY.

Cuando [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) devuelve un valor, el cliente puede usar el *parámetro lpdwResult* para acceder a la marca de estado de transacción. Si la marca es DDE \_ FBUSY, el cliente debe volver a enviar la transacción más adelante.

Si un servidor no es compatible con la transacción [**\_ XTYP RADIUSE,**](xtyp-poke.md) debe especificar la marca de filtro CBF FAIL DHCPES en \_ \_ [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Esta marca impide que DDEML envíe esta transacción al servidor.

## <a name="advise-transaction"></a>Aconsejar transacción

Una aplicación cliente puede usar DDEML para establecer uno o varios vínculos a elementos de una aplicación de servidor. Cuando se ha establecido este vínculo, el servidor envía actualizaciones periódicas sobre el elemento vinculado al cliente (normalmente, cada vez que cambia el valor del elemento asociado a la aplicación de servidor). La vinculación establece un bucle de asesoramiento entre las dos aplicaciones que permanecen en su lugar hasta que el cliente lo finaliza.

Hay dos tipos de bucles de aviso: "caliente" y "caliente". En un bucle de avisos en caliente, el servidor envía inmediatamente un identificador de datos que identifica el valor cambiado. En un bucle de avisos en caliente, el servidor notifica al cliente que el valor del elemento ha cambiado, pero no envía el identificador de datos hasta que el cliente lo solicita.

Un cliente puede solicitar un bucle de avisos rápidos con un servidor especificando el tipo de transacción [**\_ ADVSTART de XTYP**](xtyp-advstart.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Para solicitar un bucle de aviso automático, el cliente debe combinar la marca XTYPF NODATA con el tipo de transacción \_ **\_ XTYP ADVSTART.** En cualquier caso, DDEML pasa la transacción **\_ ADVSTART de XTYP** a la función de devolución de llamada datos dinámicos Exchange (DDE) del servidor. La función de devolución de llamada DDE del servidor debe examinar los parámetros que acompañan a la transacción **\_ ADVSTART de XTYP** (incluido el formato solicitado, el nombre del tema y el nombre del elemento) y, a continuación, devolver **TRUE** para permitir que el bucle advise o **FALSE** lo denieguen.

Una vez establecido un bucle de asesoramiento, la aplicación de servidor debe llamar a la función [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) cada vez que cambie el valor del elemento asociado al nombre de elemento solicitado. Esta llamada da como resultado que se envíe una transacción [**\_ ADBIZQ de XTYP**](xtyp-advreq.md) a la propia función de devolución de llamada DDE del servidor. La función de devolución de llamada DDE del servidor debe devolver un identificador de datos que identifique el nuevo valor del elemento de datos. A continuación, DDEML notifica al cliente que el elemento especificado ha cambiado mediante el envío de la transacción [**\_ ADVDATA de XTYP**](xtyp-advdata.md) a la función de devolución de llamada DDE del cliente.

Si el cliente solicitó un bucle de avisos en caliente, DDEML pasa el identificador de datos al elemento cambiado al cliente durante la transacción [**\_ ADVDATA de XTYP.**](xtyp-advdata.md) De lo contrario, el cliente puede enviar una [**transacción \_ XTYP REQUEST**](xtyp-request.md) para obtener el identificador de datos.

Es posible que un servidor envíe actualizaciones más rápido de lo que un cliente puede procesar los nuevos datos. La velocidad de las actualizaciones puede ser un problema para un cliente que debe realizar operaciones de procesamiento largas en los datos. En este caso, el cliente debe especificar la marca \_ XTYPF ACKREQ cuando solicite un bucle de aviso. Esta marca hace que el servidor espere a que el cliente confirme que ha recibido y procesado un elemento de datos antes de que el servidor envíe el siguiente elemento de datos. Los bucles de aviso que se establecen con la marca ACKREQ de XTYPF son más sólidos con servidores rápidos, pero en ocasiones pueden \_ perder actualizaciones. Se garantiza que los bucles de aviso establecidos sin la marca ACKREQ de XTYPF no pierdan las actualizaciones mientras el cliente se mantenga \_ al día con el servidor.

Un cliente puede finalizar un bucle de aviso especificando el tipo de transacción [**\_ XTYP ADVSTOP**](xtyp-advstop.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).

Si un servidor no admite bucles advise, debe especificar la marca de filtro CBF FAIL ADVISES en la \_ \_ función [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Esta marca impide que DDEML envíe las transacciones [**\_ ADVSTART**](xtyp-advstart.md) y [**\_ ADVSTOP de XTYP**](xtyp-advstop.md) al servidor.

## <a name="execute-transaction"></a>Ejecutar transacción

Un cliente puede usar la [**transacción \_ XTYP EXECUTE**](xtyp-execute.md) para hacer que un servidor ejecute un comando o una serie de comandos.

Para ejecutar un comando de servidor, el cliente crea primero un búfer que contiene una cadena de comandos para que el servidor ejecute y, a continuación, pasa un puntero al búfer o un identificador de datos que identifica el búfer cuando llama a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction). Otros parámetros necesarios incluyen el identificador de conversación, el identificador de cadena de nombre de elemento, la especificación de formato y el tipo de [**transacción \_ XTYP EXECUTE.**](xtyp-execute.md) Una aplicación que crea un identificador de datos para pasar datos de ejecución debe especificar **NULL** para el parámetro *hszItem* de la función [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) y cero para el *parámetro uFmt.*

DDEML pasa la transacción [**\_ XTYP EXECUTE**](xtyp-execute.md) a la función de devolución de llamada DDE del servidor y especifica el nombre de formato, el identificador de conversación, el nombre del tema y el identificador de datos que identifican la cadena de comando. Si el servidor admite el comando , debe usar la función [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obtener un puntero a la cadena de comando, ejecutar el comando y, a continuación, devolver DDE \_ FACK. Si el servidor no admite el comando o no puede completar la transacción, debe devolver DDE \_ FNOTPROCESSED. El servidor debe devolver DDE \_ FBUSY si está demasiado ocupado para completar la transacción.

En general, la función de devolución de llamada de un servidor debe procesar la [**transacción \_ XTYP EXECUTE**](xtyp-execute.md) antes de devolver con las siguientes excepciones:

1.  Cuando el comando pasado con la transacción [**\_ XTYP EXECUTE**](xtyp-execute.md) solicita al servidor que finalice, el servidor no debe finalizar hasta que su función de devolución de llamada devuelva del procesamiento **XTYP \_ EXECUTE**.
2.  Si el servidor debe realizar una operación, como procesar un cuadro de diálogo o una transacción DDE que podría causar problemas de recursión de DDEML, el servidor debe devolver el código de retorno CBR BLOCK para bloquear la transacción de ejecución, realizar la operación y reanudar el procesamiento de la transacción de \_ ejecución.

Cuando [**se devuelve DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) el cliente puede usar el *parámetro lpdwResult* para acceder a la marca de estado de transacción. Si la marca es DDE \_ FBUSY, el cliente debe volver a enviar la transacción más adelante.

Si un servidor no admite la transacción [**\_ XTYP EXECUTE,**](xtyp-execute.md) debe especificar la marca de filtro CBF FAIL EXECUTES en la \_ función \_ [**DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) Esto impide que DDEML envíe la transacción al servidor.

## <a name="synchronous-and-asynchronous-transactions"></a>Transacciones sincrónicas y asincrónicas

Un cliente puede enviar transacciones sincrónicas o asincrónicas. En una transacción sincrónica, el cliente especifica un valor de tiempo de espera que indica la cantidad máxima de tiempo que esperará a que el servidor procese la transacción. [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) no devuelve hasta que el servidor procesa la transacción, se produce un error en la transacción o expira el valor de tiempo de espera. El cliente especifica el valor de tiempo de espera cuando llama a **DdeClientTransaction.**

Durante una transacción sincrónica, el cliente entra en un bucle modal mientras espera a que se procese la transacción. El cliente todavía puede procesar la entrada del usuario, pero no puede enviar otra transacción sincrónica hasta que [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) devuelva .

Un cliente envía una transacción asincrónica especificando la marca TIMEOUT \_ ASYNC en [**DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) La función devuelve una vez iniciada la transacción, pasando un identificador de transacción al cliente. Cuando el servidor termina de procesar la transacción asincrónica, DDEML envía una transacción [**\_ XTYP XACT \_ COMPLETE**](xtyp-xact-complete.md) al cliente. Uno de los parámetros que DDEML pasa al cliente durante la transacción **\_ XTYP XACT \_ COMPLETE** es el identificador de transacción. Al comparar este identificador de transacción con el identificador devuelto por **DdeClientTransaction**, el cliente identifica la transacción asincrónica que el servidor ha terminado de procesar.

Un cliente puede usar la [**función DdeSetUserHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddesetuserhandle) como ayuda para procesar una transacción asincrónica. Esta función permite que un cliente asocie un valor definido por la aplicación con un identificador de conversación y un identificador de transacción. El cliente puede usar la función [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) durante la transacción [**\_ XTYP XACT \_ COMPLETE**](xtyp-xact-complete.md) para obtener el valor definido por la aplicación. Debido a esta función, una aplicación no necesita mantener una lista de identificadores de transacción activos.

Cuando un cliente completa correctamente una solicitud de datos mediante una transacción sincrónica, DDEML no tiene forma de saber cuándo el cliente ha terminado de usar los datos recibidos. La aplicación cliente debe pasar el identificador de datos recibido a la función [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) y notificar a la DDEML que el identificador ya no se usará. Los identificadores de datos devueltos por las transacciones sincrónicas son propiedad efectiva del cliente.

Si un servidor no procesa una transacción asincrónica de forma oportuna, el cliente puede abandonar la transacción llamando a la función [**DdeAbandoneTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeabandontransaction) DDEML libera todos los recursos asociados a la transacción y descarta los resultados de la transacción cuando el servidor termina de procesarla. Un tiempo de espera durante una transacción sincrónica cancela eficazmente la transacción.

El método de transacción asincrónica se proporciona para las aplicaciones que deben enviar un gran volumen de transacciones DDE al mismo tiempo que realizan una cantidad considerable de procesamiento, como realizar cálculos. El método asincrónico también es útil en aplicaciones que deben detener temporalmente el procesamiento de transacciones DDE para poder completar otras tareas sin interrupción. En la mayoría de las demás situaciones, una aplicación debe usar el método sincrónico.

Las transacciones sincrónicas son más fáciles de mantener y son más rápidas que las transacciones asincrónicas. Sin embargo, solo se puede realizar una transacción sincrónica a la vez, mientras que muchas transacciones asincrónicas se pueden realizar simultáneamente. Con las transacciones sincrónicas, un servidor lento puede hacer que un cliente permanezca inactivo mientras espera una respuesta. Además, las transacciones sincrónicas hacen que el cliente entre en un bucle modal que podría omitir el filtrado de mensajes en el propio bucle de mensajes de la aplicación.

Si el cliente ha instalado un procedimiento de enlace para filtrar mensajes (es decir, ha especificado el tipo de enlace MSGFILTER de WH en una llamada a la función \_ [**SetWindowsHookEx),**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) una transacción sincrónica no hará que el sistema omita el procedimiento de enlace. Cuando se produce un evento de entrada mientras el cliente espera a que finalice una transacción sincrónica, el procedimiento de enlace recibe un código de enlace \_ de MSGF DDEMGR. El peligro principal de usar un bucle modal de transacción sincrónica es que un bucle modal creado por un cuadro de diálogo puede interferir con su funcionamiento. Las transacciones asincrónicas siempre se deben usar cuando un archivo DLL usa la DDEML.

## <a name="transaction-control"></a>Control de transacciones

Una aplicación puede suspender las transacciones en su función de devolución de llamada de DDE, ya sea las transacciones asociadas a un identificador de conversación específico o todas las transacciones, independientemente del identificador de conversación. Esta funcionalidad es útil cuando una aplicación recibe una transacción que requiere un procesamiento largo. En tal caso, la aplicación puede devolver el código de retorno CBR BLOCK para suspender las transacciones futuras asociadas al identificador de conversación de la transacción, de modo que la aplicación pueda procesar \_ otras conversaciones.

Una vez completado el procesamiento, la aplicación llama a la función [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) para reanudar las transacciones asociadas a la conversación suspendida. Llamar **a DdeEnableCallback** hace que DDEML vuelva a enviar la transacción que provocó que la aplicación suspendiera la conversación. Por lo tanto, la aplicación debe almacenar el resultado de la transacción de forma que pueda obtener y devolver el resultado sin volver a procesar la transacción.

Una aplicación puede suspender todas las transacciones asociadas a un identificador de conversación específico especificando el identificador y la marca EC DISABLE en una llamada \_ a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Al especificar un identificador **NULL,** una aplicación puede suspender todas las transacciones de todas las conversaciones.

Cuando se ha suspendido una conversación, la DDEML guarda las transacciones de la conversación en una cola de transacciones. Cuando la aplicación vuelve aable la conversación, DDEML quita las transacciones guardadas de la cola y pasa cada transacción a la función de devolución de llamada adecuada. La capacidad de la cola de transacciones es grande, pero una aplicación debe volver a crear una conversación suspendida lo antes posible para evitar la pérdida de transacciones.

Una aplicación puede reanudar el procesamiento de transacciones habitual especificando la marca ENABLEALL de EC \_ en [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback). Para una reanudación más controlada del procesamiento de transacciones, la aplicación puede especificar la marca \_ ENABLEONE de EC. Esta marca quita una transacción de la cola de transacciones y la pasa a la función de devolución de llamada adecuada. Una vez procesada la transacción, las conversaciones se deshabilitan de nuevo.

Si la marca ENABLEONE de EC y un identificador de conversación se especifican en la llamada \_ a [**DdeEnableCallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback), solo esa conversación se bloquea una vez procesada la transacción. Si se **especifica un** identificador de conversación NULL, todas las conversaciones se bloquean después de que se haya procesado una transacción en cualquier conversación.

## <a name="transaction-classes"></a>Clases de transacción

DDEML tiene cuatro clases de transacciones. Cada clase se identifica mediante una constante que comienza con el prefijo \_ XCLASS. Las clases se definen en el archivo de encabezado DDEML. El valor de clase se combina con el valor de tipo de transacción y se pasa a la función de devolución de llamada DDE de la aplicación receptora.

La clase de una transacción determina el valor devuelto que se espera que devuelva una función de devolución de llamada si procesa la transacción. Los siguientes valores devueltos y tipos de transacción están asociados a cada una de las cuatro clases de transacción.



| Clase                | Valor devuelto                                                     | Transacción                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| XCLASS \_ BOOL         | **TRUE** o **FALSE**                                            | [**XTYP \_ ADVSTART**](xtyp-advstart.md)<br/> [**XTYP \_ CONNECT**](xtyp-connect.md)<br/>                                                                                                                                                                                                                                                                                            |
| DATOS \_ XCLASS         | Un identificador de datos, el código de retorno \_ CBR BLOCK o **NULL**           | [**XTYP \_ AD ESTAQ**](xtyp-advreq.md)<br/> [**SOLICITUD DE \_ XTYP**](xtyp-request.md)<br/> [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)<br/>                                                                                                                                                                                                                                       |
| MARCAS \_ XCLASS        | Marca de transacción: DDE \_ FACK, DDE \_ FBUSY o DDE \_ FNOTPROCESSED | [**XTYP \_ ADVDATA**](xtyp-advdata.md)<br/> [**XTYP \_ EXECUTE**](xtyp-execute.md)<br/> [**XTYP \_ VEZE**](xtyp-poke.md)<br/>                                                                                                                                                                                                                                                   |
| NOTIFICACIÓN \_ XCLASS | Ninguno                                                             | [**XTYP \_ ADVSTOP**](xtyp-advstop.md)<br/> [**CONFIRMACIÓN DE XTYP \_ \_ CONNECT**](xtyp-connect-confirm.md)<br/> [**XTYP \_ DISCONNECT**](xtyp-disconnect.md)<br/> [**ERROR DE XTYP \_**](xtyp-error.md)<br/> [**XTYP \_ REGISTER**](xtyp-register.md)<br/> [**ANULACIÓN DEL REGISTRO DE XTYP \_**](xtyp-unregister.md)<br/> [**XTYP \_ XACT \_ COMPLETE**](xtyp-xact-complete.md)<br/> |



 

## <a name="transaction-types"></a>Tipos de transacción

Cada tipo de transacción DDE tiene un receptor y una actividad asociada que hace que DDEML genere cada tipo.



| Tipo de transacción                                       | Receptor                   | Causa                                                                                                                                                                         |
|--------------------------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XTYP \_ ADVDATA**](xtyp-advdata.md)                  | Cliente                     | Un servidor respondió a una [**transacción \_ AD FTPQ de XTYP**](xtyp-advreq.md) devolviendo un identificador de datos.                                                                          |
| [**XTYP \_ AD ESTAQ**](xtyp-advreq.md)                    | Servidor                     | Un servidor denominado función [**DdePostAdvise,**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) que indica que ha cambiado el valor de un elemento de datos en un bucle advise.                                  |
| [**XTYP \_ ADVSTART**](xtyp-advstart.md)                | Servidor                     | Un cliente especificó el tipo de transacción [**\_ ADVSTART de XTYP**](xtyp-advstart.md) en una llamada a la [**función DdeClientTransaction.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)               |
| [**XTYP \_ ADVSTOP**](xtyp-advstop.md)                  | Servidor                     | Un cliente especificó el tipo de [**transacción \_ ADVSTOP de XTYP**](xtyp-advstop.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**XTYP \_ CONNECT**](xtyp-connect.md)                  | Servidor                     | Un cliente llamó a [**la función DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) y especificó un nombre de servicio y un nombre de tema admitidos por el servidor.                                            |
| [**CONFIRMACIÓN DE XTYP \_ \_ CONNECT**](xtyp-connect-confirm.md) | Servidor                     | El servidor devolvió **TRUE en** respuesta a una [**transacción XTYP \_ CONNECT**](xtyp-connect.md) o [**XTYP \_ WILDCONNECT.**](xtyp-wildconnect.md)                            |
| [**XTYP \_ DISCONNECT**](xtyp-disconnect.md)            | Cliente/servidor              | Un asociado de una conversación denominada función [**DdeDisconnect,**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) lo que hace que ambos asociados reciban esta transacción.                                    |
| [**ERROR DE XTYP \_**](xtyp-error.md)                      | Cliente/servidor              | Se ha producido un error crítico. Es posible que DDEML no tenga suficientes recursos para continuar.                                                                                       |
| [**XTYP \_ EXECUTE**](xtyp-execute.md)                  | Servidor                     | Un cliente especificó el [**tipo de transacción \_ XTYP EXECUTE**](xtyp-execute.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**MONITOR de \_ XTYP**](xtyp-monitor.md)                  | Aplicación de supervisión de DDE | Se produjo un evento DDE en el sistema. Para obtener más información sobre las aplicaciones de supervisión de DDE, vea [Supervisión de aplicaciones](monitoring-applications.md).                       |
| [**\_XTYPPTOE**](xtyp-poke.md)                        | Servidor                     | Un cliente especificó el tipo [**de transacción \_ XTYP FTPE**](xtyp-poke.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                                    |
| [**XTYP \_ REGISTER**](xtyp-register.md)                | Cliente/servidor              | Una aplicación de servidor usó la [**función DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) para registrar un nombre de servicio.                                                                   |
| [**SOLICITUD \_ XTYP**](xtyp-request.md)                  | Servidor                     | Un cliente especificó el tipo [**de transacción XTYP \_ REQUEST**](xtyp-request.md) en una llamada a [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction).                              |
| [**ANULACIÓN DEL REGISTRO DE XTYP \_**](xtyp-unregister.md)            | Cliente/servidor              | Una aplicación de servidor [**usó DdeNameService para**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) anular el registro de un nombre de servicio.                                                                              |
| [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md)          | Servidor                     | Un cliente llamado la [**función DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) o [**DdeConnectList,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnectlist) **especificando NULL** para el nombre del servicio, el nombre del tema o ambos. |
| [**XTYP \_ XACT \_ COMPLETE**](xtyp-xact-complete.md)     | Cliente                     | Una transacción asincrónica, enviada cuando el cliente especificó la marca TIMEOUT ASYNC en una llamada \_ a [**DdeClientTransaction,**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)ha finalizado.         |



 

 

