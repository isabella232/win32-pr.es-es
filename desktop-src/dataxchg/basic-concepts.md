---
title: Conceptos básicos
description: En este tema se de abordan conceptos clave relacionados con el intercambio dinámico de datos.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Windows Interfaz de usuario,datos dinámicos Exchange (DDE)
- Windows Interfaz de usuario,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange (DDE),interacción del servidor cliente
- DDE (datos dinámicos Exchange),interacción del servidor cliente
- intercambio de datos,datos dinámicos Exchange (DDE)
- intercambio de datos,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange (DDE),aplicaciones cliente
- DDE (datos dinámicos Exchange),aplicaciones cliente
- datos dinámicos Exchange (DDE),aplicaciones de servidor
- DDE (datos dinámicos Exchange),aplicaciones de servidor
- datos dinámicos Exchange (DDE), funciones de devolución de llamada
- DDE (datos dinámicos Exchange), funciones de devolución de llamada
- datos dinámicos Exchange (DDE), transacciones
- DDE (datos dinámicos Exchange), transacciones
- datos dinámicos Exchange (DDE),nombres de servicio
- DDE (datos dinámicos Exchange),nombres de servicio
- datos dinámicos Exchange (DDE),nombres de elemento
- DDE (datos dinámicos Exchange),nombres de elemento
- datos dinámicos Exchange (DDE),nombres de tema
- DDE (datos dinámicos Exchange),nombres de tema
- datos dinámicos Exchange (DDE),Tema del sistema
- DDE (datos dinámicos Exchange),Tema del sistema
- datos dinámicos Exchange Management Library (DDEML),initialization
- DDEML (datos dinámicos Exchange management library),initialization
- datos dinámicos Exchange Management Library (DDEML), funciones de devolución de llamada
- DDEML (biblioteca datos dinámicos Exchange administración de eventos), funciones de devolución de llamada
- datos dinámicos Exchange Management Library (DDEML), administración de cadenas
- DDEML (biblioteca datos dinámicos Exchange administración de cadenas), administración de cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae271c359afd571cf6c51fb3387a15f1496416e5eb54b055ef518fd213f30fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128627"
---
# <a name="basic-concepts-dde"></a>Conceptos básicos (DDE)

Estos conceptos son clave para comprender datos dinámicos Exchange (DDE) y datos dinámicos Exchange Management Library (DDEML).

