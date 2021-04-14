---
title: Acerca de Intercambio dinámico de datos
description: En este tema se describe la transferencia de datos entre aplicaciones.
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- Intercambio dinámico de datos (DDE), acerca de
- DDE (Intercambio dinámico de datos), acerca de
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), vincular a datos en tiempo real
- DDE (Intercambio dinámico de datos), vincular a datos en tiempo real
- Intercambio dinámico de datos (DDE), crear documentos compuestos
- DDE (Intercambio dinámico de datos), crear documentos compuestos
- Intercambio dinámico de datos (DDE), consultas de datos
- DDE (Intercambio dinámico de datos), consultas de datos
- Intercambio dinámico de datos (DDE), ejemplos
- DDE (Intercambio dinámico de datos), ejemplos
- Intercambio dinámico de datos (DDE), suplantación
- DDE (Intercambio dinámico de datos), suplantación
- Intercambio dinámico de datos (DDE), mensajes
- DDE (Intercambio dinámico de datos), mensajes
- Intercambio dinámico de datos (DDE), átomos
- DDE (Intercambio dinámico de datos), átomos
- Intercambio dinámico de datos (DDE), objetos de memoria compartida
- DDE (Intercambio dinámico de datos), objetos de memoria compartida
- Intercambio dinámico de datos (DDE), funciones de empaquetado de parámetros
- DDE (Intercambio dinámico de datos), funciones de empaquetado de parámetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d38574e9182255e8f6761520aea60575d8affbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421213"
---
# <a name="about-dynamic-data-exchange"></a>Acerca de Intercambio dinámico de datos

Windows proporciona varios métodos para transferir datos entre aplicaciones. Un método es usar el protocolo Intercambio dinámico de datos (DDE). El protocolo DDE es un conjunto de mensajes e instrucciones. Envía mensajes entre aplicaciones que comparten datos y usa la memoria compartida para intercambiar datos entre aplicaciones. Las aplicaciones pueden usar el protocolo DDE para las transferencias de datos de un solo uso y para los intercambios continuos en los que las aplicaciones envían actualizaciones entre sí a medida que hay nuevos datos disponibles.

Windows también es compatible con la biblioteca de administración de Intercambio dinámico de datos (DDEML). El archivo DDEML es una biblioteca de vínculos dinámicos (DLL) que las aplicaciones pueden usar para compartir datos. DDEML proporciona funciones y mensajes que simplifican la tarea de agregar funcionalidad DDE a una aplicación. En lugar de enviar, publicar y procesar directamente los mensajes DDE, una aplicación utiliza las funciones DDEML para administrar las conversaciones DDE. (Una conversación DDE es la interacción entre las aplicaciones cliente y servidor).

DDEML también proporciona una utilidad para administrar las cadenas y los datos que comparten las aplicaciones DDE. En lugar de usar átomos y punteros a objetos de memoria compartida, las aplicaciones DDE crean e intercambian los identificadores de cadena, que identifican cadenas, y los identificadores de datos, que identifican los objetos de memoria. El DDEML también hace posible que una aplicación de servidor registre los nombres de servicio que admite. Los nombres se difunden a otras aplicaciones del sistema, que pueden usar los nombres para conectarse al servidor. Además, el DDEML garantiza la compatibilidad entre las aplicaciones DDE obligando a implementar el protocolo DDE de una manera coherente.

Las aplicaciones existentes que utilizan el protocolo DDE basado en mensajes son totalmente compatibles con las que usan DDEML. Es decir, una aplicación que utiliza DDE basado en mensajes puede establecer conversaciones y realizar transacciones con aplicaciones que usan el DDEML. Debido a las numerosas ventajas de DDEML, las nuevas aplicaciones deben utilizarla en lugar de los mensajes DDE. Para usar los elementos de la API de DDEML, debe incluir el archivo de encabezado DDEML en los archivos de código fuente, vincular con la biblioteca DDEML y asegurarse de que la biblioteca de vínculos dinámicos DDEML está en la ruta de acceso de búsqueda del sistema.

