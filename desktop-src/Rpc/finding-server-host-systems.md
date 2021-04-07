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
# <a name="finding-server-host-systems"></a><span data-ttu-id="7f579-103">Búsqueda de sistemas host de servidor</span><span class="sxs-lookup"><span data-stu-id="7f579-103">Finding Server Host Systems</span></span>

<span data-ttu-id="7f579-104">Un sistema host de servidor es el equipo que ejecuta el programa de servidor de la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="7f579-104">A server host system is the computer that executes the distributed application's server program.</span></span> <span data-ttu-id="7f579-105">Puede haber uno o varios sistemas host de servidor en una red.</span><span class="sxs-lookup"><span data-stu-id="7f579-105">There may be one or many server host systems on a network.</span></span> <span data-ttu-id="7f579-106">El modo en que el programa cliente encuentra un servidor al que se va a conectar depende de las necesidades de su programa.</span><span class="sxs-lookup"><span data-stu-id="7f579-106">How your client program finds a server to connect to depends on the needs of your program.</span></span>

<span data-ttu-id="7f579-107">Existen dos métodos para buscar sistemas de host de servidor:</span><span class="sxs-lookup"><span data-stu-id="7f579-107">There are two methods of finding server host systems:</span></span>

-   <span data-ttu-id="7f579-108">Uso de la información almacenada en cadenas en el código fuente del cliente, variables de entorno o archivos de configuración específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7f579-108">Using information stored in strings in the client source code, environment variables, or application-specific configuration files.</span></span> <span data-ttu-id="7f579-109">La aplicación cliente puede usar los datos de la cadena para crear un enlace entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="7f579-109">Your client application can use the data in the string to compose a binding between the client and the server.</span></span>
-   <span data-ttu-id="7f579-110">Consultar una base de datos del servicio de nombres para la ubicación de un programa de servidor.</span><span class="sxs-lookup"><span data-stu-id="7f579-110">Querying a name service database for the location of a server program.</span></span>

<span data-ttu-id="7f579-111">En esta sección se presenta información sobre estas dos técnicas en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="7f579-111">This section presents information on both of these techniques in the following topics:</span></span>

