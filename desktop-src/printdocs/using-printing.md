---
description: En esta sección se describe cómo imprimir desde un programa de escritorio de Windows nativo.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Impresión de aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668437"
---
# <a name="desktop-app-printing"></a><span data-ttu-id="ec8e5-103">Impresión de aplicaciones de escritorio</span><span class="sxs-lookup"><span data-stu-id="ec8e5-103">Desktop App Printing</span></span>

<span data-ttu-id="ec8e5-104">En esta sección se describe cómo imprimir desde un programa de escritorio de Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-104">This section describes how to print from a native Windows desktop program.</span></span>

## <a name="overview"></a><span data-ttu-id="ec8e5-105">Información general</span><span class="sxs-lookup"><span data-stu-id="ec8e5-105">Overview</span></span>

<span data-ttu-id="ec8e5-106">Para proporcionar la mejor experiencia de usuario al imprimir desde un programa nativo de Windows, el programa debe estar diseñado para imprimir desde un subproceso dedicado.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-106">To provide the best user experience when you print from a native Windows program, the program must be designed to print from a dedicated thread.</span></span> <span data-ttu-id="ec8e5-107">En un programa nativo de Windows, el programa es responsable de administrar los mensajes y eventos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-107">In a native Windows program, the program is responsible for managing user interface events and messages.</span></span> <span data-ttu-id="ec8e5-108">Las operaciones de impresión pueden requerir períodos de cálculo intensivo a medida que se representa el contenido de la aplicación para la impresora, lo que puede impedir que el programa responda a la interacción del usuario si este procesamiento se realiza en el mismo subproceso que el procesamiento de eventos de la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-108">Printing operations can require periods of intense computation as the application content is rendered for the printer, which can prevent the program from responding to user interaction if this processing is performed in the same thread as event processing of the user interaction.</span></span>

<span data-ttu-id="ec8e5-109">Si ya está familiarizado con la forma de escribir un programa de Windows nativo con varios subprocesos, puede ir directamente a [Cómo imprimir desde una aplicación de Windows](how-to--print-from-a-windows-application.md) y obtener información sobre cómo agregar la funcionalidad de impresión a su programa.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-109">If you are already familiar with how to write a multi-threaded native Windows program, you go directly to [How to print from a Windows application](how-to--print-from-a-windows-application.md) and learn how to add printing functionality to your program.</span></span>

### <a name="basic-windows-program-requirements"></a><span data-ttu-id="ec8e5-110">Requisitos básicos de programas de Windows</span><span class="sxs-lookup"><span data-stu-id="ec8e5-110">Basic Windows Program Requirements</span></span>

<span data-ttu-id="ec8e5-111">Para obtener el mejor rendimiento y la capacidad de respuesta del programa, no realice el procesamiento del trabajo de impresión de un programa en el subproceso que procesa la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-111">For best performance and program responsiveness, do not perform a program's print job processing in the thread that processes user interaction.</span></span>

<span data-ttu-id="ec8e5-112">Esta separación de la impresión de la interacción del usuario influirá en el modo en que el programa administra los datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-112">This separation of printing from user interaction will influence how the program manages the application data.</span></span> <span data-ttu-id="ec8e5-113">Debe comprender perfectamente estas implicaciones antes de empezar a escribir la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-113">You should thoroughly understand these implications before you start writing the application.</span></span> <span data-ttu-id="ec8e5-114">En los temas siguientes se describen los requisitos básicos para controlar la impresión en un subproceso independiente de un programa.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-114">The following topics describe the basic requirements of handling printing in a separate thread of a program.</span></span>

### <a name="windows-program-basics"></a><span data-ttu-id="ec8e5-115">Aspectos básicos de los programas de Windows</span><span class="sxs-lookup"><span data-stu-id="ec8e5-115">Windows Program Basics</span></span>

<span data-ttu-id="ec8e5-116">Un programa nativo de Windows debe proporcionar el procedimiento de ventana principal para procesar los mensajes de ventana que recibe del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-116">A native Windows program must provide the main window procedure to process the window messages that it receives from the operating system.</span></span> <span data-ttu-id="ec8e5-117">Cada ventana de un programa de Windows tiene una función **WndProc** correspondiente que procesa estos mensajes de ventana.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-117">Every window in a Windows program has a corresponding **WndProc** function that processes these window messages.</span></span> <span data-ttu-id="ec8e5-118">El subproceso en el que se ejecuta esta función se denomina interfaz de usuario o subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-118">The thread in which this function runs is called the user interface, or UI, thread.</span></span>

