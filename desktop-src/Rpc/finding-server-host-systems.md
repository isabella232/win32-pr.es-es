---
title: Búsqueda de sistemas host de servidor
description: Buscar sistemas host de servidor mediante enlaces de cadena y consultando una base de datos de servicio de nombres para la ubicación de un programa de servidor.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903551"
---
# <a name="finding-server-host-systems"></a>Búsqueda de sistemas host de servidor

Un sistema host de servidor es el equipo que ejecuta el programa de servidor de la aplicación distribuida. Puede haber uno o varios sistemas host de servidor en una red. El modo en que el programa cliente encuentra un servidor al que se va a conectar depende de las necesidades de su programa.

Existen dos métodos para buscar sistemas de host de servidor:

-   Uso de la información almacenada en cadenas en el código fuente del cliente, variables de entorno o archivos de configuración específicos de la aplicación. La aplicación cliente puede usar los datos de la cadena para crear un enlace entre el cliente y el servidor.
-   Consultar una base de datos del servicio de nombres para la ubicación de un programa de servidor.

En esta sección se presenta información sobre estas dos técnicas en los temas siguientes:

-   [Usar enlaces de cadena](#using-string-bindings)
-   [Importar desde bases de datos de nombre de servicio](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Usar enlaces de cadena

Las aplicaciones pueden crear enlaces a partir de la información almacenada en cadenas. La aplicación cliente compone esta información como una cadena y, a continuación, llama a la función [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) . El cliente debe proporcionar la siguiente información para identificar el servidor:

-   El nombre de la interfaz, el identificador único global (GUID) del objeto o el UUID del objeto. Para obtener más información, vea generación de UUID de [interfaz](generating-interface-uuids.md) y [UUID de cadena](string-uuid.md).
-   Tipo de transporte que se va a comunicar, como canalizaciones con nombre o TCP/IP. Para obtener más información, vea [terminología de enlace RPC esencial](essential-rpc-binding-terminology.md) y [seleccionar una secuencia de protocolo](selecting-a-protocol-sequence.md).
-   La dirección de red o el nombre del equipo host del servidor.
-   Extremo del programa de servidor en el equipo host del servidor. Para obtener más información, consulte [búsqueda de puntos de conexión](finding-endpoints.md)y especificación de puntos de [conexión](specifying-endpoints.md).

(El UUID del objeto y la información del punto de conexión son opcionales).

En los ejemplos siguientes, el parámetro *pszNetworkAddress* y otros parámetros incluyen barras diagonales inversas incrustadas. La barra diagonal inversa es un carácter de escape en el lenguaje de programación C. Se necesitan dos barras diagonales inversas para representar cada carácter de barra diagonal inversa literal. La estructura de enlace de cadena debe contener cuatro caracteres de barra diagonal inversa para representar los dos caracteres de barra diagonal inversa literal que preceden al nombre del servidor.

En el ejemplo siguiente se muestra que el nombre del servidor debe ir precedido por ocho barras diagonales inversas para que aparezcan cuatro caracteres de barra diagonal inversa literal en la estructura de datos de enlace de cadenas después de que la función **sprintf \_ s** procese la cadena.


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



En el ejemplo siguiente, el enlace de cadena aparece como:

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *ServerName* \[ \\ \\ Pipe \\ \\ *pipename*\]

Después, el cliente llama a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obtener el identificador de enlace:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Una función conveniente, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) ensambla el UUID del objeto, la secuencia del Protocolo, la dirección de red y el punto de conexión en la sintaxis correcta para la llamada a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding). No tiene que preocuparse de colocar la y comercial, los dos puntos y los distintos componentes de cada secuencia de protocolo en el lugar adecuado; basta con proporcionar las cadenas como parámetros a la función. La biblioteca en tiempo de ejecución incluso asigna la memoria necesaria para el enlace de cadenas.


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



Otra función útil, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), toma un identificador de enlace como entrada y genera el enlace de cadena correspondiente.

## <a name="importing-from-name-service-databases"></a>Importar desde bases de datos de nombre de servicio

