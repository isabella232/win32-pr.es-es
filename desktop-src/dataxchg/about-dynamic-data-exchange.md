---
title: Acerca de datos dinámicos Exchange
description: En este tema se describe la transferencia de datos entre aplicaciones.
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- datos dinámicos Exchange (DDE),about
- DDE (datos dinámicos Exchange),about
- intercambio de datos, datos dinámicos Exchange (DDE)
- datos dinámicos Exchange (DDE), vinculación a datos en tiempo real
- DDE (datos dinámicos Exchange), vinculación a datos en tiempo real
- datos dinámicos Exchange (DDE), crear documentos compuestos
- DDE (datos dinámicos Exchange), crear documentos compuestos
- datos dinámicos Exchange (DDE), consultas de datos
- DDE (datos dinámicos Exchange), consultas de datos
- datos dinámicos Exchange (DDE),examples
- DDE (datos dinámicos Exchange),ejemplos
- datos dinámicos Exchange (DDE),suplantación
- DDE (datos dinámicos Exchange), suplantación
- datos dinámicos Exchange (DDE),messages
- DDE (datos dinámicos Exchange),messages
- datos dinámicos Exchange (DDE),atoms
- DDE (datos dinámicos Exchange),atoms
- datos dinámicos Exchange (DDE), objetos de memoria compartida
- DDE (datos dinámicos Exchange), objetos de memoria compartida
- datos dinámicos Exchange (DDE), funciones de empaquetado de parámetros
- DDE (datos dinámicos Exchange), funciones de empaquetado de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d38574e9182255e8f6761520aea60575d8affbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070357"
---
# <a name="about-dynamic-data-exchange"></a>Acerca de datos dinámicos Exchange

Windows proporciona varios métodos para transferir datos entre aplicaciones. Un método consiste en usar el protocolo datos dinámicos Exchange (DDE). El protocolo DDE es un conjunto de mensajes e instrucciones. Envía mensajes entre aplicaciones que comparten datos y usa memoria compartida para intercambiar datos entre aplicaciones. Las aplicaciones pueden usar el protocolo DDE para las transferencias de datos de un solo uso y para los intercambios continuos en los que las aplicaciones envían actualizaciones entre sí a medida que los nuevos datos están disponibles.

Windows también admite la biblioteca datos dinámicos Exchange Management Library (DDEML). DDEML es una biblioteca de vínculos dinámicos (DLL) que las aplicaciones pueden usar para compartir datos. DDEML proporciona funciones y mensajes que simplifican la tarea de agregar funcionalidad DDE a una aplicación. En lugar de enviar, publicar y procesar mensajes DDE directamente, una aplicación usa las funciones de DDEML para administrar las conversaciones de DDE. (Una conversación de DDE es la interacción entre las aplicaciones cliente y servidor).

DDEML también proporciona una facilidad para administrar las cadenas y los datos que comparten las aplicaciones DDE. En lugar de usar átomos y punteros a objetos de memoria compartida, las aplicaciones DDE crean e intercambian identificadores de cadena, que identifican cadenas y identificadores de datos, que identifican objetos de memoria. DDEML también permite que una aplicación de servidor registre los nombres de servicio que admite. Los nombres se difunden a otras aplicaciones del sistema, que pueden usar los nombres para conectarse al servidor. Además, DDEML garantiza la compatibilidad entre las aplicaciones DDE al obligarlas a implementar el protocolo DDE de forma coherente.

Las aplicaciones existentes que usan el protocolo DDE basado en mensajes son totalmente compatibles con las que usan DDEML. Es decir, una aplicación que usa DDE basado en mensajes puede establecer conversaciones y realizar transacciones con aplicaciones que usan DDEML. Debido a las muchas ventajas de DDEML, las nuevas aplicaciones deben usarla en lugar de los mensajes DDE. Para usar los elementos de API de DDEML, debe incluir el archivo de encabezado DDEML en los archivos de origen, vincular con la biblioteca DDEML y asegurarse de que la biblioteca de vínculos dinámicos de DDEML se encuentra en la ruta de acceso de búsqueda del sistema.

