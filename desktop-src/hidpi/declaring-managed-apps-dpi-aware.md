---
title: Desarrollo de una aplicación WPF con reconocimiento de PPP por monitor
description: Nota Esta página trata el desarrollo heredado de WPF para Windows 8.1. Si está desarrollando aplicaciones wpf para Windows 10, consulte la documentación más reciente sobre GitHub. .
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Windows Interfaz de usuario aplicaciones con reconocimiento de PPP
- Windows Interfaz de usuario, valores altos de PPP
- Aplicaciones con reconocimiento de PPP
- valores altos de PPP
- escritura de aplicaciones Win32 con reconocimiento de PPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575004"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Desarrollo de una aplicación WPF con reconocimiento de PPP por monitor

**API importantes**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **En esta página se trata el desarrollo de WPF heredado para Windows 8.1.** Si está desarrollando aplicaciones wpf para Windows 10, consulte la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentación más reciente sobre GitHub.</a>

 

Windows 8.1 ofrece a los desarrolladores una nueva funcionalidad para crear aplicaciones de escritorio que tienen en cuenta ppp por monitor. Para aprovechar esta funcionalidad, una aplicación compatible con PPP por monitor debe hacer lo siguiente:

-   Cambiar las dimensiones de la ventana para mantener un tamaño físico que parezca coherente en cualquier pantalla
-   Volver a diseño y volver a representar gráficos para el nuevo tamaño de ventana
-   Seleccione las fuentes que se escalan correctamente para el nivel de PPP.
-   Selección y carga de recursos de mapa de bits adaptados al nivel de PPP

Para facilitar la creación de una aplicación compatible con PPP por monitor, Windows 8.1 proporciona las siguientes API de Microsoft Win32:

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (o entrada de manifiesto de PPP) establece el proceso en un nivel de reconocimiento de PPP especificado, que luego determina cómo Windows escala la interfaz de usuario. Esto reemplaza [**a SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)
-   [**GetProcessDpiAwareness devuelve**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) el nivel de reconocimiento de PPP. Esto reemplaza a [**IsProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware)
-   [**GetDpiForMonitor devuelve**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) el valor de PPP de un monitor.
-   La notificación de ventana [**\_ WM PPPCHANGED**](wm-dpichanged.md) se envía a las aplicaciones con reconocimiento de PPP por monitor cuando cambia la posición de una ventana, de modo que la mayor parte de su área forma una intersección con un monitor con un VALOR DE PPP diferente del valor de PPP antes de que cambie la posición o cuando el usuario mueva el control deslizante de pantalla. Para crear una aplicación que cambie de tamaño y se vuelva a representar cuando un usuario la mueve a otra pantalla, use esta notificación.

Para obtener más información sobre los distintos niveles de reconocimiento de PPP admitidos para las aplicaciones de escritorio en Windows 8.1 vea el tema [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

## <a name="dpi-scaling-and-wpf"></a>Escalado de PPP y WPF

Windows Presentation Foundation aplicaciones (WPF) son de forma predeterminada compatible con PPP del sistema. Para obtener definiciones de los distintos niveles de reconocimiento de PPP, consulte el [tema Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)). El sistema de gráficos wpf usa unidades independientes del dispositivo para habilitar la resolución y la independencia del dispositivo. WPF escala automáticamente cada píxel independiente del dispositivo en función de los PPP actuales del sistema. Esto permite que las aplicaciones WPF se escalen automáticamente cuando el VALOR DE PPP del monitor en el que está la ventana es el mismo PPP del sistema. Sin embargo, dado que las aplicaciones WPF tienen en cuenta los valores de ppp del sistema, el sistema operativo escalará la aplicación cuando la aplicación se mueva a un monitor con un PPP diferente o cuando se utilice el control deslizante en el panel de control para cambiar el valor de PPP. El escalado en el sistema operativo puede dar lugar a que las aplicaciones WPF parezcan desenfoque, especialmente cuando el escalado no es integral. Para evitar el escalado de aplicaciones WPF, deben actualizarse para que sean con reconocimiento de PPP por monitor.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Tutorial de ejemplo de WPF por monitor

El [ejemplo de WPF compatible con cada](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) monitor es una aplicación WPF de ejemplo actualizada para que tenga en cuenta ppp por monitor. El ejemplo consta de dos proyectos:

-   NativeHelpers.vcxproj: se trata de un proyecto auxiliar nativo que implementa la funcionalidad principal para que una aplicación WPF sea compatible con PPP según el monitor mediante las api de Win32 anteriores. El proyecto contiene dos clases:
    -   PerMonDPIHelpers: una clase que proporciona funciones auxiliares para operaciones relacionadas con PPP, como recuperar el PPP actual del monitor activo, establecer un proceso para que tenga en cuenta ppp por monitor, etc.
    -   PerMonitorDPIWindow: una clase base derivada de **System.Windows. Ventana** que implementa la funcionalidad para que una ventana de aplicación WPF sea compatible con ppp por monitor. Ajusta el tamaño de la ventana, el tamaño de representación de gráficos y el tamaño de fuente en función de los VALORES DE PPP del monitor en lugar de los PPP del sistema.