-   [Interacción de cliente y servidor](#client-and-server-interaction)
-   [Transacciones y la función de devolución de llamada DDE](#transactions-and-the-dde-callback-function)
-   [Nombres de servicio, nombres de tema y nombres de elemento](#service-names-topic-names-and-item-names)
-   [Tema del sistema](#system-topic)
-   [Inicialización](#initialization)
-   [Función de devolución de llamada](#callback-function)
-   [Administración de cadenas](#string-management)
-   [DDEML y subprocesos](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Interacción de cliente y servidor

DDE siempre se produce entre una aplicación cliente y una aplicación de servidor. La *aplicación cliente DDE* inicia el intercambio estableciendo una conversación con el servidor para enviar transacciones al servidor. Una transacción es una solicitud de datos o servicios. La *aplicación de servidor DDE* responde a las transacciones proporcionando datos o servicios al cliente. Por ejemplo, una aplicación gráfica puede contener un gráfico de barras que representa los beneficios trimestrales de una empresa, pero los datos del gráfico de barras pueden estar contenidos en una aplicación de hoja de cálculo. Para obtener las cifras de beneficios más recientes, la aplicación de gráficos (el cliente) podría establecer una conversación con la aplicación de hoja de cálculo (el servidor). Después, la aplicación de gráficos podría enviar una transacción a la aplicación de hoja de cálculo, solicitando las cifras de beneficios más recientes.

Un servidor puede tener muchos clientes al mismo tiempo y un cliente puede solicitar datos de varios servidores. Una aplicación también puede ser un cliente y un servidor. El cliente o el servidor pueden finalizar la conversación en cualquier momento.

## <a name="transactions-and-the-dde-callback-function"></a>Transacciones y la función de devolución de llamada DDE

DDEML notifica a una aplicación la actividad DDE que afecta a la aplicación mediante el envío de transacciones a la función de devolución de llamada DDE de la aplicación. Una *transacción DDE* es similar a un mensaje, es una constante con nombre acompañada de otros parámetros que contienen información adicional sobre la transacción.

DDEML pasa una transacción a una función de devolución de llamada DDE definida por la aplicación que lleva a cabo una acción adecuada para el tipo de transacción. Por ejemplo, cuando una aplicación cliente intenta establecer una conversación con una aplicación de servidor, el cliente llama a la [**función DdeConnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) Esta función hace que DDEML envíe una transacción [**XTYP \_ CONNECT**](xtyp-connect.md) a la función de devolución de llamada DDE del servidor. La función de devolución de llamada puede permitir la conversación devolviendo **TRUE** a DDEML, o bien puede denegar la conversación devolviendo **FALSE**. Para obtener una explicación detallada de las transacciones, vea [Administración de transacciones.](transaction-management.md)

## <a name="service-names-topic-names-and-item-names"></a>Nombres de servicio, nombres de tema y nombres de elemento

Un servidor DDE usa un nombre de servicio de jerarquía de tres niveles (denominado "nombre de aplicación" en la documentación de DDE anterior), el nombre del tema y el nombre del elemento para identificar de forma única una unidad de datos que el servidor puede intercambiar durante una conversación.

Un *nombre de servicio* es una cadena a la que responde una aplicación de servidor cuando un cliente intenta establecer una conversación con el servidor. Un cliente debe especificar este nombre de servicio para establecer una conversación con el servidor. Aunque un servidor puede responder a muchos nombres de servicio, la mayoría de los servidores responden a un solo nombre.

Un *nombre de tema* es una cadena que identifica un contexto de datos lógicos. En el caso de los servidores que operan en documentos basados en archivos, los nombres de tema suelen ser nombres de archivo; para otros servidores, son otras cadenas específicas de la aplicación. Un cliente debe especificar un nombre de tema junto con el nombre de servicio de un servidor cuando intenta establecer una conversación con un servidor.

Un *nombre de elemento* es una cadena que identifica una unidad de datos que un servidor puede pasar a un cliente durante una transacción. Por ejemplo, un nombre de elemento podría identificar un entero, una cadena, varios párrafos de texto o un mapa de bits.

Los nombres de servicio, tema y elemento permiten al cliente establecer una conversación con un servidor y recibir datos del servidor.

## <a name="system-topic"></a>Tema del sistema

El tema Sistema proporciona un contexto para la información de interés general para cualquier cliente DDE. Se recomienda que las aplicaciones de servidor admitan el tema Sistema en todo momento. El tema System se define en DDEML. Archivo de encabezado H como SZDDESYS \_ TOPIC.

Para determinar qué servidores están presentes y los tipos de información que pueden proporcionar, una aplicación cliente puede solicitar una conversación en el tema Sistema al iniciarse, estableciendo el nombre del dispositivo en **NULL.** Estas conversaciones con caracteres comodín son costosas en términos de rendimiento del sistema, por lo que se deben mantener al mínimo. Para obtener más información sobre cómo iniciar conversaciones de DDE, vea [Conversation Management](conversation-management.md).

Un servidor debe admitir los siguientes nombres de elemento dentro del tema Sistema y cualquier otro nombre de elemento que sea útil para un cliente.



| Elemento                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SZDDE \_ ITEM \_ ITEMLIST    | Lista de los elementos admitidos en un tema que no es del sistema. (Esta lista puede variar de un momento a otro y de un tema a otro).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| FORMATOS DE ELEMENTOS SZDDESYS \_ \_  | Lista delimitada por tabulaciones de cadenas que representan todos los formatos del Portapapeles posiblemente admitidos por la aplicación de servicio. Las cadenas que representan formatos predefinidos del Portapapeles son equivalentes a los valores cf \_ con el prefijo \_ "CF" quitado. Por ejemplo, el formato CF \_ TEXT se representa mediante la cadena "TEXT". Estas cadenas deben estar en mayúsculas para identificarlas aún más como formatos predefinidos. La lista de formatos debe aparecer en el orden de contenido más enriquecido a menos enriquecido en contenido. Para obtener más información sobre los formatos del Portapapeles y los datos de representación, vea [Portapapeles.](clipboard.md)<br/> |
| AYUDA DEL ELEMENTO SZDDESYS \_ \_     | Información legible por el usuario de interés general. Este elemento debe contener, como mínimo, información sobre cómo usar las características de DDE de la aplicación de servidor. Esta información puede incluir, entre otras cosas, cómo especificar elementos dentro de temas, qué cadenas de ejecución puede realizar el servidor, qué transacciones de búsqueda se permiten y cómo encontrar ayuda sobre otros elementos de tema del sistema.                                                                                                                                                                                                                           |
| ELEMENTO SZDDESYS \_ \_ RTNMSG   | Detalles de compatibilidad para el mensaje [**wm \_ DDE \_ ACK usado más**](wm-dde-ack.md) recientemente. Este elemento es útil cuando se requieren más de 8 bits de datos devueltos específicos de la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ESTADO DEL ELEMENTO SZDDESYS \_ \_   | Indicación del estado actual del servidor. Normalmente, este elemento solo admite el formato CF \_ TEXT y contiene la cadena Listo o Ocupado.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ELEMENTOS SZDDESYS \_ \_ SYSITEMS | Lista de los elementos admitidos en el tema Sistema por este servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| TEMAS DE ELEMENTOS SZDDESYS \_ \_   | Una lista de los temas admitidos por el servidor en el momento actual. (Esta lista puede variar de un momento a otro).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Estos nombres de elemento son valores definidos en DDEML. Archivo de encabezado H. Para obtener identificadores de cadena para estas cadenas, una aplicación debe usar las funciones de administración de cadenas DDEML, como lo haría con cualquier otra cadena de una aplicación DDEML. Para obtener más información sobre cómo administrar cadenas, vea [Administración de cadenas.](#string-management)

## <a name="initialization"></a>Inicialización

Antes de llamar a cualquier otra función DDEML, una aplicación debe llamar a la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) **DdeInitialize** obtiene un identificador de instancia para la aplicación, registra la función de devolución de llamada DDE de la aplicación con el DDE y especifica las marcas de filtro de transacción para la función de devolución de llamada.

Cada instancia de una aplicación o un archivo DLL debe pasar su identificador de instancia como parámetro *idInst* a cualquier otra función DDEML que lo requiera. El propósito de varias instancias de DDEML es admitir archivos DLL que deben usar la DDEML al mismo tiempo que una aplicación la usa. Una aplicación no debe usar más de una instancia de DDEML.

*Los filtros de transacción* optimizan el rendimiento del sistema al impedir que DDEML pase transacciones no deseadas a la función de devolución de llamada DDE de la aplicación. Una aplicación establece los filtros de transacción [**en el parámetro DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd.* Una aplicación debe especificar una marca de filtro de transacción para cada tipo de transacción que no procese en su función de devolución de llamada. Una aplicación puede cambiar sus filtros de transacción con una llamada posterior a **DdeInitialize**. Para obtener más información sobre las transacciones, vea [Administración de transacciones.](transaction-management.md)

En el ejemplo siguiente se muestra cómo inicializar una aplicación para usar DDEML.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Una aplicación debe llamar a [**la función DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) cuando ya no vaya a usar la DDEML. Esta función finaliza todas las conversaciones abiertas actualmente para la aplicación y libera los recursos de DDEML que el sistema asignó a la aplicación.

## <a name="callback-function"></a>Función de devolución de llamada

Una aplicación que use DDEML debe proporcionar una función de devolución de llamada que procese los eventos DDE que afectan a la aplicación. DDEML notifica a una aplicación estos eventos mediante el envío de transacciones a la función de devolución de llamada DDE de la aplicación. Las transacciones que recibe una función de devolución de llamada dependen de qué filtro de devolución de llamada marca la aplicación especificada en [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) y de si la aplicación es un cliente, un servidor o ambos. Para obtener más información, vea [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

En el ejemplo siguiente se muestra la estructura general de una función de devolución de llamada para una aplicación cliente típica.


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



El *parámetro uType* especifica el tipo de transacción enviado a la función de devolución de llamada por DDEML. Los valores de los parámetros restantes dependen del tipo de transacción. Los tipos de transacción y los eventos que los generan se describen en los temas siguientes. Para obtener información detallada sobre cada tipo de transacción, vea [Administración de transacciones.](transaction-management.md)

## <a name="string-management"></a>Administración de cadenas

Para llevar a cabo una tarea DDE, muchas funciones de DDEML requieren acceso a las cadenas. Por ejemplo, un cliente debe especificar un nombre de servicio y un nombre de tema cuando llama a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) para solicitar una conversación con un servidor. Una aplicación especifica una cadena pasando un identificador de cadena (HSZ) en lugar de un puntero en una función DDEML. Un *identificador de* cadena es un valor **DWORD,** asignado por el sistema, que identifica una cadena.

Una aplicación puede obtener un identificador de cadena para una cadena determinada llamando a la [**función DdeCreateStringHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) Esta función registra la cadena con el sistema y devuelve un identificador de cadena a la aplicación. La aplicación puede pasar el identificador a las funciones de DDEML que deben tener acceso a la cadena. En el ejemplo siguiente se obtienen identificadores de cadena para la cadena de tema System y la cadena de nombre de servicio.


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



El *parámetro idInst* del ejemplo anterior especifica el identificador de instancia obtenido por la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

La función de devolución de llamada DDE de una aplicación recibe uno o varios identificadores de cadena durante la mayoría de las transacciones de DDE. Por ejemplo, un servidor recibe dos identificadores de cadena durante la transacción [**XTYP \_ REQUEST:**](xtyp-request.md) uno identifica una cadena que especifica un nombre de tema y la otra identifica una cadena que especifica un nombre de elemento. Una aplicación puede obtener la longitud de la cadena que corresponde a un identificador de cadena y copiar la cadena en un búfer definido por la aplicación llamando a la función [**DdeQueryString,**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) como se muestra en el ejemplo siguiente.


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



No se puede asignar un identificador de cadena específico de instancia del identificador de cadena a la cadena y volver al identificador de cadena. Por ejemplo, aunque [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crea una cadena a partir de un identificador de cadena y, a continuación, [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) crea un identificador de cadena a partir de esa cadena, los dos identificadores no son los mismos, como se muestra en el ejemplo siguiente.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Para comparar los valores de dos identificadores de cadena, use la [**función DdeCmpStringHandles.**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles)

Un identificador de cadena pasado a la función de devolución de llamada DDE de una aplicación deja de ser válido cuando se devuelve la función de devolución de llamada. Una aplicación puede guardar un identificador de cadena para su uso después de que la función de devolución de llamada devuelva mediante la [**función DdeKeepStringHandle.**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)

Cuando una aplicación llama a [**DdeCreateStringHandle,**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea)el sistema escribe la cadena especificada en una tabla de cadenas y genera un identificador que usa para acceder a la cadena. El sistema también mantiene un recuento de uso para cada cadena de la tabla de cadenas.

Cuando una aplicación llama a [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) y especifica una cadena que ya existe en la tabla, el sistema incrementa el recuento de uso en lugar de agregar otra aparición de la cadena. (Una aplicación también puede incrementar el recuento de uso mediante [**DdeKeepStringHandle).**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) Cuando una aplicación llama a la [**función DdeFreeStringHandle,**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) el sistema disminuye el recuento de uso.

Se quita una cadena de la tabla cuando su recuento de uso es igual a cero. Dado que más de una aplicación puede obtener el identificador de una cadena determinada, una aplicación no debe liberar un identificador de cadena más veces de lo que ha creado o retenido el identificador. De lo contrario, la aplicación puede hacer que la cadena se quite de la tabla, lo que deniega a otras aplicaciones el acceso a la cadena.

Las funciones de administración de cadenas DDEML se basan en el administrador atom y están sujetas a las mismas restricciones de tamaño que los átomos.

## <a name="ddeml-and-threads"></a>DDEML y subprocesos

La [**función DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registra una aplicación con la DDEML y crea una instancia de DDEML. Una instancia de DDEML está basada en subprocesos, asociada al subproceso que **llamó a DdeInitialize.**

Todas las llamadas de función DDEML para objetos que pertenecen a una instancia de DDEML deben realizarse desde el mismo subproceso que llamó a [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) para crear la instancia. Si llama a una función DDEML desde un subproceso diferente, se producirá un error en la función. No se puede acceder a una conversación DDEML desde un subproceso distinto del que asignó la conversación.

 