En esta sección se tratan los temas siguientes.

-   [datos dinámicos Exchange protocolo](#dynamic-data-exchange-protocol)
-   [Usos para Windows datos dinámicos Exchange](#uses-for-windows-dynamic-data-exchange)
-   [datos dinámicos Exchange desde el punto de vista del usuario](#dynamic-data-exchange-from-the-users-point-of-view)
-   [datos dinámicos Exchange conceptos](#dynamic-data-exchange-concepts)
    -   [Cliente, servidor y conversación](#client-server-and-conversation)
    -   [Nombres de aplicación, tema y elemento](#application-topic-and-item-names)
    -   [Tema del sistema](#the-system-topic)
    -   [Vínculos de datos permanentes](#permanent-data-links)
    -   [Atoms y objetos de memoria compartida](#atoms-and-shared-memory-objects)
-   [datos dinámicos Exchange información general sobre mensajes](#dynamic-data-exchange-messages-overview)
-   [datos dinámicos Exchange mensaje Flow](#dynamic-data-exchange-message-flow)
-   [Funciones de empaquetado de parámetros](#parameter-packing-functions)
-   [datos dinámicos Exchange y suplantación](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>datos dinámicos Exchange protocolo

Dado Windows una arquitectura basada en mensajes, pasar mensajes es el método más adecuado para transferir automáticamente información entre aplicaciones. Sin embargo, los mensajes contienen solo dos parámetros *(wParam* *y lParam)* para pasar datos. Como resultado, estos parámetros deben hacer referencia indirectamente a otros fragmentos de datos cuando pasan más de unas pocas palabras de información entre aplicaciones. El protocolo DDE define exactamente cómo las aplicaciones deben usar los parámetros *wParam* e *lParam* para pasar fragmentos de datos más grandes por medio de átomos globales y identificadores de memoria compartida. El protocolo DDE tiene reglas específicas para asignar y eliminar átomos globales y objetos de memoria compartida.

Un atom global es una referencia a una cadena de caracteres. En el protocolo DDE, los átomos identifican las aplicaciones que intercambian datos, la naturaleza de los datos que se intercambian y los propios elementos de datos. Para obtener más información sobre los átomos, vea [Acerca de los átomos.](about-atom-tables.md)

## <a name="uses-for-windows-dynamic-data-exchange"></a>Usos para Windows datos dinámicos Exchange

DDE es más adecuado para los intercambios de datos que no requieren la interacción continua del usuario. Normalmente, una aplicación proporciona un método para que el usuario establezca el vínculo entre las aplicaciones que intercambian datos. Sin embargo, una vez establecido ese vínculo, las aplicaciones intercambian datos sin más intervención del usuario.

DDE se puede usar para implementar una amplia gama de características de aplicación, por ejemplo:

-   Vinculación a datos en tiempo real, como las actualizaciones de la bolsa, los instrumento científicos o el control de procesos.
-   Crear documentos compuestos, como un documento de procesamiento de texto que incluye un gráfico generado por una aplicación de gráficos. Con DDE, el gráfico cambiará cuando se cambien los datos de origen, mientras que el resto del documento seguirá siendo el mismo.
-   Realizar consultas de datos entre aplicaciones, como una hoja de cálculo que consulta una base de datos para las cuentas que se han debido.

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>datos dinámicos Exchange desde el punto de vista del usuario

En el ejemplo siguiente se muestra cómo pueden colaborar dos aplicaciones DDE, como se ve desde el punto de vista del usuario.

Un usuario de hoja de cálculo quiere usar Microsoft Excel para realizar un seguimiento del precio de una acción determinada en el mercado de valores de Nueva York Exchange. El usuario tiene una aplicación denominada Quote que, a su vez, tiene acceso a los datos de NYSE. La conversación de DDE entre Excel y Quote tiene lugar de la siguiente manera:

-   El usuario inicia la conversación suministrando el nombre de la aplicación (Quote) que suministrará los datos y el tema de interés concreto (NYSE). La conversación DDE resultante se usa para solicitar comillas en acciones específicas.
-   Excel los nombres de aplicación y tema a todas las aplicaciones DDE que se ejecutan actualmente en el sistema. La cita responde, estableciendo una conversación con Excel sobre el tema de NYSE.
-   A continuación, el usuario puede crear una fórmula de hoja de cálculo en una celda que solicite que la hoja de cálculo se actualice automáticamente cada vez que cambie una oferta de acciones determinada. Por ejemplo, el usuario podría solicitar una actualización automática cada vez que se produzca un cambio en el precio de venta de las acciones de ZAXX especificando la siguiente fórmula Excel: ='Quote' \| 'NYSE'! ZAXX
-   El usuario puede finalizar la actualización automática de la cotización de acciones de ZAXX en cualquier momento. Otros vínculos de datos que se establecieron por separado (por ejemplo, para las citas de otras acciones) seguirán activos en la misma conversación de NYSE.
-   El usuario también puede finalizar toda la conversación entre Excel y Quote en el tema NYSE, de modo que no se pueda establecer ningún vínculo de datos específico en ese tema sin iniciar una nueva conversación.

## <a name="dynamic-data-exchange-concepts"></a>datos dinámicos Exchange conceptos

En las secciones siguientes se explican los conceptos y terminología importantes que son clave para comprender el intercambio dinámico de datos.

-   [Cliente, servidor y conversación](#client-server-and-conversation)
-   [Nombres de aplicación, tema y elemento](#application-topic-and-item-names)
-   [Tema del sistema](#the-system-topic)
-   [Vínculos de datos permanentes](#permanent-data-links)
-   [Atoms y objetos de memoria compartida](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>Cliente, servidor y conversación

Se dice que dos aplicaciones que participan en DDE participan en una conversación de DDE. La aplicación que inicia la conversación es la aplicación cliente DDE; la aplicación que responde al cliente es la aplicación de servidor DDE. Una aplicación puede participar en varias conversaciones al mismo tiempo, actuando como el cliente en algunas y como servidor en otras.

Una conversación de DDE tiene lugar entre dos ventanas, una para cada una de las aplicaciones participantes. Una ventana puede ser la ventana principal de la aplicación; una ventana asociada a un documento específico, como en una aplicación de interfaz de varios documentos (MDI); o una ventana oculta (invisible) cuyo único propósito es procesar mensajes DDE.

Puesto que una conversación de DDE se identifica mediante el par de identificadores de las ventanas que participan en la conversación, no se debe incluir ninguna ventana en más de una conversación con otra ventana. La aplicación cliente o la aplicación de servidor deben proporcionar una ventana diferente para cada una de sus conversaciones con un servidor o aplicación cliente determinados.

Una aplicación puede garantizar que un par de ventanas de cliente y servidor nunca participan en más de una conversación mediante la creación de una ventana oculta para cada conversación. El único propósito de esta ventana es procesar mensajes DDE.

### <a name="application-topic-and-item-names"></a>Nombres de aplicación, tema y elemento

El protocolo DDE identifica las unidades de datos que se pasan entre el cliente y el servidor con una jerarquía de tres niveles de nombres de aplicación, tema y elemento.

Cada conversación de DDE se define de forma única por el nombre y el tema de la aplicación. Al principio de una conversación de DDE, el cliente y el servidor determinan el nombre y el tema de la aplicación. El nombre de la aplicación suele ser el nombre de la aplicación de servidor. Por ejemplo, cuando Excel como servidor en una conversación, el nombre de la aplicación se Excel.

El tema DDE es una clasificación general de los datos en los que se pueden "analizar" (intercambiar) varios elementos de datos durante la conversación. Para las aplicaciones que operan en documentos basados en archivos, el tema suele ser un nombre de archivo. Para otras aplicaciones, el tema es un nombre específico de la aplicación.

Dado que los identificadores de ventana cliente y servidor identifican juntas una conversación de DDE, el nombre de la aplicación y el tema que definen una conversación no se pueden cambiar durante el transcurso de la conversación.

Un elemento de datos DDE es información relacionada con el tema de conversación intercambiado entre las aplicaciones. Los valores del elemento de datos se pueden pasar desde el servidor al cliente o desde el cliente al servidor. Los datos se pueden pasar con cualquiera de los formatos estándar del Portapapeles o con un formato registrado del Portapapeles. Un formato especial registrado denominado Link identifica un elemento de una conversación de DDE. Para obtener más información sobre los formatos del Portapapeles, vea [Portapapeles.](clipboard.md)

### <a name="the-system-topic"></a>El tema del sistema

Las aplicaciones deben admitir el tema del sistema en todo momento. En este tema se proporciona un contexto para la información que puede ser de interés general para otra aplicación.

Los valores de elemento de datos deben representarse en el formato [**del Portapapeles CF \_ TEXT.**](standard-clipboard-formats.md) Los elementos individuales de los valores de elemento de un tema del sistema deben delimitarse por caracteres de tabulación. En la tabla siguiente se sugieren algunos elementos para el tema del sistema.



| Elemento          | Descripción                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formatos       | Lista delimitada por tabulaciones de formatos del Portapapeles que la aplicación puede representar. Normalmente, **\_ los formatos cf** se muestran con la parte **"CF" \_** de los nombres quitados (por ejemplo, **CF \_ TEXT** aparece como **"TEXT").**                                                                                        |
| Ayuda          | Texto que explica brevemente cómo usar el servidor DDE.                                                                                                                                                                                                                                                   |
| ReturnMessage | Detalles de compatibilidad para el mensaje [**wm \_ DDE \_ ACK usado más**](wm-dde-ack.md) recientemente. Este elemento es útil cuando se requieren más de ocho bits de datos devueltos específicos de la aplicación.                                                                                                                |
| Status        | Indicación del estado actual de la aplicación. Cuando un servidor recibe un mensaje [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) para este elemento de tema del sistema, debe responder publicando un mensaje [**WM \_ DDE \_ DATA**](wm-dde-data.md) con una cadena que contenga Busy o Ready, según corresponda. |
| SysItems      | Lista de elementos del tema del sistema que admite la aplicación.                                                                                                                                                                                                                                                    |
| TopicItemList | Similar al elemento SysItems, excepto que TopicItemList debe ser compatible con cada tema distinto del tema del sistema. Esto permite examinar los elementos admitidos en cualquier tema. Si no se pueden enumerar los elementos, este elemento solo debe contener "TopicItemList".                                  |
| Temas        | Lista de temas que la aplicación admite en el momento actual; esta lista puede variar de un momento a otro.                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>Vínculos de datos permanentes

Una vez iniciada una conversación de DDE, el cliente puede establecer uno o varios vínculos de datos permanentes con el servidor. Un vínculo de datos es un mecanismo de comunicaciones por el que el servidor notifica al cliente cada vez que cambia el valor de un elemento de datos especificado. El vínculo de datos es permanente en el sentido de que este proceso de notificación continúa hasta que finaliza el vínculo de datos o la propia conversación de DDE.

Hay dos tipos de vínculos de datos DDE permanentes: warm y hot. En un vínculo de datos en caliente, el servidor notifica al cliente que el valor del elemento de datos ha cambiado, pero el servidor no envía el valor de datos al cliente hasta que el cliente lo solicita. En un vínculo de datos de acceso directo, el servidor envía inmediatamente el valor de datos modificado al cliente.

Las aplicaciones que admiten vínculos de  datos en  caliente o de acceso rápido suelen proporcionar un comando Copiar o pegar vínculo en su menú Editar para permitir al usuario establecer vínculos entre aplicaciones. 

### <a name="atoms-and-shared-memory-objects"></a>Átomos y objetos de memoria compartida

Algunos argumentos de los mensajes DDE son átomos globales u objetos de memoria compartida. Las aplicaciones que usan estos argumentos deben seguir reglas explícitas sobre cuándo asignarlas y eliminarlas. En todos los casos, el remitente del mensaje debe eliminar cualquier átomo o objeto de memoria compartida que el receptor previsto no recibirá debido a una condición de error, como un error de la [**función PostMessage.**](/windows/desktop/api/winuser/nf-winuser-postmessagea)

DDE usa objetos de memoria compartida para tres propósitos:

-   Para llevar un valor de elemento de datos que se va a intercambiar. Se trata de un elemento al que hace referencia el *parámetro hData* en los mensajes [**WM \_ DDE \_ DATA**](wm-dde-data.md) y [**WM \_ DDE \_ SOAPE.**](wm-dde-poke.md)
-   Para llevar opciones en un mensaje. Se trata de un elemento al que hace referencia el *parámetro hOptions* en un [**mensaje \_ DDE ADVISE \_ de WM.**](wm-dde-advise.md)
-   Para llevar una cadena de ejecución de comandos. Se trata de un elemento al que hace referencia el *parámetro hCommands* en el mensaje [**EXECUTE de WM \_ DDE \_**](wm-dde-execute.md) y su mensaje [**\_ DDE \_ ACK**](wm-dde-ack.md) de WM correspondiente.

Una aplicación que recibe un objeto de memoria compartida DDE debe tratarlo como de solo lectura. La aplicación no debe usar el objeto como un área de lectura y escritura mutua para el intercambio libre de datos.

Al igual que con un átomo DDE, una aplicación debe liberar un objeto de memoria compartida para administrar la memoria de forma eficaz. La aplicación también debe bloquear y desbloquear objetos de memoria.

## <a name="dynamic-data-exchange-messages-overview"></a>datos dinámicos Exchange información general sobre mensajes

Dado que DDE es un protocolo basado en mensajes, no emplea funciones ni bibliotecas. Todas las transacciones de DDE se realizan pasando determinados mensajes DDE definidos entre las ventanas de cliente y servidor.

Hay nueve mensajes DDE; Las constantes simbólicas de estos mensajes se definen en el archivo de encabezado DDE. En este archivo de encabezado también se definen ciertas estructuras para los distintos mensajes DDE.

En la tabla siguiente se resumen los mensajes DDE.



| Message                                        | Descripción                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ ACK**](wm-dde-ack.md)             | Confirma la recepción o no recepción de un mensaje.                                                                                               |
| [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)       | Solicita a la aplicación de servidor que proporcione una actualización o notificación para un elemento de datos cada vez que cambie. Esto establece un vínculo de datos permanente. |
| [**WM \_ DDE \_ DATA**](wm-dde-data.md)           | Envía un valor de elemento de datos a la aplicación cliente.                                                                                               |
| [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)     | Envía una cadena a la aplicación de servidor, que se espera que procese la cadena como una serie de comandos.                                       |
| [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)   | Inicia una conversación entre las aplicaciones cliente y servidor.                                                                             |
| [**WM \_ DDE \_ POKE**](wm-dde-poke.md)           | Envía un valor de elemento de datos a la aplicación de servidor.                                                                                               |
| [**SOLICITUD \_ DDE de WM \_**](wm-dde-request.md)     | Solicita a la aplicación de servidor que proporcione el valor de un elemento de datos.                                                                             |
| [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) | Finaliza una conversación.                                                                                                                       |
| [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)   | Finaliza un vínculo de datos permanente.                                                                                                                |



 

Una aplicación llama a [**SendMessage para**](/windows/desktop/api/winuser/nf-winuser-sendmessage) emitir el mensaje WM DDE INITIATE o un mensaje wm [**\_ \_ DDE**](wm-dde-initiate.md) [**\_ \_ ACK**](wm-dde-ack.md) enviado en respuesta a **WM \_ DDE \_ INITIATE.** PostMessage envía todos los demás [**mensajes.**](/windows/desktop/api/winuser/nf-winuser-postmessagea) El primer parámetro de estas llamadas es un identificador para la ventana de recepción; el segundo parámetro contiene el mensaje que se va a enviar; el tercer parámetro identifica la ventana de envío; y el cuarto parámetro contiene los argumentos específicos del mensaje.

## <a name="dynamic-data-exchange-message-flow"></a>datos dinámicos Exchange message Flow

Una conversación de DDE típica consta de los siguientes eventos:

1.  La aplicación cliente inicia la conversación y la aplicación de servidor responde.
2.  Las aplicaciones intercambian datos por cualquiera de los métodos siguientes o por todos ellos:
    -   -   La aplicación de servidor envía datos al cliente a petición del cliente.
        -   La aplicación cliente envía datos no solicitados a la aplicación de servidor.
        -   La aplicación cliente solicita a la aplicación de servidor que notifique al cliente cada vez que cambia un elemento de datos (vínculo de datos en caliente).
        -   La aplicación cliente solicita a la aplicación de servidor que envíe datos cada vez que cambien los datos (vínculo de datos en caliente).
        -   La aplicación de servidor lleva a cabo un comando a petición del cliente.

3.  La aplicación cliente o servidor finaliza la conversación.

Una ventana de aplicación que procesa las solicitudes de un cliente o servidor debe procesarlas estrictamente en el orden en que se reciben.

Un cliente puede establecer conversaciones con más de un servidor; un servidor puede tener conversaciones con más de un cliente. Al controlar mensajes de más de un origen, un cliente o servidor debe procesar los mensajes de una conversación sincrónicamente, pero no es necesario procesar todos los mensajes de forma sincrónica. En otras palabras, puede cambiar de una conversación a otra según sea necesario.

Si una aplicación no puede procesar una solicitud entrante porque está esperando una respuesta DDE, debe evitar el interbloqueo mediante la publicación de un mensaje [**wm \_ DDE \_ ACK**](wm-dde-ack.md) con el miembro **fBusy** de la estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) establecido en 1. Una aplicación también puede enviar un mensaje **wm \_ DDE \_ ACK** ocupado si, por cualquier motivo, no puede procesar una solicitud entrante en un período de tiempo razonable.

Una aplicación debe ser capaz de controlar el error de un cliente o servidor para responder a un mensaje en un momento determinado. Dado que el intervalo de tiempo de espera puede variar según la naturaleza de la aplicación y la configuración del sistema del usuario (incluido si está conectado a una red), la aplicación debe proporcionar una manera de que el usuario especifique el intervalo.

## <a name="parameter-packing-functions"></a>Funciones de empaquetado de parámetros

El *parámetro lParam* de muchos mensajes DDE contiene dos fragmentos de datos. Por ejemplo, *el lParam* del mensaje [**WM \_ DDE \_ DATA**](wm-dde-data.md) contiene un identificador de datos y un átomo. Las aplicaciones deben usar la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) para empaquetar el identificador y el átomo en un parámetro *lParam* y la función [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) para quitar los valores. Las aplicaciones DDE deben **usar PackDDElParam** y **UnpackDDElParam** para todos los mensajes publicados durante una conversación de DDE.

Las aplicaciones también pueden usar [**las funciones ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) [**y FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam) **ReuseDDElParam** permite que una aplicación DDE reutilice un parámetro *lParam* empaquetado, lo que ayuda a reducir el número de reasignaciones de memoria que la aplicación debe realizar durante una conversación. Una aplicación puede usar **FreeDDElParam para** liberar la memoria asociada a un identificador de datos recibido durante una conversación de DDE.

## <a name="dynamic-data-exchange-and-impersonation"></a>datos dinámicos Exchange y suplantación

Para permitir que un servidor suplante a un cliente, el cliente llama a la función [**DdeSetQualityOfService.**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) La [**estructura SECURITY \_ IMPERSONATION \_ LEVEL**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level) se usa para controlar el nivel de suplantación que puede realizar el servidor.

Un servidor DDE puede suplantar a un cliente DDE llamando a [**la función ImpersonateDdeClientWindow.**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) Un servidor DDEML debe usar la [**función DdeImpersonateClient.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient)

 

 