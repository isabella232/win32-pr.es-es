---
title: Búsqueda de sistemas host de servidor
description: Buscar sistemas host de servidor mediante enlaces de cadena y consultando una base de datos de servicio de nombres para la ubicación de un programa de servidor.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 180e2e43c0350f55defb74762d6ab1b6b656dafbc1468bcc7f077ed9780a2e98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929994"
---
# <a name="finding-server-host-systems"></a>Búsqueda de sistemas host de servidor

Un sistema host de servidor es el equipo que ejecuta el programa de servidor de la aplicación distribuida. Puede haber uno o varios sistemas host de servidor en una red. La forma en que el programa cliente encuentra un servidor al que conectarse depende de las necesidades del programa.

Hay dos métodos para buscar sistemas host de servidor:

-   Usar información almacenada en cadenas en el código fuente del cliente, variables de entorno o archivos de configuración específicos de la aplicación. La aplicación cliente puede usar los datos de la cadena para crear un enlace entre el cliente y el servidor.
-   Consulta de una base de datos de servicio de nombres para la ubicación de un programa de servidor.

En esta sección se presenta información sobre ambas técnicas en los temas siguientes:

-   [Usar enlaces de cadena](#using-string-bindings)
-   [Importación desde bases de datos de servicio de nombres](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Usar enlaces de cadena

Las aplicaciones pueden crear enlaces a partir de información almacenada en cadenas. La aplicación cliente crea esta información como una cadena y, a continuación, llama a la [**función RpcBindingFromStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) El cliente debe proporcionar la siguiente información para identificar el servidor:

-   Nombre de interfaz, identificador único global (GUID) del objeto o UUID del objeto. Para obtener más información, vea [Generar UUID](generating-interface-uuids.md) de interfaz y [UUID de cadena.](string-uuid.md)
-   Tipo de transporte sobre el que se comunica, como canalizaciones con nombre o TCP/IP. Para obtener más información, [vea Terminología esencial del enlace RPC](essential-rpc-binding-terminology.md) y Selección de una secuencia de [protocolo.](selecting-a-protocol-sequence.md)
-   La dirección de red o el nombre del equipo host del servidor.
-   Punto de conexión del programa de servidor en el equipo host del servidor. Para obtener más información, vea [Buscar puntos de conexión](finding-endpoints.md)y Especificar puntos de [conexión.](specifying-endpoints.md)

(El UUID del objeto y la información del punto de conexión son opcionales).

En los ejemplos siguientes, el *parámetro pszNetworkAddress* y otros parámetros incluyen barras diagonales inversas incrustadas. La barra diagonal inversa es un carácter de escape en el lenguaje de programación C. Se necesitan dos barras diagonales inversas para representar cada carácter de barra diagonal inversa literal individual. La estructura de enlace de cadenas debe contener cuatro caracteres de barra diagonal inversa para representar los dos caracteres de barra diagonal inversa literales que preceden al nombre del servidor.

En el ejemplo siguiente se muestra que el nombre del servidor debe ir precedido de ocho barras diagonales inversas para que aparezcan cuatro caracteres de barra diagonal inversa literales en la estructura de datos de enlace de cadenas después de que la función **sprintf \_ s** procese la cadena.


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

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np: \\ \\ \\ \\ *nombredeservidor* \[ \\ \\ nombre de \\ \\ *canalización pipename*\]

A continuación, el [**cliente llama a RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obtener el identificador de enlace:


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Una función conveniente, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) ensambla el UUID del objeto, la secuencia de protocolo, la dirección de red y el punto de conexión en la sintaxis correcta para la llamada a [**RpcBindingFromStringBinding.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) No tiene que preocuparse de colocar la yand, los dos puntos y los distintos componentes de cada secuencia de protocolo en el lugar correcto; simplemente proporciona las cadenas como parámetros a la función . La biblioteca en tiempo de ejecución incluso asigna la memoria necesaria para el enlace de cadena.


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



Otra función conveniente, [**RpcBindingToStringBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)toma un identificador de enlace como entrada y genera el enlace de cadena correspondiente.

## <a name="importing-from-name-service-databases"></a>Importación desde bases de datos de servicio de nombres

Las bases de datos de servicio de nombres almacenan, entre otras cosas, identificadores de enlace y UUID. La aplicación cliente puede buscar uno o ambos cuando necesite enlazarse al servidor. Para obtener una explicación de la información que almacena un servicio de nombres y el formato de almacenamiento, vea [The RPC Name Service Database](the-rpc-name-service-database.md).

La biblioteca RPC proporciona dos conjuntos de funciones que el programa cliente puede usar para buscar en la base de datos del servicio de nombres. Los nombres de un conjunto comienzan por RpcNsBindingImport. Los nombres del otro conjunto comienzan por RpcNsBindingLookup. La diferencia entre los dos grupos de funciones es que las funciones RpcNsBindingImport devuelven un único identificador de enlace por llamada y las funciones RpcNsBindingLookup devuelven grupos de identificadores por llamada.

Para iniciar una búsqueda con las funciones RpcNsBindingImport, primero llame a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), como se muestra en el fragmento de código siguiente.


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



Cuando las funciones RPC buscan en la base de datos del servicio de nombres, necesitan un lugar para comenzar la búsqueda. En la terminología de RPC, esto se denomina nombre de entrada. El programa cliente pasa el nombre de la entrada como segundo parámetro a [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Este parámetro puede ser **NULL si** desea buscar en toda la base de datos del servicio de nombres. Como alternativa, puede buscar en la entrada del servidor pasando un nombre de entrada de servidor o buscar la entrada de grupo pasando un nombre de entrada de grupo. Pasar un nombre de entrada restringe la búsqueda al contenido de esa entrada.

En el ejemplo anterior, el valor RPC C NS SYNTAX DEFAULT se pasa como primer parámetro \_ \_ a \_ \_ [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Esto selecciona la sintaxis de nombre de entrada predeterminada. Actualmente, esta es la única sintaxis de nombre de entrada admitida.

La aplicación cliente puede buscar en la base de datos del servicio de nombres un nombre de interfaz, un UUID o ambos. Si quiere que busque una interfaz por nombre, pase la variable de interfaz global que el compilador MIDL genera a partir del archivo IDL como tercer parámetro a [**RpcNsBindingImportBegin.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) Encontrará su declaración en el archivo de encabezado que el compilador MIDL generó cuando generó el código auxiliar del cliente. Si desea que el programa cliente busque solo por UUID, establezca el tercer parámetro en **NULL.**

Al buscar un UUID en la base de datos del servicio de nombres, establezca el cuarto parámetro de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) en el UUID que desea buscar. Si no está buscando un UUID, establezca este parámetro en **NULL.**

La [**función RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) pasa la dirección de un identificador de contexto de búsqueda-servicio de nombre a través de su quinto parámetro. Este parámetro se pasa a otras funciones RpcNsBindingImport.

En concreto, la siguiente función que llamaría la aplicación cliente [**es RpcNsBindingImportNext.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) Los programas cliente usan esta función para recuperar identificadores de enlace compatibles de la base de datos del servicio de nombres. El fragmento de código siguiente muestra cómo se podría llamar a esta función:


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Una vez que ha llamado a la [**función RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obtener un identificador de enlace, la aplicación cliente puede determinar si el identificador que recibió es aceptable. Si no es así, el programa cliente puede ejecutar un bucle y llamar de nuevo a **RpcNsBindingImportNext** para ver si el servicio de nombres contiene un identificador más adecuado. Para cada llamada a **RpcNsBindingImportNext**, debe haber una llamada correspondiente a RpcNsBindingFree. Una vez completada la búsqueda, llame a [**la función RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) para liberar el contexto de búsqueda.

Una vez que la aplicación cliente tiene un identificador de enlace aceptable, debe comprobar que la aplicación de servidor se está ejecutando. Hay dos métodos que el cliente puede usar para realizar esta comprobación. La primera es llamar a una función en la interfaz de cliente. Si el programa de servidor se está ejecutando, se completará la llamada. Si no es así, se producirá un error en la llamada. Una mejor manera de comprobar que el servidor se está ejecutando es invocar [**RpcEpResolveBinding,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding)seguido de una llamada a [**RpcMgmtIsServerListening.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening) Para obtener más información sobre la base de datos del servicio de nombres, vea [La base de datos del servicio de nombres RPC](the-rpc-name-service-database.md).

 

 