-   [<span data-ttu-id="7f579-112">Usar enlaces de cadena</span><span class="sxs-lookup"><span data-stu-id="7f579-112">Using String Bindings</span></span>](#using-string-bindings)
-   [<span data-ttu-id="7f579-113">Importar desde bases de datos de nombre de servicio</span><span class="sxs-lookup"><span data-stu-id="7f579-113">Importing from Name Service Databases</span></span>](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a><span data-ttu-id="7f579-114">Usar enlaces de cadena</span><span class="sxs-lookup"><span data-stu-id="7f579-114">Using String Bindings</span></span>

<span data-ttu-id="7f579-115">Las aplicaciones pueden crear enlaces a partir de la información almacenada en cadenas.</span><span class="sxs-lookup"><span data-stu-id="7f579-115">Applications can create bindings from information stored in strings.</span></span> <span data-ttu-id="7f579-116">La aplicación cliente compone esta información como una cadena y, a continuación, llama a la función [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) .</span><span class="sxs-lookup"><span data-stu-id="7f579-116">Your client application composes this information as a string, then calls the [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) function.</span></span> <span data-ttu-id="7f579-117">El cliente debe proporcionar la siguiente información para identificar el servidor:</span><span class="sxs-lookup"><span data-stu-id="7f579-117">The client must supply the following information to identify the server:</span></span>

-   <span data-ttu-id="7f579-118">El nombre de la interfaz, el identificador único global (GUID) del objeto o el UUID del objeto.</span><span class="sxs-lookup"><span data-stu-id="7f579-118">The interface name, the globally unique identifier (GUID) of the object, or UUID of the object.</span></span> <span data-ttu-id="7f579-119">Para obtener más información, vea generación de UUID de [interfaz](generating-interface-uuids.md) y [UUID de cadena](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="7f579-119">For more information, see [Generating Interface UUIDs](generating-interface-uuids.md) and [String UUID](string-uuid.md).</span></span>
-   <span data-ttu-id="7f579-120">Tipo de transporte que se va a comunicar, como canalizaciones con nombre o TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7f579-120">The transport type to communicate over, such as named pipes or TCP/IP.</span></span> <span data-ttu-id="7f579-121">Para obtener más información, vea [terminología de enlace RPC esencial](essential-rpc-binding-terminology.md) y [seleccionar una secuencia de protocolo](selecting-a-protocol-sequence.md).</span><span class="sxs-lookup"><span data-stu-id="7f579-121">For details, see [Essential RPC Binding Terminology](essential-rpc-binding-terminology.md) and [Selecting a Protocol Sequence](selecting-a-protocol-sequence.md).</span></span>
-   <span data-ttu-id="7f579-122">La dirección de red o el nombre del equipo host del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f579-122">The network address or the name of the server host computer.</span></span>
-   <span data-ttu-id="7f579-123">Extremo del programa de servidor en el equipo host del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f579-123">The endpoint of the server program on the server host computer.</span></span> <span data-ttu-id="7f579-124">Para obtener más información, consulte [búsqueda de puntos de conexión](finding-endpoints.md)y especificación de puntos de [conexión](specifying-endpoints.md).</span><span class="sxs-lookup"><span data-stu-id="7f579-124">For more information, see [Finding Endpoints](finding-endpoints.md), and [Specifying Endpoints](specifying-endpoints.md).</span></span>

<span data-ttu-id="7f579-125">(El UUID del objeto y la información del punto de conexión son opcionales).</span><span class="sxs-lookup"><span data-stu-id="7f579-125">(The object UUID and the endpoint information are optional.)</span></span>

<span data-ttu-id="7f579-126">En los ejemplos siguientes, el parámetro *pszNetworkAddress* y otros parámetros incluyen barras diagonales inversas incrustadas.</span><span class="sxs-lookup"><span data-stu-id="7f579-126">In the following examples, the *pszNetworkAddress* parameter and other parameters include embedded backslashes.</span></span> <span data-ttu-id="7f579-127">La barra diagonal inversa es un carácter de escape en el lenguaje de programación C.</span><span class="sxs-lookup"><span data-stu-id="7f579-127">The backslash is an escape character in the C programming language.</span></span> <span data-ttu-id="7f579-128">Se necesitan dos barras diagonales inversas para representar cada carácter de barra diagonal inversa literal.</span><span class="sxs-lookup"><span data-stu-id="7f579-128">Two backslashes are needed to represent each single literal backslash character.</span></span> <span data-ttu-id="7f579-129">La estructura de enlace de cadena debe contener cuatro caracteres de barra diagonal inversa para representar los dos caracteres de barra diagonal inversa literal que preceden al nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="7f579-129">The string-binding structure must contain four backslash characters to represent the two literal backslash characters that precede the server name.</span></span>

<span data-ttu-id="7f579-130">En el ejemplo siguiente se muestra que el nombre del servidor debe ir precedido por ocho barras diagonales inversas para que aparezcan cuatro caracteres de barra diagonal inversa literal en la estructura de datos de enlace de cadenas después de que la función **sprintf \_ s** procese la cadena.</span><span class="sxs-lookup"><span data-stu-id="7f579-130">The following example shows that the server name must be preceded by eight backslashes so that four literal backslash characters will appear in the string-binding data structure after the **sprintf\_s** function processes the string.</span></span>


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



<span data-ttu-id="7f579-131">En el ejemplo siguiente, el enlace de cadena aparece como:</span><span class="sxs-lookup"><span data-stu-id="7f579-131">In the following example, the string binding appears as:</span></span>

<span data-ttu-id="7f579-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP: \\ \\ \\ \\ *ServerName* \[ \\ \\ Pipe \\ \\ *pipename*\]</span><span class="sxs-lookup"><span data-stu-id="7f579-132">6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_np:\\\\\\\\*servername*\[\\\\pipe\\\\*pipename*\]</span></span>

<span data-ttu-id="7f579-133">Después, el cliente llama a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) para obtener el identificador de enlace:</span><span class="sxs-lookup"><span data-stu-id="7f579-133">The client then calls [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) to obtain the binding handle:</span></span>


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



<span data-ttu-id="7f579-134">Una función conveniente, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) ensambla el UUID del objeto, la secuencia del Protocolo, la dirección de red y el punto de conexión en la sintaxis correcta para la llamada a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span><span class="sxs-lookup"><span data-stu-id="7f579-134">A convenience function, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assembles the object UUID, protocol sequence, network address, and endpoint in the correct syntax for the call to [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).</span></span> <span data-ttu-id="7f579-135">No tiene que preocuparse de colocar la y comercial, los dos puntos y los distintos componentes de cada secuencia de protocolo en el lugar adecuado; basta con proporcionar las cadenas como parámetros a la función.</span><span class="sxs-lookup"><span data-stu-id="7f579-135">You do not have to worry about putting the ampersand, colon, and the various components for each protocol sequence in the right place; you just supply the strings as parameters to the function.</span></span> <span data-ttu-id="7f579-136">La biblioteca en tiempo de ejecución incluso asigna la memoria necesaria para el enlace de cadenas.</span><span class="sxs-lookup"><span data-stu-id="7f579-136">The run-time library even allocates the memory needed for the string binding.</span></span>


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



<span data-ttu-id="7f579-137">Otra función útil, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), toma un identificador de enlace como entrada y genera el enlace de cadena correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7f579-137">Another convenience function, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), takes a binding handle as input and produces the corresponding string binding.</span></span>

