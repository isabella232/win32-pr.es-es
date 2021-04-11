---
title: Desarrollo de una aplicación WPF con reconocimiento de PPP por monitor
description: Tenga en cuenta que en esta página se trata el desarrollo heredado de WPF para Windows 8.1. Si va a desarrollar aplicaciones de WPF para Windows 10, consulte la documentación más reciente en GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interfaz de usuario de Windows, aplicaciones compatibles con PPP
- Interfaz de usuario de Windows, alta PPP
- Aplicaciones con reconocimiento de PPP
- PPP alto
- escribir aplicaciones Win32 con reconocimiento de PPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149273"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Desarrollo de una aplicación WPF con reconocimiento de PPP por monitor

**API importantes**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **En esta página se trata el desarrollo heredado de WPF para Windows 8.1.** Si va a desarrollar aplicaciones de WPF para Windows 10, consulte la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentación más reciente en github.</a>

 

Windows 8.1 ofrece a los desarrolladores nuevas funciones para crear aplicaciones de escritorio que tengan en cuenta el reconocimiento de PPP por monitor. Con el fin de aprovechar esta funcionalidad, una aplicación por monitor con reconocimiento de PPP debe hacer lo siguiente:

-   Cambiar las dimensiones de la ventana para mantener un tamaño físico que parezca coherente en cualquier pantalla
-   Volver a diseñar y volver a representar gráficos para el nuevo tamaño de la ventana
-   Seleccione las fuentes que se van a escalar correctamente para el nivel de PPP
-   Seleccionar y cargar recursos de mapa de bits adaptados para el nivel de PPP

Para facilitar la creación de una aplicación con reconocimiento de PPP por monitor, Windows 8.1 proporciona el siguiente Win32APIs de Microsoft:

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (o entrada de manifiesto de PPP) establece el proceso en un nivel de reconocimiento de PPP especificado que, a continuación, determina el modo en que Windows escala la interfaz de usuario. Esto sustituye a [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) devuelve el nivel de reconocimiento de PPP. Esto sustituye a [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) devuelve el PPP de un monitor.
-   La notificación de la ventana de [**\_ DPICHANGED de WM**](wm-dpichanged.md) se envía a las aplicaciones compatibles con PPP por monitor cuando la posición de una ventana cambia de modo que la mayor parte de su área intersecte con un monitor con un DPI diferente del PPP antes de que cambie la posición o cuando el usuario mueva el control deslizante de pantalla. Para crear una aplicación que cambie de tamaño y se represente cuando un usuario la mueva a una pantalla diferente, utilice esta notificación.

Para obtener más información sobre los distintos niveles de reconocimiento de PPP admitidos para las aplicaciones de escritorio en Windows 8.1 vea el tema [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

## <a name="dpi-scaling-and-wpf"></a>Escala de PPP y WPF

De forma predeterminada, las aplicaciones de Windows Presentation Foundation (WPF) son compatibles con los valores de PPP del sistema. Para obtener definiciones de los distintos niveles de reconocimiento de PPP, vea el tema [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)). El sistema de gráficos de WPF usa unidades independientes del dispositivo para habilitar la resolución y la independencia del dispositivo. WPF escala cada píxel independiente del dispositivo automáticamente en función de los PPP actuales del sistema. Esto permite que las aplicaciones de WPF se escalen automáticamente cuando el PPP del monitor en el que se encuentra la ventana es el mismo DPI del sistema. Sin embargo, dado que las aplicaciones de WPF son compatibles con los PPP del sistema, la aplicación se escalará mediante el sistema operativo cuando la aplicación se mueva a un monitor con un PPP diferente o cuando se use el control deslizante del panel de control para cambiar el PPP. El escalado en el sistema operativo puede dar lugar a que las aplicaciones WPF parezcan borrosas, especialmente cuando el escalado es no integral. Para evitar el escalado de aplicaciones de WPF, es necesario actualizarla para que sea compatible con el reconocimiento de PPP por monitor.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Tutorial de ejemplo de WPF con reconocimiento de supervisión

El [ejemplo de WPF con reconocimiento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) es una aplicación WPF de ejemplo que se ha actualizado para que sea compatible con los PPP de cada monitor. El ejemplo consta de dos proyectos:

-   NativeHelpers. vcxproj: se trata de un proyecto auxiliar nativo que implementa la funcionalidad básica para crear una aplicación WPF como reconocimiento de PPP por monitor mediante el Win32APIs anterior. El proyecto contiene dos clases:
    -   PerMonDPIHelpers: una clase que proporciona funciones auxiliares para las operaciones relacionadas con PPP, como la recuperación del valor de PPP actual del monitor activo, el establecimiento de un proceso para el reconocimiento de PPP por monitor, etc.
    -   PerMonitorDPIWindow: una clase base derivada de **System. Windows. Window** que implementa la funcionalidad para hacer que una ventana de la aplicación WPF tenga en cuenta el reconocimiento de PPP por monitor. Ajusta el tamaño de la ventana, el tamaño de la representación de gráficos y el tamaño de fuente en función de los PPP del monitor en lugar de los PPP del sistema.
