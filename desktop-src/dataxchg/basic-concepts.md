---
title: Conceptos básicos
description: En este tema se describen los conceptos básicos relacionados con el intercambio dinámico de datos.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Intercambio dinámico de datos (DDE), interacción del servidor cliente
- DDE (Intercambio dinámico de datos), interacción del servidor cliente
- intercambio de datos, Intercambio dinámico de datos (DDE)
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Intercambio dinámico de datos (DDE), aplicaciones cliente
- DDE (Intercambio dinámico de datos), aplicaciones cliente
- Intercambio dinámico de datos (DDE), aplicaciones de servidor
- DDE (Intercambio dinámico de datos), aplicaciones de servidor
- Intercambio dinámico de datos (DDE), funciones de devolución de llamada
- DDE (Intercambio dinámico de datos), funciones de devolución de llamada
- Intercambio dinámico de datos (DDE), transacciones
- DDE (Intercambio dinámico de datos), transacciones
- Intercambio dinámico de datos (DDE), nombres de servicio
- DDE (Intercambio dinámico de datos), nombres de servicio
- Intercambio dinámico de datos (DDE), nombres de elemento
- DDE (Intercambio dinámico de datos), nombres de elemento
- Intercambio dinámico de datos (DDE), nombres de tema
- DDE (Intercambio dinámico de datos), nombres de tema
- Intercambio dinámico de datos (DDE), tema del sistema
- DDE (Intercambio dinámico de datos), tema del sistema
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), inicialización
- DDEML (biblioteca de administración de Intercambio dinámico de datos), inicialización
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), funciones de devolución de llamada
- DDEML (biblioteca de administración de Intercambio dinámico de datos), funciones de devolución de llamada
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), administración de cadenas
- DDEML (biblioteca de administración de Intercambio dinámico de datos), administración de cadenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792088"
---
# <a name="basic-concepts-dde"></a>Conceptos básicos (DDE)

Estos conceptos son fundamentales para comprender Intercambio dinámico de datos (DDE) y la biblioteca de administración de Intercambio dinámico de datos (DDEML).

