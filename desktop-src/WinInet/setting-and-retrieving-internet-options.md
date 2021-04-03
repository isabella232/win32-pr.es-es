---
title: Establecer y recuperar opciones de Internet
description: En este tema se describe cómo establecer y recuperar opciones de Internet mediante las funciones InternetSetOption y InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Establecer y recuperar opciones de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418bf21620cf7b7c4426844c95a39ef1fde04e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904759"
---
# <a name="setting-and-retrieving-internet-options"></a>Establecer y recuperar opciones de Internet

En este tema se describe cómo establecer y recuperar opciones de Internet mediante las funciones [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) y [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) .

Las opciones de Internet se pueden establecer en o recuperar desde un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) especificado o la configuración actual en Microsoft Internet Explorer.

-   [Pasos de implementación](#implementation-steps)
    -   [Elegir opciones de Internet](#choosing-internet-options)
    -   [Elección del controlador HINTERNET](#choosing-the-hinternet-handle)
    -   [Establecimiento o recuperación de las opciones](#setting-or-retrieving-the-options)
-   [Ámbito del identificador de HINTERNET](#scope-of-hinternet-handle)
-   [Establecer opciones individuales](#setting-individual-options)
-   [Recuperación de opciones individuales](#retrieving-individual-options)
    -   [Ejemplo completo](#complete-sample)
-   [Establecer opciones de conexión](#setting-connection-options)
-   [Recuperación de opciones de conexión](#retrieving-connection-options)
-   [Temas relacionados](#related-topics)

## <a name="implementation-steps"></a>Pasos de implementación

Para establecer o recuperar las opciones de Internet, realice lo siguiente:

-   [Elegir opciones de Internet](#choosing-internet-options)
-   [Elección del controlador HINTERNET](#choosing-the-hinternet-handle)
-   [Establecimiento o recuperación de las opciones](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Elegir opciones de Internet

Dado que hay tantas opciones de Internet, es importante elegir las opciones adecuadas. Muchas opciones de Internet afectan al comportamiento de las funciones WinINet e Internet Explorer:

Por ejemplo, puede:

-   Controlar la autenticación básica de servidor y proxy mediante la configuración de nombres de usuario y contraseñas.
-   Establezca o recupere la cadena de agente de usuario utilizada por los servidores para identificar las características de la aplicación cliente o el explorador.
-   Recupera el tipo de identificador del identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.

Para obtener más información y una lista de las opciones de Internet, vea [**marcas de opciones**](option-flags.md).

En Internet Explorer 5 y versiones posteriores, algunas opciones se pueden establecer o recuperar desde una conexión a Internet específica mediante la lista de opciones de [**Internet \_ por \_ \_ \_ cada**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) una de las estructuras de opciones de Internet y [**\_ por \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conexión. Para obtener más información y una lista de opciones que se pueden establecer o recuperar de una conexión a Internet específica, vea el miembro **dwOptions** de la estructura de la [**\_ opción Internet por \_ Conn \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) .

### <a name="choosing-the-hinternet-handle"></a>Elección del controlador HINTERNET

El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que se usa para establecer o recuperar opciones de Internet determina el ámbito de la operación. Todos los identificadores creados a través de este identificador heredarán las opciones establecidas en este controlador.

Por ejemplo, las aplicaciones cliente que requieren un proxy con autenticación, probablemente no requieren el establecimiento del nombre de usuario y la contraseña de proxy cada vez que la aplicación intenta obtener acceso a un recurso de Internet. Si el mismo proxy controla todas las solicitudes de una conexión determinada, el establecimiento del nombre de usuario y la contraseña de proxy en un tipo de conexión [**HINTERNET**](appendix-a-hinternet-handles.md) identificador, es decir, un identificador creado por una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permitiría que cualquier llamada procedente de este controlador **HINTERNET** usara el mismo nombre de usuario y contraseña de proxy. Establecer el nombre de usuario y la contraseña de proxy cada vez que [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) crea un identificador de **HINTERNET** requiere una sobrecarga adicional e innecesaria. Tenga en cuenta que si la aplicación usa un proxy que requiere autenticación, debe establecer las credenciales de proxy en cada nueva conexión.

### <a name="setting-or-retrieving-the-options"></a>Establecimiento o recuperación de las opciones

Cuando haya determinado qué opciones de Internet y identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) usar, recupere esas opciones de Internet. Para establecer o recuperar opciones, llame a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o a [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

## <a name="scope-of-hinternet-handle"></a>Ámbito del identificador de HINTERNET

El identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) que se usa para establecer o recuperar opciones de Internet determina las acciones para las que las opciones son válidas.

Estos identificadores tienen tres niveles:

-   El identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz (creado por una llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena)) incluiría todas las opciones de Internet que afectan a esta instancia de Wininet.
-   [**HINTERNET**](appendix-a-hinternet-handles.md) controla que se conecta a un servidor (creado por una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta))
-   [**HINTERNET**](appendix-a-hinternet-handles.md) controla los identificadores asociados a un recurso o una enumeración de los recursos de un servidor determinado.

Además de los distintos identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , una aplicación también puede usar **null** para establecer o recuperar los valores predeterminados de las opciones de Internet usadas por Internet Explorer y las funciones de Wininet. Al establecer las opciones de Internet cuando se usa **null** como identificador, se cambian los valores predeterminados de las opciones, que se almacenan actualmente en el registro. Las aplicaciones cliente no deben usar funciones del registro para cambiar los valores predeterminados de las opciones de Internet, ya que la implementación de cómo se almacenan las opciones se puede modificar en el futuro.

En la tabla siguiente se enumeran los tipos de identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) y el ámbito de las opciones de Internet asociadas a ellos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de identificador</th>
<th>Ámbito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>NULL</strong></td>
<td>La configuración de opciones predeterminada de Internet Explorer.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_FTP</td>
<td>La configuración de la opción para esta conexión a un servidor FTP. Estas opciones afectan a las operaciones iniciadas desde este identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como descargas de archivos.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_CONNECT_GOPHER</td>
<td>La configuración de la opción para esta conexión a un servidor gopher. Estas opciones afectan a las operaciones iniciadas desde este identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como descargas de archivos.
<blockquote>
[!Note]<br />
Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_CONNECT_HTTP</td>
<td>La configuración de la opción para esta conexión a un servidor HTTP. Estas opciones afectan a las operaciones iniciadas desde este identificador de <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET</strong></a> , como descargas de archivos.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FILE_REQUEST</td>
<td>La configuración de opciones asociada a esta solicitud de archivo.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FILE</td>
<td>La configuración de opciones asociada a esta descarga de recursos FTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FILE_HTML</td>
<td>La configuración de opciones asociada a esta descarga de recursos FTP tiene el formato HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_FTP_FIND</td>
<td>La configuración de opciones asociada a esta búsqueda de archivos en un servidor FTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_FTP_FIND_HTML</td>
<td>La configuración de opciones asociada a esta búsqueda de archivos en un servidor FTP con formato HTML.</td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE</td>
<td>La configuración de opciones asociada a esta descarga de recursos Gopher.
<blockquote>
[!Note]<br />
Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML</td>
<td>La configuración de opciones asociada a esta descarga de recursos Gopher tiene el formato HTML.
<blockquote>
[!Note]<br />
Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND</td>
<td>La configuración de opciones asociada a esta búsqueda de archivos en un servidor gopher.
<blockquote>
[!Note]<br />
Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML</td>
<td>La configuración de opciones asociada a esta búsqueda de archivos en un servidor gopher con formato HTML.
<blockquote>
[!Note]<br />
Solo Windows XP y Windows Server 2003 R2 y versiones anteriores.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>INTERNET_HANDLE_TYPE_HTTP_REQUEST</td>
<td>Configuración de opciones asociada a esta solicitud HTTP.</td>
</tr>
<tr class="odd">
<td>INTERNET_HANDLE_TYPE_INTERNET</td>
<td>Configuración de opciones asociada a esta instancia de las funciones de WinINet.</td>
</tr>
</tbody>
</table>



 

## <a name="setting-individual-options"></a>Establecer opciones individuales

Después de determinar las opciones de Internet que desea establecer y el ámbito que desea que se vea afectado por estas opciones, el establecimiento de opciones de Internet no es complicado. Lo único que debe hacer es llamar a la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) deseado, la marca de opción de Internet y un búfer que contiene la información que desea establecer.

En el ejemplo siguiente se muestra cómo establecer el nombre de usuario y la contraseña de proxy en un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.


```C++
// strUsername is a string buffer of cchMax characters or less.
// It contains the proxy user name.
size_t cchMax = 80;
size_t cchUserLength, cchPasswordLength;
HRESULT hr = StringCchLength(strUsername, cchMax, &cchUserLength);

if (SUCCEEDED(hr))
{
   // hOpen is the HINTERNET handle created by InternetConnect.
   InternetSetOption(hConnect, INTERNET_OPTION_PROXY_USERNAME,
      strUsername, DWORD(cchUserLength)+1);
}
else
{
   // Insert error handling code here.
}

// strPassword is the string buffer that contains the proxy password.
hr = StringCchLength(strPassword, cchMax, &cchPasswordLength);

InternetSetOption(hOpen, INTERNET_OPTION_PROXY_PASSWORD,
    strPassword, DWORD(cchPasswordLength)+1);
```



## <a name="retrieving-individual-options"></a>Recuperación de opciones individuales

Las opciones de Internet se pueden recuperar mediante la función [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) . Para recuperar opciones de Internet:

1.  Determine el tamaño del búfer necesario para recuperar la información de la opción de Internet.

    El tamaño del búfer se puede determinar usando **null** para la dirección del búfer y pasándole un tamaño de búfer de cero.

    ```C++
    DWORD dwSize;
    InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);
    ```

    

    El valor devuelto por [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) es la cantidad de memoria necesaria para recuperar la información, en bytes.

2.  Asigne una memoria para el búfer.
    ```C++
    char *lpszData;
    lpszData = new char[dwSize];
    ```

    

3.  Recupere los datos.
    ```C++
    InternetQueryOption( NULL, 
                         INTERNET_OPTION_USER_AGENT,
                         lpszData, &dwSize );
    ```

    

4.  Libere memoria.
    ```C++
    delete [] lpszData;
    ```

    

### <a name="complete-sample"></a>Ejemplo completo

A continuación se muestra el ejemplo completo usado en la sección anterior. En este ejemplo se muestra cómo recuperar la cadena de agente de usuario predeterminada.


```C++
// This call determines the required buffer size.
DWORD dwSize;
InternetQueryOption(NULL, INTERNET_OPTION_USER_AGENT, NULL, &dwSize);

// Allocate the necessary memory.
char *lpszData;
lpszData = new char[dwSize];

// Call InternetQueryOption again with the provided buffer.
InternetQueryOption( NULL, 
                     INTERNET_OPTION_USER_AGENT,
                     lpszData, &dwSize );

// Insert code here to use the user agent string data.

// Free the allocated memory.
delete [] lpszData;
```



## <a name="setting-connection-options"></a>Establecer opciones de conexión

En Internet Explorer 5 y versiones posteriores, se pueden establecer opciones de Internet para en una conexión específica. Anteriormente, todas las conexiones compartían la misma configuración de opciones de Internet. Para establecer opciones para una conexión determinada:

1.  Cree una estructura de [**\_ lista de \_ \_ opciones \_ de Internet por**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) conexión.
2.  Asigne la memoria para las opciones de Internet individuales que desea establecer para la conexión.
3.  Establezca las opciones de las estructuras de opciones de [**Internet \_ por \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conexión.
4.  Establezca las opciones mediante [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

En el ejemplo de código siguiente se muestra cómo establecer los datos de proxy para una conexión LAN.


```C++
BOOL SetConnectionOptions()
{
    INTERNET_PER_CONN_OPTION_LIST list;
    BOOL    bReturn;
    DWORD   dwBufSize = sizeof(list);

    // Fill the list structure.
    list.dwSize = sizeof(list);

    // NULL == LAN, otherwise connectoid name.
    list.pszConnection = NULL;

    // Set three options.
    list.dwOptionCount = 3;
    list.pOptions = new INTERNET_PER_CONN_OPTION[3];

    // Ensure that the memory was allocated.
    if(NULL == list.pOptions)
    {
        // Return FALSE if the memory wasn't allocated.
        return FALSE;
    }

    // Set flags.
    list.pOptions[0].dwOption = INTERNET_PER_CONN_FLAGS;
    list.pOptions[0].Value.dwValue = PROXY_TYPE_DIRECT |
        PROXY_TYPE_PROXY;

    // Set proxy name.
    list.pOptions[1].dwOption = INTERNET_PER_CONN_PROXY_SERVER;
    list.pOptions[1].Value.pszValue = TEXT("https://proxy:80");

    // Set proxy override.
    list.pOptions[2].dwOption = INTERNET_PER_CONN_PROXY_BYPASS;
    list.pOptions[2].Value.pszValue = TEXT("local");

    // Set the options on the connection.
    bReturn = InternetSetOption(NULL,
        INTERNET_OPTION_PER_CONNECTION_OPTION, &list, dwBufSize);

    // Free the allocated memory.
    delete [] list.pOptions;

    return bReturn;
}
```



## <a name="retrieving-connection-options"></a>Recuperación de opciones de conexión

En Internet Explorer 5 y versiones posteriores, las opciones de Internet se pueden recuperar de una conexión específica. Para recuperar opciones de una conexión determinada:

1.  Cree una estructura de [**\_ lista de \_ \_ opciones \_ de Internet por**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) conexión.
2.  Asigne la memoria para las opciones de Internet individuales que se van a recuperar de la conexión.
3.  Especifique las opciones mediante las estructuras de opciones de [**Internet \_ por \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) conexión.
4.  Recupere las opciones mediante [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).
5.  Use los datos de la opción.
6.  Libere la memoria, asignada para contener los datos de la opción, mediante la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlar la autenticación](handling-authentication.md)
</dt> <dt>

[Controladores de HINTERNET](appendix-a-hinternet-handles.md)
</dt> </dl>

 