-   WPFApplication. csproj: aplicación WPF de ejemplo que usa PerMonitorDPIWindow (PerMonitorDPIWindow) y muestra cómo se cambia el tamaño de la representación y la ventana de la aplicación cuando la ventana se mueve a un monitor con un PPP diferente o cuando se usa el control deslizante del panel de control para cambiar el PPP.

Para ejecutar el ejemplo, siga estos pasos:

1.  Descargar y descomprimir el [ejemplo de WPF con reconocimiento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
2.  Iniciar Microsoft Visual Studio y seleccionar **archivo > abrir > proyecto o solución**
3.  Busque el directorio que contiene el ejemplo descomprimido. Vaya al directorio denominado para el ejemplo y haga doble clic en el archivo de solución de Visual Studio (. sln).
4.  Presione F7 o use compilar > compilar **solución** para compilar el ejemplo
5.  Presione Ctrl + F5 o use **Debug > iniciar sin depurar** para ejecutar el ejemplo

Para ver el impacto del cambio de PPP en una aplicación WPF que se actualiza para que sea compatible con PPP por monitor mediante la clase base en el ejemplo, mueva la ventana de la aplicación a y desde las pantallas que tienen diferentes ppp. A medida que la ventana se mueve entre monitores, el tamaño de la ventana y la escala de la interfaz de usuario se actualizan en función del DPI de la pantalla mediante el sistema de gráficos escalable de WPF, en lugar de escalarse mediante el sistema operativo. La interfaz de usuario de la aplicación se representa de forma nativa y no aparece borrosa. Si no tiene dos pantallas con distintos PPP, cámbielos cambiando el control deslizante en el panel de control de pantalla. Cambiar el control deslizante y hacer clic en **aplicar** cambiará el tamaño de la ventana de la aplicación y actualizará automáticamente la escala de la interfaz de usuario.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Actualizar una aplicación de WPF existente para que sea compatible con PPP por monitor mediante el proyecto auxiliar en el ejemplo de WPF

Si tiene una aplicación de WPF existente y desea aprovechar el proyecto auxiliar de PPP del ejemplo para que sea compatible con los PPP, siga estos pasos.

1.  Descargar y descomprimir el ejemplo de WPF con reconocimiento de monitor
2.  Inicie Visual Studio y seleccione **archivo > abrir > proyecto o solución**
3.  Busque el directorio que contiene una aplicación de WPF existente y haga doble clic en el archivo de solución de Visual Studio (. sln).
4.  Haga clic con el botón derecho en la **solución > agregar > proyecto existente** ![ una captura de pantalla que muestra la selección del menú Agregar: proyecto existente.](images/scrvs-image1.png)
5.  En el cuadro de diálogo de selección de archivo, busque el directorio que contiene el ejemplo descomprimido. Abra el directorio denominado para el ejemplo, vaya a la carpeta "NativeHelpers", seleccione el archivo de proyecto de Visual C++ "NativeHelpers. vcxproj" y haga clic en **Aceptar** .
6.  Haga clic con el botón derecho en el proyecto NativeHelpers y seleccione **compilar**. Se generará NativeHelpers.dll que se agregará como referencia a la aplicación WPF en el paso siguiente ![ una captura de pantalla que ilustra la selección del menú compilar.](images/scrvs-image2.png)
7.  Agregue una referencia a NativeHelpers.dll desde la aplicación WPF. Expanda el proyecto de aplicación WPF, haga clic con el botón derecho en **referencias** y haga clic en **Agregar referencia..** .
8.  En el cuadro de diálogo resultante, expanda la sección **solución** . En **proyectos**, seleccione NativeHelpers y haga clic en **Aceptar** ![ una captura de pantalla que ilustra el cuadro de diálogo Administrador de recursos.](images/scrvs-image3.png)
9.  Expanda el proyecto de aplicación de WPF, expanda **propiedades** y Abra **AssemblyInfo. CS**. Realice las siguientes adiciones a AssemblyInfo. cs.
    -   Agregar referencia a System. Windows. media en la sección de referencia (mediante System. Windows. Media;)
    -   Agregue el atributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )

    ![una captura de pantalla que ilustra las propiedades adicionales](images/scrvs-image4.png)
