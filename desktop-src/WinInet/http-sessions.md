---
title: Sesiones HTTP
description: Se accede a los recursos de www mediante http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580161"
---
# <a name="http-sessions"></a>Sesiones HTTP

WinINet le permite acceder a los recursos de World Wide Web (WWW). Se puede acceder a estos recursos directamente mediante [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para obtener más información, vea [Acceso a direcciones URL directamente).](handling-uniform-resource-locators.md)

Se accede a los recursos de www mediante http. Las funciones HTTP controlan los protocolos subyacentes, a la vez que permiten que la aplicación acceda a la información de www. A medida que el protocolo HTTP evoluciona, los protocolos subyacentes se actualizan para mantener el comportamiento de la función.

En el diagrama siguiente se muestran las relaciones de las funciones que se usan con el protocolo HTTP. Los cuadros sombreados representan funciones que devuelven identificadores [**HINTERNET,**](appendix-a-hinternet-handles.md) mientras que los cuadros sin formato representan funciones que usan el identificador **HINTERNET** creado por la función de la que dependen.

![Funciones wininet usadas para http](images/ax-wnt05.png)

Para obtener más información, vea [HINTERNET Handles](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Uso de las funciones de WinINet para acceder a www

-   [Iniciar una conexión a www](#initiating-a-connection-to-the-www)
-   [Abrir una solicitud](#opening-a-request)
-   [Agregar encabezados de solicitud](#adding-request-headers)
-   [Envío de una solicitud](#sending-a-request)
-   [Publicar datos en el servidor](#posting-data-to-the-server)
-   [Obtener información sobre una solicitud](#getting-information-about-a-request)
-   [Descarga de recursos desde WWW](#downloading-resources-from-the-www)

Las siguientes funciones se usan durante las sesiones HTTP para acceder a www.



| Función                                               | Descripción                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Agrega encabezados de solicitud HTTP al identificador de solicitud HTTP. Esta función requiere un identificador creado por [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                 |
| [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Abre un identificador de solicitud HTTP. Esta función requiere un identificador creado por [**InternetConnect.**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Consulta información sobre una solicitud HTTP. Esta función requiere un identificador creado por la [**función HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl.**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Envía la solicitud HTTP especificada al servidor HTTP. Esta función requiere un identificador creado por [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)                                                  |
| [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Muestra cuadros de diálogo predefinidos para condiciones de error comunes de Internet. Esta función requiere el identificador utilizado en la llamada a [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Iniciar una conexión a www

Para iniciar una conexión a WWW, la aplicación debe llamar a la función [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) en la [**raíz HINTERNET**](appendix-a-hinternet-handles.md) devuelta [**por InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) debe establecer una sesión HTTP declarando el tipo de \_ servicio HTTP DE INTERNET \_ SERVICE. Para obtener más información sobre el [**uso de InternetConnect,**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)vea [Uso de InternetConnect.](enabling-internet-functionality.md)

### <a name="opening-a-request"></a>Abrir una solicitud

La [**función HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) abre una solicitud HTTP y devuelve un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que pueden usar las otras funciones HTTP. A diferencia de las otras funciones abiertas (como [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetOpenUrl),**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) no envía la solicitud a Internet cuando se llama a . La [**función HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envía la solicitud y establece una conexión a través de la red.

[**HttpOpenRequest toma**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) un identificador de sesión HTTP creado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) y un verbo HTTP, nombre de objeto, cadena de versión, referencia, tipos de aceptación, marcas y valor de contexto.

El verbo HTTP es una cadena que se usará en la solicitud. Los verbos HTTP comunes que se usan en las solicitudes incluyen GET, PUT y POST. Si este valor se establece en **NULL,** [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa el valor predeterminado GET.

El nombre del objeto es una cadena que contiene el nombre del objeto de destino del verbo HTTP especificado. Suele ser un nombre de archivo, un módulo ejecutable o un especificador de búsqueda. Si el nombre de objeto proporcionado es una cadena vacía, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) busca la página predeterminada.

La cadena de versión debe contener la versión HTTP. Si este parámetro es **NULL,** la función usa ""HTTP/1.1"".

El origen de referencia especifica la dirección del documento del que se obtuvo el nombre del objeto. Si este parámetro es **NULL,** no se especifica ningún referenciador.

La **cadena** terminada en NULL que contiene los tipos de aceptación indica los tipos de contenido aceptados por la aplicación. Establecer este parámetro en **NULL** indica que la aplicación no acepta ningún tipo de contenido. Si se proporciona una cadena vacía, la aplicación indica que solo acepta documentos de tipo ""text/ \* "". El valor ""text/ "" indica documentos de solo \* texto, no imágenes u otros archivos binarios.

Los valores de marca controlan el almacenamiento en caché, las cookies y los problemas de seguridad. Para Microsoft Network (MSN), NTLM y otros tipos de autenticación, establezca la marca [ \_ INTERNET FLAG KEEP \_ \_ CONNECTION.](api-flags.md)

Si la [marca \_ INTERNET FLAG \_ ASYNC](api-flags.md) se estableció en la llamada a [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), se debe establecer un valor de contexto distinto de cero para una operación asincrónica adecuada.

El ejemplo siguiente es una llamada de ejemplo a [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Agregar encabezados de solicitud

La [**función HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permite a las aplicaciones agregar uno o varios encabezados de solicitud a la solicitud inicial. Esta función permite a una aplicación anexar encabezados de formato libre adicionales al identificador de solicitud HTTP; está pensado para su uso por aplicaciones sofisticadas que requieren un control preciso sobre la solicitud enviada al servidor HTTP.

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) necesita un identificador de solicitud HTTP creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), una cadena que contiene los encabezados, la longitud de los encabezados y los modificadores.

### <a name="sending-a-request"></a>Envío de una solicitud

[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establece una conexión a Internet y envía la solicitud al sitio especificado. Esta función requiere un [**identificador HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) [**HttpSendRequest también**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) puede enviar encabezados adicionales o información opcional. La información opcional se usa generalmente para las operaciones que escriben información en el servidor, como PUT y POST.

Una vez [**que HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envía la solicitud, la aplicación puede usar las funciones [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) en el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) para descargar los recursos del servidor.

### <a name="posting-data-to-the-server"></a>Publicar datos en el servidor

Para publicar datos en un servidor, el verbo HTTP de la llamada a [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) debe ser POST o PUT. La dirección del búfer que contiene los datos POST se debe pasar al parámetro *lpOptional* en [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) El *parámetro dwOptionalLength* debe establecerse en el tamaño de los datos.

También puede usar la función [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para publicar datos en un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) enviado mediante [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).

### <a name="getting-information-about-a-request"></a>Obtener información sobre una solicitud

[**HttpQueryInfo permite**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) a una aplicación recuperar información sobre una solicitud HTTP. La función requiere un [**identificador HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) o [**InternetOpenUrl,**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)un valor de nivel de información y una longitud de búfer. [**HttpQueryInfo también**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) acepta un búfer que almacena la información y un índice de encabezado de base cero que enumera varios encabezados con el mismo nombre.

### <a name="downloading-resources-from-the-www"></a>Descarga de recursos desde WWW

Después de abrir una solicitud con [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y enviarla al servidor con [**HttpSendRequest,**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)la aplicación puede usar las funciones [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) para descargar el recurso desde el servidor HTTP.

En el ejemplo siguiente se descarga un recurso. La función acepta el identificador en la ventana actual, el número de identificación de un cuadro de edición y un identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) y enviado por [**HttpSendRequest.**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) Usa [**InternetQueryDataAvailable para**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) determinar el tamaño del recurso y, a continuación, lo descarga [**mediante InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). A continuación, el contenido se muestra en el cuadro de edición.


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
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. Para las implementaciones o servicios de servidor, use [Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 