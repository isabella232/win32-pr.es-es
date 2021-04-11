---
title: Sesiones HTTP
description: Se tiene acceso a los recursos del WWW mediante http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149386"
---
# <a name="http-sessions"></a>Sesiones HTTP

WinINet le permite tener acceso a los recursos del World Wide Web (WWW). Se puede tener acceso a estos recursos directamente mediante [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para obtener más información, vea [acceso directo a las direcciones URL](handling-uniform-resource-locators.md)).

Se tiene acceso a los recursos del WWW mediante http. Las funciones HTTP controlan los protocolos subyacentes, a la vez que permiten que la aplicación tenga acceso a información en WWW. A medida que evoluciona el protocolo HTTP, los protocolos subyacentes se actualizan para mantener el comportamiento de la función.

En el diagrama siguiente se muestran las relaciones de las funciones que se utilizan con el protocolo HTTP. Los cuadros sombreados representan funciones que devuelven los identificadores de [**HINTERNET**](appendix-a-hinternet-handles.md) , mientras que los cuadros simples representan funciones que utilizan el identificador **HINTERNET** creado por la función de la que dependen.

![funciones WinInet utilizadas para http](images/ax-wnt05.png)

Para obtener más información, vea [identificadores de HINTERNET](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Usar las funciones de WinINet para tener acceso a WWW

-   [Iniciar una conexión a WWW](#initiating-a-connection-to-the-www)
-   [Abrir una solicitud](#opening-a-request)
-   [Agregar encabezados de solicitud](#adding-request-headers)
-   [Envío de una solicitud](#sending-a-request)
-   [Publicar datos en el servidor](#posting-data-to-the-server)
-   [Obtención de información acerca de una solicitud](#getting-information-about-a-request)
-   [Descargar recursos desde WWW](#downloading-resources-from-the-www)

Las siguientes funciones se usan durante las sesiones HTTP para tener acceso a WWW.



| Función                                               | Descripción                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Agrega encabezados de solicitud HTTP al identificador de la solicitud HTTP. Esta función requiere un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                 |
| [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Abre un identificador de solicitud HTTP. Esta función requiere un identificador creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Consulta información acerca de una solicitud HTTP. Esta función requiere un identificador creado por la función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Envía la solicitud HTTP especificada al servidor HTTP. Esta función requiere un identificador creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                  |
| [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Muestra cuadros de diálogo predefinidos para las condiciones de error comunes de Internet. Esta función requiere el identificador usado en la llamada a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Iniciar una conexión a WWW

Para iniciar una conexión a WWW, la aplicación debe llamar a la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) en el [**HINTERNET**](appendix-a-hinternet-handles.md) raíz devuelto por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe establecer una sesión http declarando el \_ tipo de servicio http del servicio de Internet \_ . Para obtener más información sobre el uso de [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consulte [uso de InternetConnect](enabling-internet-functionality.md).

### <a name="opening-a-request"></a>Abrir una solicitud

La función [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) abre una solicitud HTTP y devuelve un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que pueden usar las otras funciones http. A diferencia de las otras funciones abiertas (como [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) y [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) no envía la solicitud a Internet cuando se llama. La función [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envía la solicitud y establece una conexión a través de la red.

[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) toma un identificador de sesión http creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y un verbo http, un nombre de objeto, una cadena de versión, un referrer, tipos de aceptación, marcas y valores de contexto.

El verbo HTTP es una cadena que se va a usar en la solicitud. Los verbos HTTP comunes que se usan en las solicitudes incluyen GET, PUT y POST. Si este valor se establece en **null**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa el valor predeterminado get.

El nombre del objeto es una cadena que contiene el nombre del objeto de destino del verbo HTTP especificado. Suele ser un nombre de archivo, un módulo ejecutable o un especificador de búsqueda. Si el nombre de objeto proporcionado es una cadena vacía, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) busca la página predeterminada.

La cadena de versión debe contener la versión HTTP. Si este parámetro es **null**, la función utiliza "" http/1.1 "".

El remitente de referencia especifica la dirección del documento a partir del que se obtuvo el nombre del objeto. Si este parámetro es **null**, no se especifica ningún referencia.

La cadena terminada en **null** que contiene los tipos de aceptación indica los tipos de contenido aceptados por la aplicación. Establecer este parámetro en **null** indica que la aplicación no acepta ningún tipo de contenido. Si se proporciona una cadena vacía, la aplicación indica que solo acepta documentos de tipo "" Text/ \* "". El valor "" Text/ \* "" indica documentos solo de texto, no imágenes u otros archivos binarios.

Los valores de marca controlan el almacenamiento en caché, las cookies y los problemas de seguridad. En el caso de Microsoft Network (MSN), NTLM y otros tipos de autenticación, establezca la marca de [Internet \_ marcar para mantener la \_ \_ conexión](api-flags.md) .

Si se estableció la marca [ \_ \_ Async de marca de Internet](api-flags.md) en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), debe establecerse un valor de contexto distinto de cero para la operación asincrónica correcta.

En el ejemplo siguiente se muestra una llamada de ejemplo a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Agregar encabezados de solicitud

La función [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permite que las aplicaciones agreguen uno o más encabezados de solicitud a la solicitud inicial. Esta función permite a una aplicación anexar encabezados de formato libre adicionales al identificador de la solicitud HTTP; está diseñado para aplicaciones sofisticadas que requieren un control preciso de la solicitud enviada al servidor HTTP.

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) necesita un identificador de solicitud HTTP creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), una cadena que contiene los encabezados, la longitud de los encabezados y los modificadores.

### <a name="sending-a-request"></a>Envío de una solicitud

[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establece una conexión a Internet y envía la solicitud al sitio especificado. Esta función requiere un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) también puede enviar encabezados adicionales u información opcional. La información opcional se utiliza generalmente para las operaciones que escriben información en el servidor, como PUT y POST.

Una vez que [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envía la solicitud, la aplicación puede usar las funciones [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)y [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) en el identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) para descargar los recursos del servidor.

### <a name="posting-data-to-the-server"></a>Publicar datos en el servidor

Para publicar datos en un servidor, el verbo HTTP de la llamada a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) debe ser post o Put. La dirección del búfer que contiene los datos de envío se debe pasar al parámetro *lpOptional* en [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). El parámetro *dwOptionalLength* debe establecerse en el tamaño de los datos.

También puede usar la función [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para publicar datos en un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) enviado mediante [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).

### <a name="getting-information-about-a-request"></a>Obtención de información acerca de una solicitud

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) permite que una aplicación recupere información acerca de una solicitud HTTP. La función requiere un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), un valor de nivel de información y una longitud de búfer. [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) también acepta un búfer que almacena la información y un índice de encabezado basado en cero que enumera varios encabezados con el mismo nombre.

### <a name="downloading-resources-from-the-www"></a>Descargar recursos desde WWW

Después de abrir una solicitud con [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y enviarla al servidor con [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), la aplicación puede usar las funciones [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)y [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) para descargar el recurso desde el servidor http.

En el ejemplo siguiente se descarga un recurso. La función acepta el identificador de la ventana actual, el número de identificación de un cuadro de edición y un identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Usa [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) para determinar el tamaño del recurso y luego lo descarga mediante [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). El contenido se muestra en el cuadro de edición.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 