-   WPFApplication.csproj: aplicación WPF de ejemplo que consume PerMonitorDPIWindow (PerMonitorDPIWindow) y muestra cómo cambia el tamaño de la ventana de la aplicación y la representación cuando la ventana se mueve a un monitor con un PPP diferente o cuando se usa el control deslizante en el panel de control Mostrar para cambiar el ppp.

Para ejecutar el ejemplo, siga estos pasos:

1.  Descargar y descomprimir el [ejemplo de WPF por monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
2.  Inicie Microsoft Visual Studio y seleccione File > Open > Project/Solution (Abrir **> Project/Solución).**
3.  Vaya al directorio que contiene el ejemplo descomprimido. Vaya al directorio denominado para el ejemplo y haga doble clic en el archivo Visual Studio Solution (.sln).
4.  Presione F7 o use **Build > Build Solution** para compilar el ejemplo.
5.  Presione Ctrl+F5 o use **Depurar > Iniciar sin depurar** para ejecutar el ejemplo.

Para ver el impacto de cambiar PPP en una aplicación WPF que se actualiza para que tenga en cuenta ppp por monitor mediante la clase base del ejemplo, mueva la ventana de la aplicación hacia y desde las pantallas que tienen diferentes DPI. A medida que la ventana se mueve entre monitores, el tamaño de la ventana y la escala de la interfaz de usuario se actualizan en función de los PPP de la pantalla mediante el sistema de gráficos escalable de WPF, en lugar de escalarse por el sistema operativo. La interfaz de usuario de la aplicación se representa de forma nativa y no parece desenfoque. Si no tiene dos pantallas con valores de PPP diferentes, cambie el control deslizante en el panel de control Mostrar. Al cambiar el control deslizante y hacer clic **en Aplicar,** se cambiará el tamaño de la ventana de la aplicación y se actualizará automáticamente la escala de la interfaz de usuario.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Actualización de una aplicación WPF existente para que tenga en cuenta ppp por monitor mediante un proyecto auxiliar en el ejemplo de WPF

Si tiene una aplicación WPF existente y desea aprovechar el proyecto del asistente de PPP del ejemplo para que tenga en cuenta los valores de PPP, siga estos pasos.

1.  Descargar y descomprimir el ejemplo de WPF por monitor
2.  Inicie Visual Studio seleccione **File > Open > Project/Solution (Abrir > Project/Solución).**
3.  Vaya al directorio que contiene una aplicación WPF existente y haga doble clic en el archivo Visual Studio Solution (.sln).
4.  Haga clic con el botón **derecho en > Agregar > existente Project** una captura de pantalla que ilustra la selección del menú ![ Agregar: proyecto existente](images/scrvs-image1.png)
5.  En el cuadro de diálogo de selección de archivos, vaya al directorio que contiene el ejemplo descomprimido. Abra el directorio denominado para el ejemplo, vaya a la carpeta "NativeHelpers", seleccione el archivo de proyecto de Visual C++ "NativeHelpers.vcxproj" y haga clic en **Aceptar.**
6.  Haga clic con el botón derecho en el proyecto NativeHelpers y seleccione **Compilar**. Esto generará una NativeHelpers.dll que se agregará como referencia a la aplicación WPF en el paso siguiente, una captura de pantalla que ilustra la ![ selección del menú de compilación.](images/scrvs-image2.png)
7.  Agregue una referencia a NativeHelpers.dll desde la aplicación WPF. Expanda el proyecto de aplicación wpf, haga clic con el botón derecho **en Referencias y** haga clic en Agregar **referencia...**
8.  En el cuadro de diálogo resultante, expanda la **sección** Solución. En **Proyectos,** seleccione NativeHelpers y haga clic **en Aceptar** en una captura de pantalla que ilustra el cuadro de diálogo del administrador de ![ recursos.](images/scrvs-image3.png)
9.  Expanda el proyecto de aplicación WPF, expanda **Propiedades** y **abra AssemblyInfo.cs**. Realice las siguientes adiciones a AssemblyInfo.cs.
    -   Agregue una referencia al sistema. Windows. Medios en la sección de referencia (mediante System.Windows. Media;)
    -   Agregue el atributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )

    ![una captura de pantalla que ilustra las propiedades adicionales](images/scrvs-image4.png)
