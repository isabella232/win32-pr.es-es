---
description: En esta sección se describe cómo imprimir desde un programa de escritorio Windows nativo.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Impresión de aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5e0ebab666258f62b1e6bb87497d38a1b521fdde9a7668bb28e3bb3e9868e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112115"
---
# <a name="desktop-app-printing"></a>Impresión de aplicaciones de escritorio

En esta sección se describe cómo imprimir desde un programa de escritorio Windows nativo.

## <a name="overview"></a>Información general

Para proporcionar la mejor experiencia de usuario al imprimir desde un programa Windows nativo, el programa debe diseñarse para imprimir desde un subproceso dedicado. En un programa Windows nativo, el programa es responsable de administrar los mensajes y eventos de la interfaz de usuario. Las operaciones de impresión pueden requerir períodos de cálculo intensas a medida que se representa el contenido de la aplicación para la impresora, lo que puede impedir que el programa responda a la interacción del usuario si este procesamiento se realiza en el mismo subproceso que el procesamiento de eventos de la interacción del usuario.

Si ya está familiarizado con cómo escribir un programa Windows nativo multiproceso, vaya directamente a Cómo imprimir desde una aplicación Windows y aprenda [a](how-to--print-from-a-windows-application.md) agregar funcionalidad de impresión al programa.

### <a name="basic-windows-program-requirements"></a>Requisitos Windows programa básico

Para obtener el mejor rendimiento y capacidad de respuesta del programa, no realice el procesamiento del trabajo de impresión de un programa en el subproceso que procesa la interacción del usuario.

Esta separación de la impresión de la interacción del usuario influirá en la forma en que el programa administra los datos de la aplicación. Debe comprender exhaustivamente estas implicaciones antes de empezar a escribir la aplicación. En los temas siguientes se describen los requisitos básicos para controlar la impresión en un subproceso independiente de un programa.

### <a name="windows-program-basics"></a>Windows Conceptos básicos del programa

Un programa Windows nativo debe proporcionar el procedimiento de ventana principal para procesar los mensajes de ventana que recibe del sistema operativo. Cada ventana de un Windows programa tiene una función **WndProc correspondiente** que procesa estos mensajes de ventana. El subproceso en el que se ejecuta esta función se denomina subproceso de interfaz de usuario o interfaz de usuario.

**Use recursos para cadenas.**  
Use recursos de cadena del archivo de recursos del programa en lugar de constantes de cadena para las cadenas que podrían tener que cambiarse cuando admita otro lenguaje. Para que un programa pueda usar un recurso de cadena como una cadena, el programa debe recuperar el recurso del archivo de recursos y copiarlo en un búfer de memoria local. Esto requiere cierta programación adicional al principio, pero permite una modificación, traducción y localización más sencillas del programa en el futuro.  
**Procese los datos en pasos.**  
Procese el trabajo de impresión en los pasos que se pueden interrumpir. Este diseño permite al usuario cancelar una operación de procesamiento larga antes de que se complete e impide que el programa bloquee otros programas que podrían ejecutarse al mismo tiempo.  
**Usar datos de usuario de ventana.**  
Las aplicaciones de impresión suelen tener varias ventanas y subprocesos. Para mantener los datos disponibles entre subprocesos y pasos de procesamiento sin usar variables estáticas globales, haga referencia a las estructuras de datos mediante un puntero de datos que forma parte de la ventana en la que se usan.  


En el ejemplo de código siguiente se muestra un punto de entrada principal para una aplicación de impresión. En este ejemplo se muestra cómo usar recursos de cadena en lugar de constantes de cadena y también se muestra el bucle de mensajes principal que procesa los mensajes de ventana del programa.


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



### <a name="document-information"></a>Información del documento

Los Windows nativos que se imprimen deben diseñarse para el procesamiento multiproceso. Uno de los requisitos de un diseño multiproceso es proteger los elementos de datos del programa para que sean seguros para que varios subprocesos los usen al mismo tiempo. Puede proteger los elementos de datos mediante el uso de objetos de sincronización y la organización de los datos para evitar conflictos entre los subprocesos. Al mismo tiempo, el programa debe evitar cambios en los datos del programa mientras se imprime. El programa de ejemplo usa varias técnicas de programación multiproceso diferentes.

 **Eventos de sincronización**  
El programa de ejemplo usa eventos, identificadores de subprocesos y funciones de espera para sincronizar el procesamiento entre el subproceso de impresión y el programa principal e indicar que los datos están en uso.  
**Mensajes de Windows específicos de la aplicación**  
El programa de ejemplo usa mensajes de ventana específicos de la aplicación para que el programa sea más compatible con otros programas Windows nativos. Dividir el procesamiento en pasos más pequeños y hacer cola en esos pasos en el bucle de mensajes de ventana facilita a Windows administrar el procesamiento sin bloquear otras aplicaciones que también podrían ejecutarse en el equipo.  
**Estructuras de datos**  
El programa de ejemplo no se escribe en un estilo orientado a objetos mediante objetos y clases, aunque agrupa elementos de datos en estructuras de datos. El ejemplo no usa un enfoque orientado a objetos para evitar implicar que un enfoque es mejor o peor que otro.  
Puede usar las funciones y estructuras de datos del programa de ejemplo como punto de partida al diseñar el programa. Tanto si decide diseñar un programa orientado a objetos como si no, la consideración de diseño importante que debe recordar es agrupar los elementos de datos relacionados para que pueda usarlos de forma segura en distintos subprocesos según sea necesario.  


### <a name="printer-device-context"></a>Contexto del dispositivo de impresora

Al imprimir, es posible que desee representar el contenido que se va a imprimir en un contexto de dispositivo. [Cómo: Recuperar un contexto de dispositivo de](retrieving-a-printer-device-context.md) impresora describe las distintas maneras de obtener un contexto de dispositivo de impresora.

## <a name="related-topics"></a>Temas relacionados



[Cómo imprimir desde una Windows aplicación](how-to--print-from-a-windows-application.md)


 

 