-   [Interacción entre cliente y servidor](#client-and-server-interaction)
-   [Transacciones y la función de devolución de llamada DDE](#transactions-and-the-dde-callback-function)
-   [Nombres de servicio, nombres de tema y nombres de elemento](#service-names-topic-names-and-item-names)
-   [Tema del sistema](#system-topic)
-   [Inicialización](#initialization)
-   [Función de devolución de llamada](#callback-function)
-   [Administración de cadenas](#string-management)
-   [DDEML y threads](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Interacción entre cliente y servidor

DDE siempre se produce entre una aplicación cliente y una aplicación de servidor. La *aplicación cliente DDE* inicia el intercambio estableciendo una conversación con el servidor para enviar las transacciones al servidor. Una transacción es una solicitud de datos o servicios. La *aplicación de servidor DDE* responde a las transacciones proporcionando datos o servicios al cliente. Por ejemplo, una aplicación de gráficos puede contener un gráfico de barras que representa los beneficios trimestrales de una corporación, pero los datos del gráfico de barras pueden estar contenidos en una aplicación de hoja de cálculo. Para obtener las últimas cifras de beneficios, la aplicación de gráficos (el cliente) podría establecer una conversación con la aplicación de hoja de cálculo (el servidor). La aplicación de gráficos podría enviar una transacción a la aplicación de hoja de cálculo, lo que solicitaría las últimas cifras de beneficios.

Un servidor puede tener muchos clientes al mismo tiempo y un cliente puede solicitar datos de varios servidores. Una aplicación también puede ser un cliente y un servidor. El cliente o el servidor pueden finalizar la conversación en cualquier momento.

## <a name="transactions-and-the-dde-callback-function"></a>Transacciones y la función de devolución de llamada DDE

El DDEML notifica a una aplicación acerca de la actividad DDE que afecta a la aplicación mediante el envío de transacciones a la función de devolución de llamada DDE de la aplicación. Una *transacción DDE* es similar a un mensaje es una constante con nombre que acompaña a otros parámetros que contienen información adicional sobre la transacción.

El DDEML pasa una transacción a una función de devolución de llamada DDE definida por la aplicación que lleva a cabo una acción adecuada para el tipo de transacción. Por ejemplo, cuando una aplicación cliente intenta establecer una conversación con una aplicación de servidor, el cliente llama a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) . Esta función hace que DDEML envíe una transacción [**XTYP \_ Connect**](xtyp-connect.md) a la función de devolución de llamada DDE del servidor. La función de devolución de llamada puede permitir la conversación devolviendo **true** a ddeml o puede denegar la conversación devolviendo **false**. Para obtener una explicación detallada de las transacciones, consulte [Administración de transacciones](transaction-management.md).

## <a name="service-names-topic-names-and-item-names"></a>Nombres de servicio, nombres de tema y nombres de elemento

Un servidor DDE usa un nombre de servicio de jerarquía de tres niveles (denominado "nombre de aplicación" en la documentación DDE anterior), el nombre del tema y el nombre del elemento para identificar de forma única una unidad de datos que el servidor puede intercambiar durante una conversación.

Un *nombre de servicio* es una cadena a la que responde una aplicación de servidor cuando un cliente intenta establecer una conversación con el servidor. Un cliente debe especificar este nombre de servicio para establecer una conversación con el servidor. Aunque un servidor puede responder a muchos nombres de servicio, la mayoría de los servidores responden a un solo nombre.

Un *nombre de tema* es una cadena que identifica un contexto de datos lógico. En el caso de los servidores que operan en documentos basados en archivos, los nombres de tema suelen ser nombres de archivo. en el caso de otros servidores, son otras cadenas específicas de la aplicación. Un cliente debe especificar un nombre de tema junto con el nombre de servicio de un servidor cuando intenta establecer una conversación con un servidor.

Un *nombre de elemento* es una cadena que identifica una unidad de datos que un servidor puede pasar a un cliente durante una transacción. Por ejemplo, un nombre de elemento puede identificar un entero, una cadena, varios párrafos de texto o un mapa de bits.

Los nombres de servicio, tema y elemento permiten al cliente establecer una conversación con un servidor y recibir datos del servidor.

## <a name="system-topic"></a>Tema del sistema

El tema sistema proporciona un contexto para la información de interés general para cualquier cliente DDE. Se recomienda que las aplicaciones de servidor admitan el tema del sistema en todo momento. El tema del sistema se define en el DDEML. H archivo de encabezado como \_ tema de SZDDESYS.

Para determinar qué servidores están presentes y los tipos de información que pueden proporcionar, una aplicación cliente puede solicitar una conversación en el tema del sistema al iniciarse y establecer el nombre del dispositivo en **null**. Estas conversaciones de carácter comodín son costosas en términos de rendimiento del sistema, por lo que deben mantenerse al mínimo. Para obtener más información acerca de cómo iniciar conversaciones DDE, vea [Administración](conversation-management.md)de conversaciones.

Un servidor debe admitir los siguientes nombres de elemento en el tema del sistema y cualquier otro nombre de elemento que sea útil para un cliente.



| Elemento                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SZDDE \_ elemento \_ ITEMLIST    | Una lista de los elementos admitidos en un tema que no es del sistema. (Esta lista puede variar de un momento a un momento y del tema al tema).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_formatos de elemento SZDDESYS \_  | Una lista delimitada por tabulaciones de cadenas que representan todos los formatos del portapapeles admitidos por la aplicación de servicio. Las cadenas que representan formatos predefinidos del portapapeles son equivalentes a los \_ valores CF con el \_ prefijo "CF" quitado. Por ejemplo, el \_ formato de texto CF se representa mediante la cadena "Text". Estas cadenas deben estar en mayúsculas para identificarlas como formatos predefinidos. La lista de formatos debe aparecer en el orden de contenido más rico en el contenido menos amplio. Para obtener más información sobre los formatos del portapapeles y los datos de representación, vea [portapapeles](clipboard.md).<br/> |
| \_ayuda del elemento SZDDESYS \_     | Información legible por el usuario de interés general. Este elemento debe contener, como mínimo, información sobre cómo usar las características DDE de la aplicación de servidor. Esta información puede incluir, entre otras cosas, cómo especificar elementos en los temas, qué ejecutar las cadenas que el servidor puede realizar, qué transacciones de ejemplo se permiten y cómo buscar ayuda en otros elementos del tema del sistema.                                                                                                                                                                                                                           |
| SZDDESYS \_ elemento \_ RTNMSG   | Detalles de compatibilidad del mensaje de [**confirmación de \_ DDE \_ de WM**](wm-dde-ack.md) usado más recientemente. Este elemento es útil cuando se requieren más de 8 bits de datos devueltos específicos de la aplicación.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_Estado del elemento SZDDESYS \_   | Indicación del estado actual del servidor. Normalmente, este elemento solo admite el \_ formato de texto CF y contiene la cadena Ready o busy.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SZDDESYS \_ elemento \_ SYSITEMS | Una lista de los elementos admitidos en el tema del sistema por este servidor.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_ \_ temas sobre elementos SZDDESYS   | Una lista de los temas admitidos por el servidor en el momento actual. (Esta lista puede variar de un momento a un momento).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Estos nombres de elemento son valores definidos en DDEML. Archivo de encabezado H. Para obtener los identificadores de cadena de estas cadenas, una aplicación debe usar las funciones de administración de cadenas DDEML, del mismo modo que lo haría con cualquier otra cadena en una aplicación DDEML. Para obtener más información sobre cómo administrar cadenas, vea [Administración](#string-management)de cadenas.

## <a name="initialization"></a>Inicialización

Antes de llamar a cualquier otra función DDEML, una aplicación debe llamar a la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . **DdeInitialize** obtiene un identificador de instancia de la aplicación, registra la función de devolución de llamada DDE de la aplicación con el DDE y especifica las marcas de filtro de transacción para la función de devolución de llamada.

Cada instancia de una aplicación o un archivo DLL debe pasar su identificador de instancia como el parámetro *idInst* a cualquier otra función ddeml que lo requiera. El propósito de varias instancias de DDEML es admitir archivos DLL que deben usar el DDEML al mismo tiempo que una aplicación lo está usando. Una aplicación no debe usar más de una instancia de DDEML.

Los *filtros de transacciones* optimizan el rendimiento del sistema evitando que el ddeml pase transacciones no deseadas a la función de devolución de llamada DDE de la aplicación. Una aplicación establece los filtros de transacción en el parámetro *ufCmd* de [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Una aplicación debe especificar una marca de filtro de transacción para cada tipo de transacción que no procese en su función de devolución de llamada. Una aplicación puede cambiar sus filtros de transacciones con una llamada subsiguiente a **DdeInitialize**. Para obtener más información acerca de las transacciones, consulte [Administración de transacciones](transaction-management.md).

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



Una aplicación debe llamar a la función [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) cuando ya no vaya a usar ddeml. Esta función finaliza todas las conversaciones abiertas actualmente para la aplicación y libera los recursos de DDEML que el sistema ha asignado para la aplicación.

## <a name="callback-function"></a>Función de devolución de llamada

Una aplicación que usa DDEML debe proporcionar una función de devolución de llamada que procese los eventos DDE que afectan a la aplicación. El DDEML notifica a una aplicación de estos eventos mediante el envío de transacciones a la función de devolución de llamada DDE de la aplicación. Las transacciones que recibe una función de devolución de llamada dependen de qué filtro de devolución de llamada marca la aplicación especificada en [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) y si la aplicación es un cliente, un servidor o ambos. Para obtener más información, consulte [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

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



El parámetro *uType* especifica el tipo de transacción que el ddeml envía a la función de devolución de llamada. Los valores de los parámetros restantes dependen del tipo de transacción. En los temas siguientes se describen los tipos de transacción y los eventos que los generan. Para obtener información detallada acerca de cada tipo de transacción, consulte [Administración de transacciones](transaction-management.md).

## <a name="string-management"></a>Administración de cadenas

Para llevar a cabo una tarea DDE, muchas funciones DDEML requieren acceso a las cadenas. Por ejemplo, un cliente debe especificar un nombre de servicio y un nombre de tema cuando llama a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) para solicitar una conversación con un servidor. Una aplicación especifica una cadena pasando un identificador de cadena (HSZ) en lugar de un puntero en una función DDEML. Un *identificador de cadena* es un valor **DWORD** , asignado por el sistema, que identifica una cadena.

Una aplicación puede obtener un identificador de cadena para una cadena determinada mediante una llamada a la función [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) . Esta función registra la cadena con el sistema y devuelve un identificador de cadena a la aplicación. La aplicación puede pasar el identificador a las funciones DDEML que deben tener acceso a la cadena. En el ejemplo siguiente se obtienen los identificadores de cadena para la cadena de tema del sistema y la cadena de nombre de servicio.


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



El parámetro *idInst* en el ejemplo anterior especifica el identificador de instancia obtenido por la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

La función de devolución de llamada DDE de una aplicación recibe uno o más identificadores de cadena durante la mayoría de las transacciones DDE. Por ejemplo, un servidor recibe dos identificadores de cadena durante la transacción de [**\_ solicitud XTYP**](xtyp-request.md) : uno identifica una cadena que especifica un nombre de tema y el otro identifica una cadena que especifica un nombre de elemento. Una aplicación puede obtener la longitud de la cadena que corresponde a un identificador de cadena y copiar la cadena en un búfer definido por la aplicación mediante una llamada a la función [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) , tal y como se muestra en el ejemplo siguiente.


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



Un identificador de cadena específico de la instancia no se puede asignar desde el identificador de cadena a la cadena y volver al identificador de cadena. Por ejemplo, aunque [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crea una cadena a partir de un identificador de cadena y, a continuación, [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) crea un identificador de cadena a partir de esa cadena, los dos identificadores no son los mismos, tal y como se muestra en el ejemplo siguiente.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Para comparar los valores de dos identificadores de cadena, utilice la función [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .

Un identificador de cadena que se pasa a la función de devolución de llamada DDE de una aplicación deja de ser válido cuando devuelve la función de devolución de llamada. Una aplicación puede guardar un identificador de cadena para su uso después de que la función de devolución de llamada devuelva mediante la función [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) .

Cuando una aplicación llama a [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), el sistema escribe la cadena especificada en una tabla de cadenas y genera un identificador que usa para tener acceso a la cadena. El sistema también mantiene un recuento de uso de cada cadena en la tabla de cadenas.

Cuando una aplicación llama a [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) y especifica una cadena que ya existe en la tabla, el sistema incrementa el recuento de uso en lugar de agregar otra aparición de la cadena. (Una aplicación también puede incrementar el recuento de uso mediante [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle)). Cuando una aplicación llama a la función [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) , el sistema disminuye el recuento de uso.

Una cadena se quita de la tabla cuando su recuento de uso es igual a cero. Dado que más de una aplicación puede obtener el identificador de una cadena determinada, una aplicación no debe liberar un identificador de cadena más veces de lo que ha creado o retenido el identificador. De lo contrario, la aplicación puede hacer que la cadena se quite de la tabla, denegando el acceso de otras aplicaciones a la cadena.

Las funciones de administración de cadenas de DDEML se basan en el administrador de Atom y están sujetas a las mismas restricciones de tamaño que los átomos.

## <a name="ddeml-and-threads"></a>DDEML y threads

La función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) registra una aplicación con el ddeml y crea una instancia de ddeml. Una instancia de DDEML está basada en subprocesos, asociada al subproceso que llamó a **DdeInitialize**.

Todas las llamadas de función DDEML para objetos que pertenecen a una instancia de DDEML deben realizarse desde el mismo subproceso que llamó a [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) para crear la instancia. Si llama a una función DDEML desde otro subproceso, se producirá un error en la función. No se puede tener acceso a una conversación DDEML desde un subproceso distinto del que asignó la conversación.

 