Los temas siguientes se describen en esta sección.

-   [Protocolo Intercambio dinámico de datos](#dynamic-data-exchange-protocol)
-   [Usos de Windows Intercambio dinámico de datos](#uses-for-windows-dynamic-data-exchange)
-   [Intercambio dinámico de datos desde el punto de vista del usuario](#dynamic-data-exchange-from-the-users-point-of-view)
-   [Conceptos de Intercambio dinámico de datos](#dynamic-data-exchange-concepts)
    -   [Cliente, servidor y conversación](#client-server-and-conversation)
    -   [Nombres de aplicación, tema y elemento](#application-topic-and-item-names)
    -   [El tema sistema](#the-system-topic)
    -   [Vínculos de datos permanentes](#permanent-data-links)
    -   [Átomos y objetos de memoria compartida](#atoms-and-shared-memory-objects)
-   [Información general sobre mensajes de Intercambio dinámico de datos](#dynamic-data-exchange-messages-overview)
-   [Intercambio dinámico de datos flujo de mensajes](#dynamic-data-exchange-message-flow)
-   [Funciones de empaquetado de parámetros](#parameter-packing-functions)
-   [Intercambio dinámico de datos y suplantación](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>Protocolo Intercambio dinámico de datos

Dado que Windows tiene una arquitectura basada en mensajes, el paso de mensajes es el método más adecuado para la transferencia automática de información entre aplicaciones. Sin embargo, los mensajes contienen solo dos parámetros (*wParam* y *lParam*) para pasar datos. Como resultado, estos parámetros deben hacer referencia indirectamente a otros fragmentos de datos cuando se superan algunas palabras de información entre aplicaciones. El protocolo DDE define exactamente el modo en que las aplicaciones deben usar los parámetros *wParam* e *lParam* para pasar partes más grandes de datos por medio de átomos globales y controladores de memoria compartida. El protocolo DDE tiene reglas específicas para asignar y eliminar átomos globales y objetos de memoria compartida.

Un átomo global es una referencia a una cadena de caracteres. En el protocolo DDE, los átomos identifican las aplicaciones que intercambian datos, la naturaleza de los datos que se intercambian y los propios elementos de datos. Para obtener más información acerca de los átomos, vea acerca de los [átomos](about-atom-tables.md).

## <a name="uses-for-windows-dynamic-data-exchange"></a>Usos de Windows Intercambio dinámico de datos

El DDE es más adecuado para los intercambios de datos que no requieren la interacción continua del usuario. Normalmente, una aplicación proporciona un método para que el usuario establezca el vínculo entre las aplicaciones que intercambian datos. Sin embargo, una vez establecido el vínculo, las aplicaciones intercambian datos sin la intervención del usuario.

DDE se puede usar para implementar una amplia gama de características de la aplicación, por ejemplo:

-   Vinculación a datos en tiempo real, como las actualizaciones del mercado de acciones, los instrumentos científicos o el control del proceso.
-   Crear documentos compuestos, como un documento de procesamiento de texto que incluye un gráfico generado por una aplicación de gráficos. Con DDE, el gráfico cambiará cuando se cambien los datos de origen, mientras que el resto del documento seguirá siendo el mismo.
-   Realizar consultas de datos entre aplicaciones, como una hoja de cálculo que consulta una base de datos para las cuentas vencidas.

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>Intercambio dinámico de datos desde el punto de vista del usuario

En el ejemplo siguiente se muestra cómo pueden cooperar dos aplicaciones DDE, tal como se muestra en el punto de vista del usuario.

Un usuario de hoja de cálculo desea usar Microsoft Excel para realizar el seguimiento del precio de una acción determinada en la bolsa de valores de Nueva York. El usuario tiene una aplicación denominada quote que, a su vez, tiene acceso a los datos de NYSE. La conversación DDE entre Excel y quote tiene lugar de la siguiente manera:

-   El usuario inicia la conversación proporcionando el nombre de la aplicación (oferta) que proporcionará los datos y el tema concreto de interés (NYSE). La conversación DDE resultante se usa para solicitar ofertas en acciones específicas.
-   Excel difunde los nombres de aplicación y tema a todas las aplicaciones DDE que se ejecutan actualmente en el sistema. La oferta responde y establece una conversación con Excel sobre el tema NYSE.
-   A continuación, el usuario puede crear una fórmula de hoja de cálculo en una celda que solicite que la hoja de cálculo se actualice automáticamente cada vez que cambie una cotización bursátil determinada. Por ejemplo, el usuario podría solicitar una actualización automática cada vez que se produzca un cambio en el precio de venta de ZAXX stock especificando la siguiente fórmula de Excel: = ' quote ' \| ' NYSE '! ZAXX
-   El usuario puede finalizar la actualización automática de la cotización de acciones de ZAXX en cualquier momento. Otros vínculos de datos que se establecieron por separado (por ejemplo, para las cotizaciones de otros materiales) seguirán estando activos en la misma conversación NYSE.
-   El usuario también puede finalizar la conversación completa entre Excel y quote en el tema NYSE, de modo que no se pueda establecer ningún vínculo de datos específico en ese tema sin iniciar una conversación nueva.

## <a name="dynamic-data-exchange-concepts"></a>Conceptos de Intercambio dinámico de datos

En las secciones siguientes se explican los conceptos y la terminología importantes que son fundamentales para comprender el intercambio dinámico de datos.

-   [Cliente, servidor y conversación](#client-server-and-conversation)
-   [Nombres de aplicación, tema y elemento](#application-topic-and-item-names)
-   [El tema sistema](#the-system-topic)
-   [Vínculos de datos permanentes](#permanent-data-links)
-   [Átomos y objetos de memoria compartida](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>Cliente, servidor y conversación

Se dice que dos aplicaciones que participan en DDE están dedicadas a una conversación DDE. La aplicación que inicia la conversación es la aplicación cliente DDE; la aplicación que responde al cliente es la aplicación de servidor DDE. Una aplicación puede participar en varias conversaciones al mismo tiempo, actuando como el cliente en algunos y como el servidor en otros.

Una conversación DDE se realiza entre dos ventanas, una para cada una de las aplicaciones participantes. Una ventana puede ser la ventana principal de la aplicación; ventana asociada a un documento concreto, como en una aplicación de interfaz de múltiples documentos (MDI). o una ventana oculta (invisible) cuyo único propósito es procesar los mensajes DDE.

Dado que una conversación DDE se identifica mediante el par de identificadores para las ventanas configuradas en la conversación, no se debe usar ninguna ventana en más de una conversación con otra ventana. Tanto la aplicación cliente como la aplicación de servidor deben proporcionar una ventana diferente para cada una de sus conversaciones con una aplicación de servidor o cliente determinada.

Una aplicación puede garantizar que un par de ventanas de cliente y de servidor nunca participa en más de una conversación creando una ventana oculta para cada conversación. El único propósito de esta ventana es procesar los mensajes DDE.

### <a name="application-topic-and-item-names"></a>Nombres de aplicación, tema y elemento

El protocolo DDE identifica las unidades de datos que se pasan entre el cliente y el servidor con una jerarquía de tres niveles de nombres de aplicación, tema y elemento.

Cada conversación DDE se define de forma única mediante el nombre de la aplicación y el tema. Al principio de una conversación DDE, el cliente y el servidor determinan el nombre de la aplicación y el tema. Normalmente, el nombre de la aplicación es el nombre de la aplicación de servidor. Por ejemplo, cuando Excel actúa como el servidor en una conversación, el nombre de la aplicación es Excel.

El tema DDE es una clasificación general de los datos en los que se pueden "discutir" (intercambiar) varios elementos de datos durante la conversación. En el caso de las aplicaciones que operan en documentos basados en archivos, el tema suele ser un nombre de archivo. Para otras aplicaciones, el tema es un nombre específico de la aplicación.

Dado que la ventana de cliente y de servidor se encarga de identificar conjuntamente una conversación DDE, el nombre de la aplicación y el tema que definen una conversación no se pueden cambiar durante el transcurso de la conversación.

Un elemento de datos DDE es información relacionada con el tema de conversación intercambiado entre las aplicaciones. Los valores para el elemento de datos se pueden pasar desde el servidor al cliente o desde el cliente al servidor. Los datos se pueden pasar con cualquiera de los formatos de Portapapeles estándar o con un formato de Portapapeles registrado. Un formato registrado especial denominado Link identifica un elemento en una conversación DDE. Para obtener más información sobre los formatos del portapapeles, vea [portapapeles](clipboard.md).

### <a name="the-system-topic"></a>El tema sistema

Las aplicaciones deben admitir el tema del sistema en todo momento. En este tema se proporciona un contexto para la información que puede ser de interés general para otra aplicación.

Los valores de los elementos de datos se deben representar en el formato del portapapeles de [**\_ texto CF**](standard-clipboard-formats.md) . Los elementos individuales de los valores de elemento de un tema del sistema deben estar delimitados por caracteres de tabulación. En la tabla siguiente se sugieren algunos elementos para el tema del sistema.



| Elemento          | Descripción                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formatos       | Lista delimitada por tabuladores de los formatos de Portapapeles que puede representar la aplicación. Normalmente, **los \_ formatos CF** se muestran con la parte "**CF \_**" de los nombres que se han quitado (por ejemplo, el **\_ texto CF** aparece como "**texto**").                                                                                        |
| Ayuda          | Texto que explica brevemente cómo usar el servidor DDE.                                                                                                                                                                                                                                                   |
| ReturnMessage | Detalles de compatibilidad del mensaje de [**confirmación de \_ DDE \_ de WM**](wm-dde-ack.md) usado más recientemente. Este elemento es útil cuando se requieren más de ocho bits de datos devueltos específicos de la aplicación.                                                                                                                |
| Status        | Indicación del estado actual de la aplicación. Cuando un servidor recibe un mensaje de [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) para este elemento de tema del sistema, debe responder mediante la publicación de un mensaje de [**\_ \_ datos de WM DDE**](wm-dde-data.md) con una cadena que contiene ocupado o listo, según corresponda. |
| SysItems      | Lista de elementos de tema del sistema admitidos por la aplicación.                                                                                                                                                                                                                                                    |
| TopicItemList | Similar al elemento SysItems, excepto que se debe admitir TopicItemList para cada tema que no sea el tema del sistema. Esto permite examinar los elementos admitidos en cualquier tema. Si no se pueden enumerar los elementos, este elemento solo debe contener "TopicItemList".                                  |
| Temas        | Lista de temas que la aplicación admite en el momento actual; Esta lista puede variar de un momento a un momento.                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>Vínculos de datos permanentes

Una vez iniciada una conversación DDE, el cliente puede establecer uno o más vínculos de datos permanentes con el servidor. Un vínculo de datos es un mecanismo de comunicaciones por el que el servidor notifica al cliente cada vez que cambia el valor de un elemento de datos especificado. El vínculo de datos es permanente en el sentido de que este proceso de notificación continúa hasta que se terminan el vínculo de datos o la propia conversación DDE.

Hay dos tipos de vínculos de datos DDE permanentes: en caliente y en caliente. En un vínculo de datos semiactivos, el servidor notifica al cliente que el valor del elemento de datos ha cambiado, pero el servidor no envía el valor de los datos al cliente hasta que el cliente lo solicita. En un vínculo de datos activos, el servidor envía inmediatamente el valor de los datos modificados al cliente.

Las aplicaciones que admiten vínculos de datos semiactivos o activos normalmente proporcionan un comando **copiar** o **pegar vínculo** en el menú **edición** para permitir al usuario establecer vínculos entre las aplicaciones.

### <a name="atoms-and-shared-memory-objects"></a>Átomos y objetos de memoria compartida

Algunos argumentos de los mensajes DDE son los átomos globales o los objetos de memoria compartida. Las aplicaciones que usan estos argumentos deben seguir las reglas explícitas sobre cuándo se deben asignar y eliminar. En todos los casos, el remitente del mensaje debe eliminar cualquier átomo o objeto de memoria compartida que el receptor previsto no recibirá debido a una condición de error, como el error de la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

DDE utiliza objetos de memoria compartida para tres propósitos:

-   Para llevar un valor de elemento de datos que se va a intercambiar. Se trata de un elemento al que hace referencia el parámetro *hData* en los mensajes de [**\_ \_ datos DDE de WM**](wm-dde-data.md) y de la función de consulta de [**\_ DDE \_ de WM**](wm-dde-poke.md) .
-   Para llevar las opciones de un mensaje. Se trata de un elemento al que hace referencia el parámetro *hOptions* en un mensaje de [**notificación de \_ DDE \_ de WM**](wm-dde-advise.md) .
-   Para llevar una cadena de ejecución de comandos. Se trata de un elemento al que hace referencia el parámetro *hCommands* en el mensaje de [**ejecución de WM \_ DDE \_**](wm-dde-execute.md) y su correspondiente mensaje de [**confirmación de WM \_ DDE \_**](wm-dde-ack.md) .

Una aplicación que recibe un objeto de memoria compartida DDE debe tratarla como de solo lectura. La aplicación no debe usar el objeto como un área de lectura y escritura mutua para el intercambio de datos libre.

Como en el caso de un átomo DDE, una aplicación debe liberar un objeto de memoria compartida para administrar la memoria de forma eficaz. La aplicación también debe bloquear y desbloquear los objetos de memoria.

## <a name="dynamic-data-exchange-messages-overview"></a>Información general sobre mensajes de Intercambio dinámico de datos

Dado que DDE es un protocolo basado en mensajes, no se emplean funciones o bibliotecas. Todas las transacciones DDE se llevan a cabo pasando algunos mensajes DDE definidos entre las ventanas cliente y servidor.

Hay nueve mensajes DDE; las constantes simbólicas de estos mensajes se definen en el archivo de encabezado DDE. También se definen ciertas estructuras para los distintos mensajes DDE en este archivo de encabezado.

En la tabla siguiente se resumen los mensajes DDE.



| Message                                        | Descripción                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_confirmación de DDE de WM \_**](wm-dde-ack.md)             | Confirma la recepción o no recepción de un mensaje.                                                                                               |
| [**\_aviso de DDE de WM \_**](wm-dde-advise.md)       | Solicita a la aplicación de servidor que proporcione una actualización o notificación para un elemento de datos cada vez que cambie. Esto establece un vínculo de datos permanente. |
| [**\_datos DDE de WM \_**](wm-dde-data.md)           | Envía un valor de elemento de datos a la aplicación cliente.                                                                                               |
| [**ejecución de WM \_ DDE \_**](wm-dde-execute.md)     | Envía una cadena a la aplicación de servidor, que se espera que procese la cadena como una serie de comandos.                                       |
| [**Inicio de WM \_ DDE \_**](wm-dde-initiate.md)   | Inicia una conversación entre las aplicaciones cliente y servidor.                                                                             |
| [**hiperdinámico de WM \_ \_**](wm-dde-poke.md)           | Envía un valor de elemento de datos a la aplicación de servidor.                                                                                               |
| [**\_solicitud de DDE de WM \_**](wm-dde-request.md)     | Solicita a la aplicación de servidor que proporcione el valor de un elemento de datos.                                                                             |
| [**\_finalización de WM DDE \_**](wm-dde-terminate.md) | Finaliza una conversación.                                                                                                                       |
| [**\_DESaconsejar DDE de WM \_**](wm-dde-unadvise.md)   | Finaliza un vínculo de datos permanente.                                                                                                                |



 

Una aplicación llama a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para emitir el mensaje de [**\_ \_ Inicio del DDE de WM**](wm-dde-initiate.md) o un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) enviado como respuesta a un **\_ \_ Inicio de WM DDE**. El resto de los mensajes se envían por [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). El primer parámetro de estas llamadas es un identificador de la ventana receptora; el segundo parámetro contiene el mensaje que se va a enviar; el tercer parámetro identifica la ventana de envío; y el cuarto parámetro contiene los argumentos específicos del mensaje.

## <a name="dynamic-data-exchange-message-flow"></a>Intercambio dinámico de datos flujo de mensajes

Una conversación DDE típica consta de los siguientes eventos:

1.  La aplicación cliente inicia la conversación y la aplicación de servidor responde.
2.  Las aplicaciones intercambian datos por cualquiera de los métodos siguientes:
    -   -   La aplicación de servidor envía datos al cliente en la solicitud del cliente.
        -   La aplicación cliente envía datos no solicitados a la aplicación de servidor.
        -   La aplicación cliente solicita a la aplicación de servidor que notifique al cliente cada vez que un elemento de datos cambia (vínculo de datos cálidos).
        -   La aplicación cliente solicita a la aplicación de servidor que envíe datos cada vez que cambien los datos (vínculo de datos activo).
        -   La aplicación de servidor lleva a cabo un comando en la solicitud del cliente.

3.  La aplicación de cliente o de servidor finaliza la conversación.

Una ventana de la aplicación que procesa las solicitudes de un cliente o servidor debe procesarlas estrictamente en el orden en que se reciben.

Un cliente puede establecer conversaciones con más de un servidor; un servidor puede tener conversaciones con más de un cliente. Al controlar los mensajes de más de un origen, un cliente o servidor debe procesar los mensajes de una conversación sincrónicamente, pero no es necesario procesar todos los mensajes sincrónicamente. En otras palabras, puede desplazarse de una conversación a otra según sea necesario.

Si una aplicación no puede procesar una solicitud entrante porque está esperando una respuesta DDE, debe evitar el interbloqueo mediante la publicación de un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) con el miembro **fBusy** de la estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) establecido en 1. Una aplicación también puede enviar un mensaje **de \_ \_ confirmación de DDE de WM** ocupado si, por cualquier motivo, no puede procesar una solicitud entrante en un período de tiempo razonable.

Una aplicación debe ser capaz de controlar el error de un cliente o servidor para responder a un mensaje dentro de un período de tiempo determinado. Dado que el intervalo de tiempo de espera puede variar en función de la naturaleza de la aplicación y de la configuración del sistema del usuario (incluido si está conectado a una red), la aplicación debe proporcionar una manera para que el usuario especifique el intervalo.

## <a name="parameter-packing-functions"></a>Funciones de empaquetado de parámetros

El parámetro *lParam* de muchos mensajes DDE contiene dos fragmentos de datos. Por ejemplo, el *lParam* del mensaje [**de \_ \_ datos DDE de WM**](wm-dde-data.md) contiene un identificador de datos y un átomo. Las aplicaciones deben usar la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) para empaquetar el identificador y Atom en un parámetro *lParam* y la función [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) para quitar los valores. Las aplicaciones DDE deben usar **PackDDElParam** y **UnpackDDElParam** para todos los mensajes publicados durante una conversación DDE.

Las aplicaciones también pueden usar las funciones [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) y [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) . **ReuseDDElParam** permite que una aplicación DDE reutilice un parámetro *lParam* empaquetado, lo que ayuda a reducir el número de reasignaciones de memoria que la aplicación debe realizar durante una conversación. Una aplicación puede utilizar **FreeDDElParam** para liberar la memoria asociada a un identificador de datos recibido durante una conversación DDE.

## <a name="dynamic-data-exchange-and-impersonation"></a>Intercambio dinámico de datos y suplantación

Para permitir que un servidor suplante a un cliente, el cliente llama a la función [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) . La estructura de [**\_ \_ nivel de suplantación de seguridad**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level) se utiliza para controlar el nivel de suplantación que el servidor puede llevar a cabo.

Un servidor DDE puede suplantar a un cliente DDE mediante una llamada a la función [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) . Un servidor DDEML debe utilizar la función [**DdeImpersonateClient**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient) .

 

 