## <a name="importing-from-name-service-databases"></a><span data-ttu-id="7f579-138">Importar desde bases de datos de nombre de servicio</span><span class="sxs-lookup"><span data-stu-id="7f579-138">Importing from Name Service Databases</span></span>

<span data-ttu-id="7f579-139">Almacén de bases de datos del servicio de nombres, entre otras cosas, identificadores de enlace y UUID.</span><span class="sxs-lookup"><span data-stu-id="7f579-139">Name service databases store, among other things, binding handles and UUIDs.</span></span> <span data-ttu-id="7f579-140">La aplicación cliente puede buscar uno o ambos de ellos cuando sea necesario enlazar con el servidor.</span><span class="sxs-lookup"><span data-stu-id="7f579-140">Your client application can search for either or both of these when it needs to bind to the server.</span></span> <span data-ttu-id="7f579-141">Para obtener una explicación de la información que almacena un servicio de nombres y el formato de almacenamiento, consulte [la base de datos del servicio de nombres de RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="7f579-141">For a discussion of the information that a name service stores, and the storage format, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

<span data-ttu-id="7f579-142">La biblioteca RPC proporciona dos conjuntos de funciones que el programa cliente puede utilizar para buscar en la base de datos del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7f579-142">The RPC library provides two sets of functions that your client program can use to search the name service database.</span></span> <span data-ttu-id="7f579-143">Los nombres de un conjunto comienzan por RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="7f579-143">The names of one set begin with RpcNsBindingImport.</span></span> <span data-ttu-id="7f579-144">Los nombres del otro conjunto comienzan por RpcNsBindingLookup.</span><span class="sxs-lookup"><span data-stu-id="7f579-144">The names of the other set begin with RpcNsBindingLookup.</span></span> <span data-ttu-id="7f579-145">La diferencia entre los dos grupos de funciones es que las funciones RpcNsBindingImport devuelven un único identificador de enlace por llamada y las funciones RpcNsBindingLookup devuelven grupos de identificadores por llamada.</span><span class="sxs-lookup"><span data-stu-id="7f579-145">The difference between the two groups of functions is that the RpcNsBindingImport functions return a single binding handle per call and the RpcNsBindingLookup functions return groups of handles per call.</span></span>

<span data-ttu-id="7f579-146">Para iniciar una búsqueda con las funciones de RpcNsBindingImport, llame primero a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), como se muestra en el fragmento de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="7f579-146">To begin a search with the RpcNsBindingImport functions, first call [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), as shown in the following code fragment.</span></span>


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



