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
# <a name="creating-status-callback-functions"></a><span data-ttu-id="d702d-103">Crear funciones de devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="d702d-103">Creating Status Callback Functions</span></span>

<span data-ttu-id="d702d-104">En este tutorial se describe cómo crear una función de devolución de llamada de estado que se usa para supervisar el estado de una solicitud de Internet.</span><span class="sxs-lookup"><span data-stu-id="d702d-104">This tutorial describes how to create a status callback function used to monitor the status of an Internet request.</span></span>

<span data-ttu-id="d702d-105">Las funciones de devolución de llamada de estado reciben devoluciones de llamada de estado en cualquier solicitud de Internet que se originó desde cualquier función WinINet a la que se pasó un valor de contexto distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="d702d-105">Status callback functions receive status callbacks on any Internet requests that originated from any WinINet function that was passed a nonzero context value.</span></span>


<span data-ttu-id="d702d-106">Los pasos siguientes son necesarios para crear una función de devolución de llamada de estado:</span><span class="sxs-lookup"><span data-stu-id="d702d-106">The following steps are necessary for creating a status callback function:</span></span>

1.  [<span data-ttu-id="d702d-107">Defina el valor de contexto.</span><span class="sxs-lookup"><span data-stu-id="d702d-107">Define the context value.</span></span>](#defining-the-context-value)
2.  [<span data-ttu-id="d702d-108">Cree la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-108">Create the status callback function.</span></span>](#creating-status-callback-functions)

### <a name="defining-the-context-value"></a><span data-ttu-id="d702d-109">Definir el valor de contexto</span><span class="sxs-lookup"><span data-stu-id="d702d-109">Defining the Context Value</span></span>

<span data-ttu-id="d702d-110">El valor de contexto puede ser cualquier valor entero largo sin signo.</span><span class="sxs-lookup"><span data-stu-id="d702d-110">The context value can be any unsigned long integer value.</span></span> <span data-ttu-id="d702d-111">Idealmente, el valor de contexto debe identificar qué solicitud se acaba de completar y la ubicación de los recursos asociados, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="d702d-111">Ideally, the context value should identify what request has just been completed and the location of any associated resources, if needed.</span></span>

<span data-ttu-id="d702d-112">Una de las formas más útiles de usar el valor de contexto es pasar la dirección de una estructura y convertirla en un valor de **DWORD \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="d702d-112">One of the most useful ways to use the context value is to pass the address of a structure and cast it to a **DWORD\_PTR**.</span></span> <span data-ttu-id="d702d-113">La estructura se puede usar para almacenar información sobre la solicitud, de modo que se pase a la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-113">The structure can be used to store information about the request, so that it is passed to the status callback function.</span></span>

<span data-ttu-id="d702d-114">La estructura siguiente es un ejemplo de un posible valor de contexto.</span><span class="sxs-lookup"><span data-stu-id="d702d-114">The following structure is an example of a possible context value.</span></span> <span data-ttu-id="d702d-115">Los miembros de la estructura se seleccionan teniendo en cuenta la función [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="d702d-115">The members of the structure are chosen with the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function in mind.</span></span>


```C++
typedef struct{
    HWND       hWindow;      // Window handle
    int        nStatusList;  // List box control to hold callbacks
    HINTERNET  hResource;    // HINTERNET handle created by InternetOpenUrl
    char       szMemo[512];  // String to store status memo
} REQUEST_CONTEXT;
```



<span data-ttu-id="d702d-116">En este ejemplo, la función de devolución de llamada de estado tendría acceso al identificador de ventana, lo que le permitiría mostrar una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d702d-116">In this example, the status callback function would have access to the window handle, which would allow it to display a user interface.</span></span> <span data-ttu-id="d702d-117">El identificador [**HINTERNET**](appendix-a-hinternet-handles.md) creado por [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) se podría pasar a otra función que puede descargar el recurso y una matriz de caracteres que se puede usar para pasar información sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d702d-117">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) could be passed to another function that can download the resource and an array of characters that can be used to pass information about the request.</span></span>

<span data-ttu-id="d702d-118">Los miembros de la estructura se pueden cambiar para ajustarse a las necesidades de una aplicación determinada, por lo que no se ve restringido por este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d702d-118">The members of the structure can be changed to fit the needs of a particular application, so do not feel constrained by this example.</span></span>

### <a name="creating-the-status-callback-function"></a><span data-ttu-id="d702d-119">Crear la función de devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="d702d-119">Creating the Status Callback Function</span></span>

<span data-ttu-id="d702d-120">La función de devolución de llamada de Estado debe seguir el formato de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="d702d-120">The status callback function must follow the format of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span> <span data-ttu-id="d702d-121">Para hacerlo:</span><span class="sxs-lookup"><span data-stu-id="d702d-121">To do this:</span></span>

1.  <span data-ttu-id="d702d-122">Escriba una declaración de función para la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-122">Write a function declaration for your status callback function.</span></span>

    <span data-ttu-id="d702d-123">En el ejemplo siguiente se muestra una declaración de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d702d-123">The following example shows a sample declaration.</span></span>

    ```C++
    void CALLBACK CallMaster( HINTERNET,
                              DWORD_PTR,
                              DWORD,
                              LPVOID,
                              DWORD );
    ```

    

2.  <span data-ttu-id="d702d-124">Determine qué hará su función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-124">Determine what your status callback function will do.</span></span> <span data-ttu-id="d702d-125">En el caso de las aplicaciones que realizan llamadas asincrónicas, la función de devolución de llamada de Estado debe controlar el valor completo de la solicitud de estado de INTERNET \_ \_ \_ , que indica que se ha completado una solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="d702d-125">For applications that are making asynchronous calls, the status callback function must handle the INTERNET\_STATUS\_REQUEST\_COMPLETE value, which indicates an asynchronous request is complete.</span></span> <span data-ttu-id="d702d-126">La función de devolución de llamada de estado también se puede usar para realizar un seguimiento del progreso de una solicitud de Internet.</span><span class="sxs-lookup"><span data-stu-id="d702d-126">The status callback function can also be used to track the progress of an Internet request.</span></span>

    <span data-ttu-id="d702d-127">En general, funciona mejor para usar una instrucción switch con *dwInternetStatus* como valor de modificador y los valores de estado para las instrucciones Case.</span><span class="sxs-lookup"><span data-stu-id="d702d-127">In general, it works best to use a switch statement with *dwInternetStatus* as the switch value and the status values for the case statements.</span></span> <span data-ttu-id="d702d-128">Dependiendo de los tipos de funciones a las que llama la aplicación, puede omitir algunos de los valores de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-128">Depending on the types of functions your application is calling, you can ignore some of the status values.</span></span> <span data-ttu-id="d702d-129">Para obtener una definición de los distintos valores de estado, consulte la lista en el parámetro *dwInternetStatus* de [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span><span class="sxs-lookup"><span data-stu-id="d702d-129">For a definition of the different status values, see the listing under the *dwInternetStatus* parameter of [*InternetStatusCallback*](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback).</span></span>

    <span data-ttu-id="d702d-130">La siguiente instrucción switch es un ejemplo de cómo controlar las devoluciones de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-130">The following switch statement is an example of how to handle status callbacks.</span></span>

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

3.  <span data-ttu-id="d702d-131">Cree el código para controlar los valores de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-131">Create the code to handle the status values.</span></span>

    <span data-ttu-id="d702d-132">El código para controlar cada uno de los valores de estado depende en gran medida del uso previsto de la función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-132">The code to handle each of the status values depends heavily on your intended use of the status callback function.</span></span> <span data-ttu-id="d702d-133">En el caso de las aplicaciones que solo están realizando el seguimiento del progreso de una solicitud, es posible que sea necesario escribir una cadena en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="d702d-133">For applications that are just tracking the progress of a request, writing a string to a list box might be all you need.</span></span> <span data-ttu-id="d702d-134">En el caso de las operaciones asincrónicas, el código debe administrar algunos de los datos devueltos en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="d702d-134">For asynchronous operations, the code must handle some of the data returned in the callback.</span></span>

    <span data-ttu-id="d702d-135">La siguiente función de devolución de llamada de estado usa una función switch para determinar cuál es el valor de estado y crea una cadena que incluye el nombre del valor de estado y la función anterior llamada, que se almacena en el miembro szMemo de la estructura de contexto de solicitud \_ .</span><span class="sxs-lookup"><span data-stu-id="d702d-135">The following status callback function uses a switch function to determine what the status value is and creates a string that includes the name of the status value and the previous function called, which is stored in the szMemo member of the REQUEST\_CONTEXT structure.</span></span>

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

    

4.  <span data-ttu-id="d702d-136">Utilice la función [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) para establecer la función de devolución de llamada de estado en el identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para el que desea recibir devoluciones de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-136">Use the [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) function to set the status callback function on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle for which you want to receive status callbacks.</span></span>

    <span data-ttu-id="d702d-137">En el ejemplo siguiente se muestra cómo establecer una función de devolución de llamada de estado.</span><span class="sxs-lookup"><span data-stu-id="d702d-137">The following example demonstrates how to set a status callback function.</span></span>

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
> <span data-ttu-id="d702d-138">WinINet no admite implementaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="d702d-138">WinINet does not support server implementations.</span></span> <span data-ttu-id="d702d-139">Además, no se debe usar desde un servicio.</span><span class="sxs-lookup"><span data-stu-id="d702d-139">In addition, it should not be used from a service.</span></span> <span data-ttu-id="d702d-140">En el caso de servicios o implementaciones de servidor, use los [servicios http de Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="d702d-140">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d702d-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d702d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d702d-142">Crear funciones de devolución de llamada de estado</span><span class="sxs-lookup"><span data-stu-id="d702d-142">Creating Status Callback Functions</span></span>](creating-status-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="d702d-143">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="d702d-143">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)
</dt> <dt>

[<span data-ttu-id="d702d-144">*InternetStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="d702d-144">*InternetStatusCallback*</span></span>](/windows/desktop/api/Wininet/nc-wininet-internet_status_callback)
</dt> </dl>

 

 