10. Heredar la clase de ventana principal de WPF de la clase base PerMonitorDPIWindow
    -   Actualice el archivo .cs de la ventana principal de WPF para heredar de la clase base PerMonitorDPIWindow.
        -   Agregue una referencia a NativeHelpers en la sección de referencia agregando la línea `using NativeHelpers;`
        -   Heredar la clase de ventana principal de la clase PerMonitorDPIWindow

        ![una captura de pantalla que ilustra la referencia de c++](images/scrvs-image5.png)
    -   Actualización del archivo .xaml de la ventana principal de WPF para heredar de la clase base PerMonitorDPIWindow
        -   Agregue una referencia a NativeHelpers en la sección de referencia agregando la línea `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Heredar la clase de ventana principal de la clase PerMonitorDPIWindow

        ![una captura de pantalla que ilustra la adición de la referencia .xaml](images/scrvs-image6.png)
11. Presione F7 o use **Build > Build Solution** para compilar el ejemplo.
12. Presione Ctrl+F5 o use **Depurar > Iniciar sin depurar** para ejecutar el ejemplo.

La aplicación de ejemplo [DE WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) compatible con cada monitor muestra cómo se puede actualizar una aplicación WPF para que tenga en cuenta ppp por monitor respondiendo a la notificación de ventana [**\_ PPPCHANGED de WM.**](wm-dpichanged.md) En respuesta a la notificación de ventana, el ejemplo actualiza la transformación de escala usada por WPF en función del ppp actual del monitor en el que está la ventana. El *wParam de* la notificación de ventana contiene el nuevo PPP en *wParam.* *LParam contiene* un rectángulo que tiene el tamaño y la posición de la nueva ventana sugerida, escalado para el nuevo PPP.

Nota:

> [!Note]  
> Puesto que este ejemplo sobrescribe el tamaño de la ventana y la transformación de escala del nodo raíz de la ventana wpf, el desarrollador de la aplicación puede necesitar más trabajo si:
>
> -   El tamaño de la ventana afecta a otras partes de la aplicación, como esta ventana de WPF, que se hospeda dentro de otra aplicación.
> -   La aplicación WPF que extiende esta clase está estableciendo alguna otra transformación en el objeto visual raíz. el ejemplo puede sobrescribir alguna otra transformación que está aplicando la propia aplicación WPF.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Información general del proyecto auxiliar en el ejemplo de WPF

Para que una aplicación WPF existente tenga en cuenta ppp por monitor, la biblioteca NativeHelpers proporciona la siguiente funcionalidad:

-   **Marca la aplicación WPF como compatible con PPP** según el rendimiento: La aplicación WPF se marca como compatible con PPP según el monitor mediante una llamada a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) para el proceso actual. Marcar la aplicación como compatible con PPP según el monitor garantizará que

    -   El sistema operativo no escala la aplicación cuando el PPP del sistema no coincide con el ppp actual del monitor en el que se encuentra la ventana de la aplicación.
    -   El [**mensaje \_ WM PPPCHANGED**](wm-dpichanged.md) se envía cada vez que cambia el valor de PPP de la ventana.

-   **Ajusta la dimensión de la ventana, vuelve** a diseño y vuelve a representar el contenido de gráficos y selecciona fuentes en función de los PPP iniciales del monitor en el que se encuentra la ventana: Una vez que la aplicación se marca como compatible con PPP según el monitor, WPF escalará el tamaño de la ventana, los gráficos y el tamaño de fuente en función del ppp del sistema. Puesto que, en el inicio de la aplicación, no se garantiza que el VALOR DE PPP del sistema sea el mismo que el valor de PPP del monitor en el que se inicia la ventana, la biblioteca ajusta estos valores una vez cargada la ventana. La clase base **PerMonitorDPIWindow las** actualiza en el **controlador OnLoaded().**

    El tamaño de la ventana se actualiza cambiando las **propiedades Ancho** **y** Alto de la ventana. El diseño y el tamaño se actualizan aplicando una transformación de escala adecuada al nodo raíz de la ventana wpf.

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

    

-   **Responde a WM \_ Notificación de ventana PPPCHANGED:** actualice el tamaño de la ventana, los gráficos y el tamaño de fuente en función del PPP pasado en la notificación de ventana. La clase base **PerMonitorDPIWindow controla** la notificación de ventana en el **método HandleMessages().**

    El tamaño de la ventana se actualiza mediante una llamada **a SetWindowPos** mediante la información que se pasa *en el lparam* del mensaje de ventana. El diseño y el tamaño de los gráficos se actualizan aplicando una transformación de escala adecuada al nodo raíz de la ventana de WPF. El factor de escala se calcula mediante el PPP pasado en *el wparam* del mensaje de ventana.

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

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Control del cambio de PPP para recursos como imágenes

Para actualizar el contenido gráfico, la aplicación WPF de ejemplo aplica una transformación de escala al nodo raíz de la aplicación WPF. Aunque esto funciona bien para el contenido representado de forma nativa por WPF (rectángulo, texto, etc.), esto implica que WPF escala los recursos de mapa de bits como imágenes.

Para evitar mapas de bits desenfocados causados por el escalado, el desarrollador de aplicaciones wpf puede escribir un control de imagen de PPP personalizado que seleccione un recurso diferente en función del PPP actual del monitor en el que se encuentra la ventana. El control de imagen puede basarse en el evento **DPIChanged()** desencadenado para la ventana de WPF que consume desde **PerMonitorDPIWindow**, cuando cambia el valor de PPP.

> [!Note]  
> El control de imagen también debe seleccionar el control correcto durante el inicio de la aplicación en el controlador de eventos de ventana de WPF **Loaded().**

 

 

 