<span data-ttu-id="7f579-147">Cuando las funciones RPC buscan en la base de datos del servicio de nombres, necesitan un lugar para comenzar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7f579-147">When the RPC functions search the name service database, they need a place to begin the search.</span></span> <span data-ttu-id="7f579-148">En la terminología de RPC, esto se denomina nombre de entrada.</span><span class="sxs-lookup"><span data-stu-id="7f579-148">In RPC terminology, this is called the entry name.</span></span> <span data-ttu-id="7f579-149">El programa cliente pasa el nombre de la entrada como el segundo parámetro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="7f579-149">Your client program passes the entry name as the second parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="7f579-150">Este parámetro puede ser **null** si desea buscar en toda la base de datos del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7f579-150">This parameter can be **NULL** if you want to search the entire name service database.</span></span> <span data-ttu-id="7f579-151">Como alternativa, puede buscar en la entrada del servidor pasando un nombre de entrada de servidor o buscar en la entrada de grupo pasando un nombre de entrada de grupo.</span><span class="sxs-lookup"><span data-stu-id="7f579-151">Alternatively, you can search the server entry by passing a server-entry name or search the group entry by passing a group-entry name.</span></span> <span data-ttu-id="7f579-152">Al pasar un nombre de entrada, se restringe la búsqueda al contenido de esa entrada.</span><span class="sxs-lookup"><span data-stu-id="7f579-152">Passing an entry name restricts the search to the contents of that entry.</span></span>

<span data-ttu-id="7f579-153">En el ejemplo anterior, se pasa el valor default de la sintaxis de RPC \_ C \_ NS \_ \_ como primer parámetro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="7f579-153">In the preceding example, the value RPC\_C\_NS\_SYNTAX\_DEFAULT is passed as the first parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="7f579-154">Esto selecciona la sintaxis del nombre de entrada predeterminado.</span><span class="sxs-lookup"><span data-stu-id="7f579-154">This selects the default entry name syntax.</span></span> <span data-ttu-id="7f579-155">Actualmente, esta es la única sintaxis de nombre de entrada admitida.</span><span class="sxs-lookup"><span data-stu-id="7f579-155">Currently, this is the only supported entry-name syntax.</span></span>

<span data-ttu-id="7f579-156">La aplicación cliente puede buscar en la base de datos del servicio de nombres un nombre de interfaz, un UUID o ambos.</span><span class="sxs-lookup"><span data-stu-id="7f579-156">Your client application can search the name service database for an interface name, a UUID, or both.</span></span> <span data-ttu-id="7f579-157">Si desea que busque una interfaz por nombre, pase la variable de interfaz global que genera el compilador MIDL desde el archivo IDL como el tercer parámetro a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span><span class="sxs-lookup"><span data-stu-id="7f579-157">If you want to have it search for an interface by name, pass the global interface variable that the MIDL compiler generates from your IDL file as the third parameter to [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina).</span></span> <span data-ttu-id="7f579-158">Encontrará su declaración en el archivo de encabezado que generó el compilador MIDL cuando generó el código auxiliar del cliente.</span><span class="sxs-lookup"><span data-stu-id="7f579-158">You'll find its declaration in the header file that the MIDL compiler generated when it generated the client stub.</span></span> <span data-ttu-id="7f579-159">Si desea que el programa cliente busque solo en UUID, establezca el tercer parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="7f579-159">If you want your client program to search by UUID only, set the third parameter to **NULL**.</span></span>

<span data-ttu-id="7f579-160">Al buscar un UUID en la base de datos del servicio de nombres, establezca el cuarto parámetro de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) en el UUID que desea buscar.</span><span class="sxs-lookup"><span data-stu-id="7f579-160">When searching the name service database for a UUID, set the fourth parameter of [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) to the UUID that you want to search for.</span></span> <span data-ttu-id="7f579-161">Si no está buscando un UUID, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="7f579-161">If you are not searching for a UUID, set this parameter to **NULL**.</span></span>

