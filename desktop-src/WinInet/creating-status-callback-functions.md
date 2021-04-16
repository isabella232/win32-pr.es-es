---
title: Crear funciones de devolución de llamada de estado
description: En este tutorial se describe cómo crear una función de devolución de llamada de estado que se usa para supervisar el estado de una solicitud de Internet.
ms.assetid: 518d0800-5ea6-4327-8459-901e6d9a8a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e46040d9b6f93645e2730af287a1955343ec3a
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105714499"
---
# <a name="creating-status-callback-functions"></a>Crear funciones de devolución de llamada de estado

En este tutorial se describe cómo crear una función de devolución de llamada de estado que se usa para supervisar el estado de una solicitud de Internet.

Las funciones de devolución de llamada de estado reciben devoluciones de llamada de estado en cualquier solicitud de Internet que se originó desde cualquier función WinINet a la que se pasó un valor de contexto distinto de cero.


Los pasos siguientes son necesarios para crear una función de devolución de llamada de estado:

1.  [Defina el valor de contexto.](#defining-the-context-value)
2.  [Cree la función de devolución de llamada de estado.](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a>Definir el valor de contexto

El valor de contexto puede ser cualquier valor entero largo sin signo. Idealmente, el valor de contexto debe identificar qué solicitud se acaba de completar y la ubicación de los recursos asociados, si es necesario.

Una de las formas más útiles de usar el valor de contexto es pasar la dirección de una estructura y convertirla en un valor de **DWORD \_ ptr**. La estructura se puede usar para almacenar información sobre la solicitud, de modo que se pase a la función de devolución de llamada de estado.

La estructura siguiente es un ejemplo de un posible valor de contexto. Los miembros de la estructura se seleccionan teniendo en cuenta la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



En este ejemplo, la función de devolución de llamada de estado tendría acceso al identificador de ventana, lo que le permitiría mostrar una interfaz de usuario. El identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) se podría pasar a otra función que puede descargar el recurso y una matriz de caracteres que se puede usar para pasar información sobre la solicitud.

Los miembros de la estructura se pueden cambiar para ajustarse a las necesidades de una aplicación determinada, por lo que no se ve restringido por este ejemplo.

### <a name="creating-the-status-callback-function"></a>Crear la función de devolución de llamada de estado

La función de devolución de llamada de Estado debe seguir el formato de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback). Para hacerlo:

1.  Escriba una declaración de función para la función de devolución de llamada de estado.

    En el ejemplo siguiente se muestra una declaración de ejemplo.

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  Determine qué hará su función de devolución de llamada de estado. En el caso de las aplicaciones que realizan llamadas asincrónicas, la función de devolución de llamada de Estado debe controlar el valor completo de la solicitud de estado de INTERNET \_ \_ \_ , que indica que se ha completado una solicitud asincrónica. La función de devolución de llamada de estado también se puede usar para realizar un seguimiento del progreso de una solicitud de Internet.

    En general, funciona mejor para usar una instrucción switch con *dwInternetStatus* como valor de modificador y los valores de estado para las instrucciones Case. Dependiendo de los tipos de funciones a las que llama la aplicación, puede omitir algunos de los valores de estado. Para obtener una definición de los distintos valores de estado, consulte la lista en el parámetro *dwInternetStatus* de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).

    La siguiente instrucción switch es un ejemplo de cómo controlar las devoluciones de llamada de estado.

    ``` syntax
    switch (dwInternetStatus)
    {
        case INTERNET_STATUS_REQUEST_COMPLETE:
            // Add code
            break;
        default:
            // Add code
            break;
    }
    ```

3.  Cree el código para controlar los valores de estado.

    El código para controlar cada uno de los valores de estado depende en gran medida del uso previsto de la función de devolución de llamada de estado. En el caso de las aplicaciones que solo están realizando el seguimiento del progreso de una solicitud, es posible que sea necesario escribir una cadena en un cuadro de lista. En el caso de las operaciones asincrónicas, el código debe administrar algunos de los datos devueltos en la devolución de llamada.

    La siguiente función de devolución de llamada de estado usa una función switch para determinar cuál es el valor de estado y crea una cadena que incluye el nombre del valor de estado y la función anterior llamada, que se almacena en el miembro szMemo de la estructura de contexto de solicitud \_ .

    ```C++
    void __stdcall CallMaster(
        HINTERNET hInternet,
        DWORD_PTR dwContext,
        DWORD dwInternetStatus,
        LPVOID lpvStatusInformation,
        DWORD dwStatusInformationLength
    )
    {
        UNREFERENCED_PARAMETER(hInternet);
        UNREFERENCED_PARAMETER(lpvStatusInformation);
        UNREFERENCED_PARAMETER(dwStatusInformationLength);

        REQUEST_CONTEXT *cpContext;
        cpContext = (REQUEST_CONTEXT*)dwContext;
        char szStatusText[80];

        switch (dwInternetStatus)
        {
            case INTERNET_STATUS_CLOSING_CONNECTION:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CLOSING_CONNECTION",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_CONNECTED_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTED_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTING_TO_SERVER:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTING_TO_SERVER",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_CONNECTION_CLOSED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s CONNECTION_CLOSED",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CLOSING:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CLOSING",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_HANDLE_CREATED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s HANDLE_CREATED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_INTERMEDIATE_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s INTERMEDIATE_RESPONSE",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_NAME_RESOLVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s NAME_RESOLVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RECEIVING_RESPONSE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RECEIVING_RESPONSE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESPONSE_RECEIVED:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESPONSE_RECEIVED",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REDIRECT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REDIRECT",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_REQUEST_COMPLETE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_COMPLETE",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_REQUEST_SENT:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s REQUEST_SENT",
                                  cpContext->szMemo);
                break;
            case INTERNET_STATUS_RESOLVING_NAME:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s RESOLVING_NAME",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_SENDING_REQUEST:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s SENDING_REQUEST",
                                  cpContext->szMemo );
                break;
            case INTERNET_STATUS_STATE_CHANGE:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s STATE_CHANGE",
                                  cpContext->szMemo );
                break;
            default:
                StringCchPrintfA( szStatusText,
                                  80,
                                  "%s Unknown Status %d Given",
                                  cpContext->szMemo,
                                  dwInternetStatus);
                break;
        }

        SendDlgItemMessage( cpContext->hWindow,
                          cpContext->nStatusList,
                          LB_ADDSTRING,
                          0, (LPARAM)szStatusText );

    }
    ```

    

4.  Utilice la función [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para establecer la función de devolución de llamada de estado en el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para el que desea recibir devoluciones de llamada de estado.

    En el ejemplo siguiente se muestra cómo establecer una función de devolución de llamada de estado.

    ```C++
    HINTERNET hOpen;                       // Root HINTERNET handle
    INTERNET_STATUS_CALLBACK iscCallback;  // Holds the callback function

    // Create the root HINTERNET handle.
    hOpen = InternetOpen( TEXT("Test Application"),
                          INTERNET_OPEN_TYPE_PRECONFIG,
                          NULL, NULL, 0);

    // Set the status callback function.
    iscCallback = InternetSetStatusCallback( hOpen, (INTERNET_STATUS_CALLBACK)CallMaster );
    ```

    

> [!Note]  
> WinINet no admite implementaciones de servidor. Además, no se debe usar desde un servicio. En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear funciones de devolución de llamada de estado](creating-status-callback-functions.md)
</dt> <dt>

[**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 