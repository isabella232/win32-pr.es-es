---
title: Configuración y recuperación de opciones de Internet
description: En este tema se describe cómo establecer y recuperar opciones de Internet mediante las funciones InternetSetOption e InternetQueryOption.
ms.assetid: b596a4a9-c34a-402a-af76-b930fe5f0901
keywords:
- Configuración y recuperación de opciones de Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9440af59efc763e034615f7919e94c4cfe9227
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482491"
---
# <a name="setting-and-retrieving-internet-options"></a>Configuración y recuperación de opciones de Internet

En este tema se describe cómo establecer y recuperar opciones de Internet mediante las funciones [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) [**e InternetQueryOption.**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)

Las opciones de Internet se pueden establecer o recuperar de un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado o la configuración actual de Microsoft Internet Explorer.

-   [Pasos de implementación](#implementation-steps)
    -   [Elegir opciones de Internet](#choosing-internet-options)
    -   [Elección del identificador HINTERNET](#choosing-the-hinternet-handle)
    -   [Establecer o recuperar las opciones](#setting-or-retrieving-the-options)
-   [Ámbito del identificador HINTERNET](#scope-of-hinternet-handle)
-   [Establecer opciones individuales](#setting-individual-options)
-   [Recuperar opciones individuales](#retrieving-individual-options)
    -   [Ejemplo completo](#complete-sample)
-   [Establecer opciones de conexión](#setting-connection-options)
-   [Recuperar opciones de conexión](#retrieving-connection-options)
-   [Temas relacionados](#related-topics)

## <a name="implementation-steps"></a>Pasos de implementación

Para establecer o recuperar opciones de Internet, complete lo siguiente:

-   [Elegir opciones de Internet](#choosing-internet-options)
-   [Elección del identificador HINTERNET](#choosing-the-hinternet-handle)
-   [Establecer o recuperar las opciones](#setting-or-retrieving-the-options)

### <a name="choosing-internet-options"></a>Elegir opciones de Internet

Dado que hay muchas opciones de Internet, es importante elegir las opciones correctas. Muchas opciones de Internet afectan al comportamiento de las funciones de WinINet y Internet Explorer:

Por ejemplo, puede:

-   Controle la autenticación básica de servidor y proxy estableciendo nombres de usuario y contraseñas.
-   Establezca o recupere la cadena de agente de usuario que usan los servidores para identificar las características de la aplicación cliente o el explorador.
-   Recupere el tipo de identificador del identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.

Para obtener más información y una lista de las opciones de Internet, vea [**Marcas de opción**](option-flags.md).

En Internet Explorer 5 y versiones posteriores, algunas opciones se pueden establecer o recuperar de una conexión a Internet específica mediante las estructuras [**INTERNET \_ PER \_ CONN OPTION \_ \_ LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) e [**INTERNET PER \_ \_ CONN \_ OPTION.**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona) Para obtener más información y una lista de las opciones que se pueden establecer o recuperar de una conexión a Internet específica, vea el **miembro dwOptions** de la estructura [**INTERNET PER \_ \_ CONN \_ OPTION.**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona)

### <a name="choosing-the-hinternet-handle"></a>Elección del identificador HINTERNET

El [**identificador HINTERNET**](appendix-a-hinternet-handles.md) utilizado para establecer o recuperar opciones de Internet determina el ámbito de la operación. Todos los identificadores creados a través de este identificador heredarán las opciones establecidas en este identificador.

Por ejemplo, las aplicaciones cliente que requieren un proxy con autenticación, probablemente no requieran establecer el nombre de usuario y la contraseña del proxy cada vez que la aplicación intenta acceder a un recurso de Internet. Si todas las solicitudes de una conexión determinada se controlan mediante el mismo proxy, establecer el nombre de usuario y la contraseña del proxy en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) de tipo de conexión, es decir, un identificador creado por una llamada a [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), permitiría que las llamadas derivadas de este identificador **HINTERNET** usarían el mismo nombre de usuario y contraseña del proxy. Establecer el nombre de usuario y la contraseña del proxy cada vez que [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) crea un identificador **HINTERNET** requeriría sobrecarga adicional e innecesaria. Tenga en cuenta que si la aplicación usa un proxy que requiere autenticación, debe establecer las credenciales de proxy en cada nueva conexión.

### <a name="setting-or-retrieving-the-options"></a>Establecer o recuperar las opciones

Cuando haya determinado qué opciones de Internet y [**control HINTERNET**](appendix-a-hinternet-handles.md) usar, recupere esas opciones de Internet. Para establecer o recuperar opciones, llame a [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) o [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

## <a name="scope-of-hinternet-handle"></a>Ámbito del identificador HINTERNET

El [**identificador HINTERNET**](appendix-a-hinternet-handles.md) utilizado para establecer o recuperar opciones de Internet determina las acciones para las que las opciones son válidas.

Estos identificadores tienen tres niveles:

-   El identificador [**HINTERNET**](appendix-a-hinternet-handles.md) raíz (creado mediante una llamada a [**InternetOpen)**](/windows/desktop/api/Wininet/nf-wininet-internetopena)contendrá todas las opciones de Internet que afectan a esta instancia de WinINet.
-   [**HINTERNET controla**](appendix-a-hinternet-handles.md) que se conectan a un servidor (creado mediante una llamada a [**InternetConnect)**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [**HINTERNET controla**](appendix-a-hinternet-handles.md) los identificadores asociados a un recurso o enumeración de recursos en un servidor determinado.

Además de los distintos identificadores [**HINTERNET,**](appendix-a-hinternet-handles.md) una aplicación también puede usar **NULL** para establecer o recuperar los valores predeterminados de las opciones de Internet usadas por Internet Explorer y las funciones de WinINet. Al establecer opciones de Internet **cuando se usa NULL** como identificador, se cambian los valores predeterminados de las opciones, que actualmente se almacenan en el Registro. Las aplicaciones cliente no deben usar funciones del Registro para cambiar los valores predeterminados de las opciones de Internet, ya que la implementación de cómo se almacenan las opciones se puede modificar en el futuro.

En la tabla siguiente se muestra el tipo de [**identificadores HINTERNET**](appendix-a-hinternet-handles.md) y el ámbito de las opciones de Internet asociadas a ellos.




| Tipo de identificador | Ámbito | 
|-------------|-------|
| <strong>NULL</strong> | La configuración de la opción predeterminada para Internet Explorer. | 
| INTERNET_HANDLE_TYPE_CONNECT_FTP | La configuración de la opción para esta conexión a un servidor FTP. Estas opciones afectan a las operaciones iniciadas desde este identificador <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET,</strong></a> como las descargas de archivos. | 
| INTERNET_HANDLE_TYPE_CONNECT_GOPHER | La configuración de la opción para esta conexión a un servidor Gopher. Estas opciones afectan a las operaciones iniciadas desde este identificador <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET,</strong></a> como las descargas de archivos.<blockquote>[!Note]<br />Windows XP y Windows Server 2003 R2 y versiones anteriores solo.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_CONNECT_HTTP | La configuración de la opción para esta conexión a un servidor HTTP. Estas opciones afectan a las operaciones iniciadas desde este identificador <a href="appendix-a-hinternet-handles.md"><strong>HINTERNET,</strong></a> como las descargas de archivos. | 
| INTERNET_HANDLE_TYPE_FILE_REQUEST | La configuración de opción asociada a esta solicitud de archivo. | 
| INTERNET_HANDLE_TYPE_FTP_FILE | La configuración de opción asociada a esta descarga de recursos ftp. | 
| INTERNET_HANDLE_TYPE_FTP_FILE_HTML | La configuración de opción asociada a esta descarga de recursos FTP con formato HTML. | 
| INTERNET_HANDLE_TYPE_FTP_FIND | La configuración de opciones asociada a esta búsqueda de archivos en un servidor FTP. | 
| INTERNET_HANDLE_TYPE_FTP_FIND_HTML | La configuración de opción asociada a esta búsqueda de archivos en un servidor FTP con formato HTML. | 
| INTERNET_HANDLE_TYPE_GOPHER_FILE | Configuración de opciones asociada a esta descarga de recursos de Gopher.<blockquote>[!Note]<br />Windows XP y Windows Server 2003 R2 y versiones anteriores solo.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML | La configuración de la opción asociada a esta descarga de recursos de Gopher con formato HTML.<blockquote>[!Note]<br />Windows XP y Windows Server 2003 R2 y versiones anteriores solo.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_GOPHER_FIND | Configuración de opciones asociada a esta búsqueda de archivos en un servidor Gopher.<blockquote>[!Note]<br />Windows XP y Windows Server 2003 R2 y versiones anteriores solo.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML | La configuración de opción asociada a esta búsqueda de archivos en un servidor Gopher con formato HTML.<blockquote>[!Note]<br />Windows XP y Windows Server 2003 R2 y versiones anteriores solo.</blockquote><br /> | 
| INTERNET_HANDLE_TYPE_HTTP_REQUEST | La configuración de opciones asociada a esta solicitud HTTP. | 
| INTERNET_HANDLE_TYPE_INTERNET | La configuración de opciones asociada a esta instancia de las funciones de WinINet. | 




 

## <a name="setting-individual-options"></a>Establecer opciones individuales

Después de determinar las opciones de Internet que desea establecer y el ámbito que desea que se ve afectado por estas opciones, establecer opciones de Internet no es complicado. Todo lo que tendría que hacer es llamar a la función [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) con el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) deseado, la marca de opción de Internet y un búfer que contiene la información que desea establecer.

En el ejemplo siguiente se muestra cómo establecer el nombre de usuario y la contraseña del proxy en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) especificado.


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



## <a name="retrieving-individual-options"></a>Recuperar opciones individuales

Las opciones de Internet se pueden recuperar mediante [**la función InternetQueryOption.**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) Para recuperar las opciones de Internet:

1.  Determine el tamaño de búfer necesario para recuperar la información de la opción de Internet.

    El tamaño del búfer se puede determinar usando **NULL para** la dirección del búfer y pasando un tamaño de búfer de cero.

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

    

4.  Liberar la memoria.
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

1.  Cree una [**estructura \_ INTERNET PER \_ CONN OPTION \_ \_ LIST.**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista)
2.  Asigne la memoria para las opciones individuales de Internet que desea establecer para la conexión.
3.  Establezca las opciones en [**las estructuras INTERNET PER \_ \_ CONN \_ OPTION.**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona)
4.  Establezca las opciones mediante [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).

En el ejemplo de código siguiente se muestra cómo establecer datos de proxy para una conexión LAN.


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



## <a name="retrieving-connection-options"></a>Recuperar opciones de conexión

En Internet Explorer 5 y versiones posteriores, las opciones de Internet se pueden recuperar de una conexión específica. Para recuperar opciones de una conexión determinada:

1.  Cree una [**estructura DE LISTA DE OPCIONES DE INTERNET PER \_ \_ \_ \_ CONN.**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista)
2.  Asigne la memoria para las opciones individuales de Internet que se recuperarán de la conexión.
3.  Especifique las opciones mediante [**las estructuras INTERNET PER \_ \_ CONN \_ OPTION.**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_optiona)
4.  Recupere las opciones mediante [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).
5.  Use los datos de la opción.
6.  Liberar la memoria, asignada para contener los datos de la opción, mediante la [**función GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree)

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones de servidor o los servicios, use [Microsoft Windows servicios HTTP (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de la autenticación](handling-authentication.md)
</dt> <dt>

[Identificadores HINTERNET](appendix-a-hinternet-handles.md)
</dt> </dl>

 