10. Heredar la clase de ventana principal de WPF de la clase base PerMonitorDPIWindow
    -   Actualice el archivo. CS de la ventana principal de WPF para que herede de la clase base PerMonitorDPIWindow
        -   Agregue una referencia a NativeHelpers en la sección de referencia agregando la línea `using NativeHelpers;`
        -   Heredar la clase de ventana principal de la clase PerMonitorDPIWindow

        ![una captura de pantalla que ilustra la referencia de c++](images/scrvs-image5.png)
    -   Actualice el archivo. XAML de la ventana principal de WPF para que herede de la clase base PerMonitorDPIWindow
        -   Agregue una referencia a NativeHelpers en la sección de referencia agregando la línea `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Heredar la clase de ventana principal de la clase PerMonitorDPIWindow

        ![una captura de pantalla que ilustra cómo agregar la referencia de. Xaml](images/scrvs-image6.png)
11. Presione F7 o use compilar > compilar **solución** para compilar el ejemplo
12. Presione Ctrl + F5 o use **Debug > iniciar sin depurar** para ejecutar el ejemplo

La aplicación de [ejemplo de WPF con reconocimiento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) muestra cómo se puede actualizar una aplicación de WPF para que sea compatible con el reconocimiento de PPP por monitor respondiendo a la notificación de ventana de [**\_ DPICHANGED de WM**](wm-dpichanged.md) . En respuesta a la notificación de ventana, el ejemplo actualiza la transformación de escala que usa WPF en función del DPI actual del monitor en el que se encuentra la ventana. El *wParam* de la notificación de ventana contiene el nuevo PPP en el *wParam*. *LParam* contiene un rectángulo con el tamaño y la posición de la nueva ventana sugerida, escalada para el nuevo dpi.

Nota:

> [!Note]  
> Dado que este ejemplo sobrescribe el tamaño de la ventana y la transformación de escala del nodo raíz de la ventana de WPF, el desarrollador de aplicaciones puede necesitar más trabajo si:
>
> -   El tamaño de la ventana afecta a otras partes de la aplicación como esta ventana de WPF que se hospeda dentro de otra aplicación.
> -   La aplicación WPF que está ampliando esta clase está estableciendo otra transformación en el visual raíz. es posible que el ejemplo sobrescriba otra transformación que esté siendo aplicada por la propia aplicación WPF.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Información general sobre el proyecto auxiliar en el ejemplo de WPF

Para hacer que una aplicación WPF existente por monitor sea compatible con PPP, la biblioteca NativeHelpers proporciona la funcionalidad siguiente:

-   **Marca la aplicación WPF según el reconocimiento de PPP por ponitor:** La aplicación WPF se marca como con reconocimiento de PPP por monitor mediante una llamada a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) para el proceso actual. Al marcar la aplicación como compatible con PPP por monitor, se asegurará de que

    -   El sistema operativo no escala la aplicación cuando el PPP del sistema no coincide con el PPP actual del monitor en el que está la ventana de la aplicación
    -   El mensaje de [**\_ DPICHANGED de WM**](wm-dpichanged.md) se envía cada vez que cambia el PPP de la ventana

-   **Ajusta la dimensión de la ventana, vuelve a crear el diseño y vuelve a representar el contenido de los gráficos y selecciona fuentes basadas en los PPP iniciales del monitor en el que se encuentra la ventana:** Una vez que la aplicación se marca como con reconocimiento de PPP por monitor, WPF seguirá escalando el tamaño de la ventana, los gráficos y el tamaño de fuente en función de los PPP del sistema. Dado que, al iniciarse la aplicación, no se garantiza que el valor de PPP del sistema sea el mismo que el valor de PPP del monitor en el que se inicia la ventana, la biblioteca ajusta estos valores una vez que se carga la ventana. La clase base **PerMonitorDPIWindow** los actualiza en el controlador **alloaded ()** .

    El tamaño de la ventana se actualiza cambiando las propiedades de **ancho** y **alto** de la ventana. El diseño y el tamaño se actualizan aplicando una transformación de escala adecuada al nodo raíz de la ventana de WPF.

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   **Responde a WM \_ Notificación de ventana de DPICHANGED:** actualice el tamaño de la ventana, los gráficos y el tamaño de fuente en función de los PPP pasados en la notificación de ventana. La clase base **PerMonitorDPIWindow** controla la notificación de ventana en el método **HandleMessages ()** .

    El tamaño de la ventana se actualiza mediante una llamada a **SetWindowPos** mediante la información que se pasa en el *lParam* del mensaje de ventana. El diseño y el tamaño de los gráficos se actualizan aplicando una transformación de escala adecuada al nodo raíz de la ventana de WPF. El factor de escala se calcula utilizando los PPP pasados en el *wParam* del mensaje de ventana.

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Controlar el cambio de PPP para activos como imágenes

Para actualizar el contenido de los gráficos, la aplicación WPF de ejemplo aplica una transformación de escala al nodo raíz de la aplicación WPF. Aunque esto funciona bien para el contenido representado de forma nativa por WPF (rectángulo, texto, etc.), esto implica que WPF escala los recursos de mapa de bits como imágenes.

Con el fin de evitar los mapas de bits desenfocados causados por el escalado, el desarrollador de aplicaciones WPF puede escribir un control de imagen PPP personalizado que seleccione un recurso diferente en función del valor de PPP actual del monitor en el que se encuentra la ventana. El control de imagen puede basarse en el evento **DPIChanged ()** que se desencadena para la ventana de WPF que usa desde **PerMonitorDPIWindow**, cuando cambia el PPP.

> [!Note]  
> El control imagen también debe seleccionar el control derecho durante el inicio de la aplicación en el controlador de eventos de la ventana de WPF **cargado ()** .

 

 

 