Almacén de bases de datos del servicio de nombres, entre otras cosas, identificadores de enlace y UUID. La aplicación cliente puede buscar uno o ambos de ellos cuando sea necesario enlazar con el servidor. Para obtener una explicación de la información que almacena un servicio de nombres y el formato de almacenamiento, consulte [la base de datos del servicio de nombres de RPC](the-rpc-name-service-database.md).

La biblioteca RPC proporciona dos conjuntos de funciones que el programa cliente puede utilizar para buscar en la base de datos del servicio de nombres. Los nombres de un conjunto comienzan por RpcNsBindingImport. Los nombres del otro conjunto comienzan por RpcNsBindingLookup. La diferencia entre los dos grupos de funciones es que las funciones RpcNsBindingImport devuelven un único identificador de enlace por llamada y las funciones RpcNsBindingLookup devuelven grupos de identificadores por llamada.

Para iniciar una búsqueda con las funciones de RpcNsBindingImport, llame primero a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), como se muestra en el fragmento de código siguiente.


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



Cuando las funciones RPC buscan en la base de datos del servicio de nombres, necesitan un lugar para comenzar la búsqueda. En la terminología de RPC, esto se denomina nombre de entrada. El programa cliente pasa el nombre de la entrada como el segundo parámetro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Este parámetro puede ser **null** si desea buscar en toda la base de datos del servicio de nombres. Como alternativa, puede buscar en la entrada del servidor pasando un nombre de entrada de servidor o buscar en la entrada de grupo pasando un nombre de entrada de grupo. Al pasar un nombre de entrada, se restringe la búsqueda al contenido de esa entrada.

En el ejemplo anterior, se pasa el valor default de la sintaxis de RPC \_ C \_ NS \_ \_ como primer parámetro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Esto selecciona la sintaxis del nombre de entrada predeterminado. Actualmente, esta es la única sintaxis de nombre de entrada admitida.

La aplicación cliente puede buscar en la base de datos del servicio de nombres un nombre de interfaz, un UUID o ambos. Si desea que busque una interfaz por nombre, pase la variable de interfaz global que genera el compilador MIDL desde el archivo IDL como el tercer parámetro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Encontrará su declaración en el archivo de encabezado que generó el compilador MIDL cuando generó el código auxiliar del cliente. Si desea que el programa cliente busque solo en UUID, establezca el tercer parámetro en **null**.

Al buscar un UUID en la base de datos del servicio de nombres, establezca el cuarto parámetro de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) en el UUID que desea buscar. Si no está buscando un UUID, establezca este parámetro en **null**.

La función [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) pasa la dirección de un servicio de nombres: identificador de contexto de búsqueda a través de su quinto parámetro. Este parámetro se pasa a otras funciones de RpcNsBindingImport.

En concreto, la siguiente función a la que llamará la aplicación cliente es [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext). Los programas cliente utilizan esta función para recuperar los identificadores de enlace compatibles de la base de datos del servicio de nombres. En el siguiente fragmento de código se muestra cómo se puede llamar a esta función:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Una vez que se ha llamado a la función [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obtener un identificador de enlace, la aplicación cliente puede determinar si el identificador recibido es aceptable. Si no es así, el programa cliente puede ejecutar un bucle y volver a llamar a **RpcNsBindingImportNext** para ver si el servicio de nombres contiene un identificador más adecuado. Para cada llamada a **RpcNsBindingImportNext**, debe haber una llamada correspondiente a RpcNsBindingFree. Una vez finalizada la búsqueda, llame a la función [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) para liberar el contexto de búsqueda.

Una vez que la aplicación cliente tiene un identificador de enlace aceptable, debe comprobar que la aplicación de servidor se está ejecutando. Hay dos métodos que el cliente puede usar para realizar esta comprobación. La primera es llamar a una función en la interfaz de cliente. Si el programa de servidor se está ejecutando, la llamada se completará. De lo contrario, se producirá un error en la llamada. Una manera mejor de comprobar que el servidor está en ejecución es invocar a [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguido de una llamada a [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Para obtener más información sobre la base de datos del servicio de nombres, vea [la base de datos del servicio de nombres RPC](the-rpc-name-service-database.md).

 

 