<span data-ttu-id="ec8e5-119">**Usar recursos para cadenas.**</span><span class="sxs-lookup"><span data-stu-id="ec8e5-119">**Use resources for strings.**</span></span>  
<span data-ttu-id="ec8e5-120">Use los recursos de cadena del archivo de recursos del programa en lugar de las constantes de cadena para las cadenas que podrían ser necesarias cambiar cuando se admita otro lenguaje.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-120">Use string resources from the program's resource file instead of string constants for strings that might need to be changed when you support another language.</span></span> <span data-ttu-id="ec8e5-121">Para que un programa pueda utilizar un recurso de cadena como una cadena, el programa debe recuperar el recurso del archivo de recursos y copiarlo en un búfer de memoria local.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-121">Before a program can use a string resource as a string, the program must retrieve the resource from the resource file and copy it to a local memory buffer.</span></span> <span data-ttu-id="ec8e5-122">Esto requiere una programación adicional al principio, pero permite una modificación, traducción y localización más fáciles del programa en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-122">This requires some additional programming in the beginning, but allows for easier modification, translation, and localization of the program in the future.</span></span>  
<span data-ttu-id="ec8e5-123">**Procese los datos en pasos.**</span><span class="sxs-lookup"><span data-stu-id="ec8e5-123">**Process data in steps.**</span></span>  
<span data-ttu-id="ec8e5-124">Procese el trabajo de impresión en pasos que se pueden interrumpir.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-124">Process the print job in steps that can be interrupted.</span></span> <span data-ttu-id="ec8e5-125">Este diseño permite al usuario cancelar una operación de procesamiento prolongada antes de que se complete y evita que el programa bloquee otros programas que podrían estar en ejecución al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-125">This design makes it possible for the user to cancel a long processing operation before it completes and prevents the program from blocking other programs that might be running at the same time.</span></span>  
<span data-ttu-id="ec8e5-126">**Usar datos de usuario de Windows.**</span><span class="sxs-lookup"><span data-stu-id="ec8e5-126">**Use window user data.**</span></span>  
<span data-ttu-id="ec8e5-127">Las aplicaciones de impresión suelen tener varias ventanas y subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-127">Printing applications often have several windows and threads.</span></span> <span data-ttu-id="ec8e5-128">Para mantener los datos disponibles entre los subprocesos y los pasos de procesamiento sin usar variables globales estáticas, haga referencia a las estructuras de datos mediante un puntero de datos que forma parte de la ventana en la que se usan.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-128">To keep the data available between threads and processing steps without using static, global variables, reference the data structures by a data pointer that is part of the window in which they are used.</span></span>  


<span data-ttu-id="ec8e5-129">En el ejemplo de código siguiente se muestra un punto de entrada principal para una aplicación de impresión.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-129">The following code example shows a main entry point for a printing application.</span></span> <span data-ttu-id="ec8e5-130">En este ejemplo se muestra cómo usar recursos de cadena en lugar de constantes de cadena y también se muestra el bucle de mensajes principal que procesa los mensajes de ventana del programa.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-130">This example shows how to use string resources instead of string constants and also shows the main message loop that processes the program's window messages.</span></span>


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a><span data-ttu-id="ec8e5-131">Información del documento</span><span class="sxs-lookup"><span data-stu-id="ec8e5-131">Document Information</span></span>

<span data-ttu-id="ec8e5-132">Los programas nativos de Windows que imprimen deben diseñarse para el procesamiento multiproceso.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-132">Native Windows programs that print should be designed for multi-threaded processing.</span></span> <span data-ttu-id="ec8e5-133">Uno de los requisitos de un diseño multiproceso es proteger los elementos de datos del programa para que sean seguros para que varios subprocesos puedan usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-133">One of the requirements of a multi-threaded design is to protect the program's data elements so that they are safe for multiple threads to use at the same time.</span></span> <span data-ttu-id="ec8e5-134">Puede proteger los elementos de datos mediante el uso de objetos de sincronización y la organización de los datos para evitar conflictos entre los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-134">You can protect data elements by using synchronization objects and organizing the data to avoid conflicts between the threads.</span></span> <span data-ttu-id="ec8e5-135">Al mismo tiempo, el programa debe impedir que se realicen cambios en los datos del programa mientras se imprime.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-135">At the same time, the program must prevent changes to the program data while it is being printed.</span></span> <span data-ttu-id="ec8e5-136">El programa de ejemplo utiliza varias técnicas diferentes de programación multiproceso.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-136">The sample program uses several different multi-threaded programming techniques.</span></span>

 <span data-ttu-id="ec8e5-137">**Eventos de sincronización**</span><span class="sxs-lookup"><span data-stu-id="ec8e5-137">**Synchronization Events**</span></span>  