<span data-ttu-id="7f579-162">La función [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) pasa la dirección de un servicio de nombres: identificador de contexto de búsqueda a través de su quinto parámetro.</span><span class="sxs-lookup"><span data-stu-id="7f579-162">The [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) function passes the address of a name service–search context handle through its fifth parameter.</span></span> <span data-ttu-id="7f579-163">Este parámetro se pasa a otras funciones de RpcNsBindingImport.</span><span class="sxs-lookup"><span data-stu-id="7f579-163">You pass this parameter to other RpcNsBindingImport functions.</span></span>

<span data-ttu-id="7f579-164">En concreto, la siguiente función a la que llamará la aplicación cliente es [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span><span class="sxs-lookup"><span data-stu-id="7f579-164">In particular, the next function your client application would call is [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).</span></span> <span data-ttu-id="7f579-165">Los programas cliente utilizan esta función para recuperar los identificadores de enlace compatibles de la base de datos del servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="7f579-165">Client programs use this function to retrieve compatible binding handles from the name service database.</span></span> <span data-ttu-id="7f579-166">En el siguiente fragmento de código se muestra cómo se puede llamar a esta función:</span><span class="sxs-lookup"><span data-stu-id="7f579-166">The following code fragment demonstrates how this function might be called:</span></span>


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



<span data-ttu-id="7f579-167">Una vez que se ha llamado a la función [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) para obtener un identificador de enlace, la aplicación cliente puede determinar si el identificador recibido es aceptable.</span><span class="sxs-lookup"><span data-stu-id="7f579-167">Once it has called the [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) function to obtain a binding handle, your client application can determine if the handle it received is acceptable.</span></span> <span data-ttu-id="7f579-168">Si no es así, el programa cliente puede ejecutar un bucle y volver a llamar a **RpcNsBindingImportNext** para ver si el servicio de nombres contiene un identificador más adecuado.</span><span class="sxs-lookup"><span data-stu-id="7f579-168">If not, your client program can execute a loop and call **RpcNsBindingImportNext** again to see if the name service contains a more appropriate handle.</span></span> <span data-ttu-id="7f579-169">Para cada llamada a **RpcNsBindingImportNext**, debe haber una llamada correspondiente a RpcNsBindingFree.</span><span class="sxs-lookup"><span data-stu-id="7f579-169">For each call to **RpcNsBindingImportNext**, there must be a corresponding call to RpcNsBindingFree.</span></span> <span data-ttu-id="7f579-170">Una vez finalizada la búsqueda, llame a la función [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) para liberar el contexto de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="7f579-170">When your search is complete, call the [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) function to free the lookup context.</span></span>

<span data-ttu-id="7f579-171">Una vez que la aplicación cliente tiene un identificador de enlace aceptable, debe comprobar que la aplicación de servidor se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="7f579-171">After your client application has an acceptable binding handle, it should check to ensure that the server application is running.</span></span> <span data-ttu-id="7f579-172">Hay dos métodos que el cliente puede usar para realizar esta comprobación.</span><span class="sxs-lookup"><span data-stu-id="7f579-172">There are two methods your client can use to perform this verification.</span></span> <span data-ttu-id="7f579-173">La primera es llamar a una función en la interfaz de cliente.</span><span class="sxs-lookup"><span data-stu-id="7f579-173">The first is to call a function in the client interface.</span></span> <span data-ttu-id="7f579-174">Si el programa de servidor se está ejecutando, la llamada se completará.</span><span class="sxs-lookup"><span data-stu-id="7f579-174">If the server program is running, the call will complete.</span></span> <span data-ttu-id="7f579-175">De lo contrario, se producirá un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="7f579-175">If not, the call will fail.</span></span> <span data-ttu-id="7f579-176">Una manera mejor de comprobar que el servidor está en ejecución es invocar a [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), seguido de una llamada a [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span><span class="sxs-lookup"><span data-stu-id="7f579-176">A better way to verify that the server is running is to invoke [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), followed by a call to [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening).</span></span> <span data-ttu-id="7f579-177">Para obtener más información sobre la base de datos del servicio de nombres, vea [la base de datos del servicio de nombres RPC](the-rpc-name-service-database.md).</span><span class="sxs-lookup"><span data-stu-id="7f579-177">For more information on the name service database, see [The RPC Name Service Database](the-rpc-name-service-database.md).</span></span>

 

 