<span data-ttu-id="ec8e5-138">El programa de ejemplo utiliza eventos, identificadores de subprocesos y funciones de espera para sincronizar el procesamiento entre el subproceso de impresión y el programa principal e indicar que los datos están en uso.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-138">The sample program uses events, thread handles, and wait functions to synchronize the processing between the print thread and the main program and to indicate that the data is in use.</span></span>  
<span data-ttu-id="ec8e5-139">**Mensajes de Windows específicos de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="ec8e5-139">**Application-Specific Windows Messages**</span></span>  
<span data-ttu-id="ec8e5-140">El programa de ejemplo usa mensajes de ventana específicos de la aplicación para que el programa sea más compatible con otros programas nativos de Windows.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-140">The sample program uses application-specific window messages to make the program more compatible with other native Windows programs.</span></span> <span data-ttu-id="ec8e5-141">Dividir el procesamiento en pasos más pequeños y poner en cola esos pasos en el bucle de mensajes de ventana facilita a Windows administrar el procesamiento sin bloquear otras aplicaciones que también podrían estar ejecutándose en el equipo.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-141">Breaking the processing into smaller steps and queuing those steps in the window message loop makes it easier for Windows to manage the processing without blocking other applications that might also be running on the computer.</span></span>  
<span data-ttu-id="ec8e5-142">**Estructuras de datos**</span><span class="sxs-lookup"><span data-stu-id="ec8e5-142">**Data Structures**</span></span>  
<span data-ttu-id="ec8e5-143">El programa de ejemplo no se escribe en un estilo orientado a objetos utilizando objetos y clases, aunque agrupa los elementos de datos en estructuras de datos.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-143">The sample program is not written in an object-oriented style using objects and classes, although it does group data elements into data structures.</span></span> <span data-ttu-id="ec8e5-144">El ejemplo no utiliza un enfoque orientado a objetos para evitar que un enfoque sea mejor o peor que otro.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-144">The sample does not use an object-oriented approach to avoid implying that one approach is better or worse than another.</span></span>  
<span data-ttu-id="ec8e5-145">Puede utilizar las funciones y las estructuras de datos del programa de ejemplo como punto de partida al diseñar el programa.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-145">You can use the functions and data structures of the sample program as a starting point when you design your program.</span></span> <span data-ttu-id="ec8e5-146">Tanto si decide diseñar un programa orientado a objetos como si no, la consideración de diseño importante que debe recordar es agrupar los elementos de datos relacionados para que pueda usarlos de forma segura en diferentes subprocesos según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-146">Whether you decide to design an object-oriented program or not, the important design consideration to remember is to group the related data elements so that you can use them safely in different threads as necessary.</span></span>  


### <a name="printer-device-context"></a><span data-ttu-id="ec8e5-147">Contexto de dispositivo de impresora</span><span class="sxs-lookup"><span data-stu-id="ec8e5-147">Printer Device Context</span></span>

<span data-ttu-id="ec8e5-148">Al imprimir, es posible que desee representar el contenido que se va a imprimir en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-148">When printing, you might want to render the content to be printed to a device context.</span></span> <span data-ttu-id="ec8e5-149">[Cómo: recuperar un contexto de dispositivo de impresora](retrieving-a-printer-device-context.md) describe las distintas formas en que puede obtener un contexto de dispositivo de impresora.</span><span class="sxs-lookup"><span data-stu-id="ec8e5-149">[How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) describes the different ways that you can obtain a printer device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec8e5-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ec8e5-150">Related topics</span></span>



[<span data-ttu-id="ec8e5-151">Cómo imprimir desde una aplicación de Windows</span><span class="sxs-lookup"><span data-stu-id="ec8e5-151">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)


 

 



