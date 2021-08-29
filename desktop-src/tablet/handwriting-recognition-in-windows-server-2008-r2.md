---
description: Windows Server 2008 R2 agrega compatibilidad con el reconocimiento de escritura a mano del lado servidor a Windows. En este tema se describe cómo reconocer la escritura a mano Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconocimiento de escritura a mano Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: 9dc13160d909cd7f0ab17b2ca40f0210e3a8f3fc732dcefbcec4d35dee0c26b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008744"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Reconocimiento de escritura a mano Windows Server 2008 R2

Windows Server 2008 R2 admite el reconocimiento de escritura a mano del lado servidor. El reconocimiento del lado servidor permite que un servidor reconozca el contenido de la entrada de lápiz en las páginas web. Esto resulta especialmente útil cuando los usuarios de una red especificarán términos que se interpretan mediante un diccionario personalizado. Por ejemplo, si tuviera una aplicación médica que consultara una base de datos de servidor para buscar nombres de pacientes, esos nombres se podrían agregar a otra base de datos a la que se realizaría una referencia cruzada al realizar búsquedas desde un formulario de Silverlight manuscrito.

## <a name="set-up-your-server-for-server-side-recognition"></a>Configuración del servidor para el Server-Side reconocimiento

Se deben seguir los pasos siguientes para configurar el reconocimiento del lado servidor.

- Instalar Servicios de Escritura con lápiz y Escritura a mano
- Instalar compatibilidad con el servidor web (IIS) y el servidor de aplicaciones
- Habilitación del rol experiencia de escritorio
- Iniciar el servicio de entrada de Tablet PC

### <a name="install-ink-and-handwriting-services"></a>Instalar Servicios de Escritura con lápiz y Escritura a mano

Para instalar los servicios ink y handwriting, abra el administrador del servidor haciendo clic en el icono del administrador del servidor de la bandeja inicio rápido cliente. En el **menú Características,** haga clic **en Agregar características.** Asegúrese de activar la casilla **de Servicios de Escritura con lápiz y Escritura a mano.** En la imagen siguiente se muestra **el cuadro de diálogo** Seleccionar características **Servicios de Escritura con lápiz y Escritura a mano** seleccionado.

![Cuadro de diálogo Seleccionar características con la casilla De entrada de lápiz y servicios de escritura a mano activada](images/setup-server-1-ink-and-handwriting.png)<br/>
*Cuadro de diálogo Seleccionar características con la casilla De entrada de lápiz y servicios de escritura a mano activada*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Compatibilidad con la instalación del servidor web (IIS) y el servidor de aplicaciones

Abra el administrador del servidor como hizo en el primer paso. A continuación, deberá agregar los roles Servidor web (IIS) y Servidor de aplicaciones. En el menú **Roles,** haga clic **en Agregar roles.** Aparece el Asistente para agregar roles. Haga clic en **Next**. Asegúrese de **que el servidor de** aplicaciones y el servidor web **(IIS)** están seleccionados. En la imagen siguiente se muestra **el cuadro de diálogo Seleccionar roles** de servidor con los roles Servidor web **(IIS)** y **Servidor** de aplicaciones seleccionados.

![Cuadro de diálogo Seleccionar roles de servidor con los roles de servidor web (iis) y de servidor de aplicaciones seleccionados](images/setup-server-2-select-server-roles.png)<br/>
*Cuadro de diálogo Seleccionar roles de servidor con los roles de servidor web (iis) y de servidor de aplicaciones seleccionados*

Al seleccionar **Servidor de aplicaciones**, se le pedirá que instale el marco ASP.NET aplicación. Haga clic **en el botón Agregar características necesarias.** Después de hacer **clic en Siguiente,** aparecerá un cuadro de diálogo de información general; Haga clic **en Siguiente.** El **cuadro de diálogo Seleccionar servicios** de rol ahora debe estar disponible. Asegúrese de que **el servidor web (IIS)** está seleccionado. En la imagen siguiente se muestra **el cuadro de diálogo Seleccionar servicios** de rol con servidor web (IIS) habilitado.

![Cuadro de diálogo Seleccionar servicios de rol con el servidor web (iis) habilitado](images/setup-server-3-select-role-services.png)<br/>
*Cuadro de diálogo Seleccionar servicios de rol con el servidor web (iis) habilitado*

Haga clic en **Next**. Aparece un cuadro de diálogo de información general; Haga clic **en Siguiente de** nuevo. Ahora se le mostrará una página que le ofrece opciones para los roles de servidor web (IIS). Haga clic en **Next**. En la página siguiente, el **botón Instalar** se activará. Haga **clic en** Instalar e instalará la compatibilidad con el servidor web (IIS) y el servidor de aplicaciones.

### <a name="enable-the-desktop-experience-role"></a>Habilitación del rol experiencia de escritorio

Para habilitar la experiencia de escritorio, haga clic **en Inicio**, **herramientas administrativas** y, a continuación, haga **clic Administrador del servidor**. Seleccione **Agregar servicios y,** a continuación, seleccione el **servicio Experiencia de** escritorio. En la imagen siguiente se muestra **el cuadro de diálogo Seleccionar** características con el elemento Experiencia de escritorio instalado.

![Cuadro de diálogo Seleccionar características con el servicio de experiencia de escritorio seleccionado](images/setup-server-4-desktop-experience.png)<br/>
*Cuadro de diálogo Seleccionar características con el servicio de experiencia de escritorio seleccionado*

Haga **clic en** Siguiente para instalar la experiencia de escritorio.

### <a name="start-the-tablet-service"></a>Iniciar tablet service

Después de instalar el servicio Experiencia de escritorio, el servicio entrada de Tablet PC aparecerá en el **menú** Servicios. Para acceder al menú **Servicios,** haga clic **en Inicio,** **herramientas administrativas** y, a continuación, en **Servicios.** Para iniciar el servicio, haga clic con el botón derecho en **Servicio de entrada de Tablet PC** y, a continuación, haga clic en **Iniciar**. En la imagen siguiente se muestra el **menú Servicios** con el servicio de entrada de Tablet PC iniciado.

![Menú Servicios con el servicio de entrada de tablet PC iniciado](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Menú Servicios con el servicio de entrada de tablet PC iniciado*

## <a name="performing-server-side-recognition-using-silverlight"></a>Realización Server-Side reconocimiento mediante Silverlight

En esta sección se muestra cómo crear una aplicación web que usa Silverlight para capturar la entrada de escritura a mano. Siga estos pasos para programar el reconocedor en Visual Studio 2008.

- Instale y actualice Visual Studio 2008 para agregar compatibilidad con Silverlight.
- Cree un proyecto de Silverlight en Visual Studio 2008.
- Agregue las referencias de servicio necesarias al proyecto.
- Cree un servicio WCF de Silverlight para el reconocimiento de entrada de lápiz.
- Agregue la referencia de servicio al proyecto de cliente.
- Agregue la clase InkCollector al proyecto InkRecognition.
- Quitar directivas de transporte seguro de la configuración de cliente

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Instalación y actualización de Visual Studio 2008 para agregar compatibilidad con Silverlight

Antes de comenzar, debe realizar los pasos siguientes en el servidor Windows Server 2008 R2.

- Instale Visual Studio 2008.
- Instale [Microsoft Visual Studio Service Pack 1 de 2008.](https://www.microsoft.com/download/details.aspx?id=10986)
- Instale [el SDK de Microsoft Silverlight 5.](https://www.microsoft.com/silverlight/)

Después de instalar estas aplicaciones y actualizaciones, está listo para crear la aplicación web de reconocimiento del lado servidor.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Creación de una instancia de Silverlight Web Project en Visual Studio 2008

En el menú **Archivo**, haga clic en **Nuevo proyecto**. Seleccione la plantilla Aplicación de Silverlight en la lista de proyectos de Visual \# C. Asigne al proyecto el nombre InkRecognition y haga clic **en Aceptar.** En la imagen siguiente se muestra el proyecto de C \# Silverlight seleccionado y denominado InkRecognition.

![Proyecto \# de c silverlight seleccionado, con el nombre inkrecognition](images/project-1-new-project.png)<br/>
*Proyecto \# de c silverlight seleccionado, con el nombre inkrecognition*

Después de hacer **clic en Aceptar**, un cuadro de diálogo le pide que agregue una aplicación de Silverlight al proyecto. Seleccione Agregar un nuevo proyecto ASP.NET web a la solución **para hospedar Silverlight** y haga clic en **Aceptar.** En la imagen siguiente se muestra cómo configurar el proyecto de ejemplo antes de hacer clic **en Aceptar.**

![Cuadro de diálogo con aviso para agregar una aplicación silverlight a un proyecto](images/project-2-add-a-new-aspnetproject.png)<br/>
*Cuadro de diálogo con aviso para agregar una aplicación de Silverlight a un proyecto*

### <a name="add-the-necessary-service-references-to-your-project"></a>Agregue las referencias de servicio necesarias a la Project

Ahora tiene el proyecto de cliente de Silverlight genérico (InkRecognition) con un proyecto web (InkRecognition.Web) configurado en la solución. El proyecto se abrirá con Page.xaml y Default.aspx abiertos. Cierre estas ventanas y agregue las referencias System.Runtime.Serialization y System.ServiceModel al proyecto InkRecognition haciendo clic con el botón derecho en la carpeta references del proyecto InkRecognition y seleccionando **Agregar referencia.** En la imagen siguiente se muestra el cuadro de diálogo con las referencias necesarias seleccionadas.

![Cuadro de diálogo Agregar referencias con system.runtime.serialization y system.servicemodel seleccionados](images/project-3a-add-references-to-inkreco.png)<br/>
*Cuadro de diálogo Agregar referencias con system.runtime.serialization y system.servicemodel seleccionados*

A continuación, debe agregar las referencias System.ServiceModel y Microsoft.Ink al proyecto InkRecognition.Web. La referencia de Microsoft.Ink no aparecerá en las referencias de .NET de forma predeterminada, por lo que busque en la carpeta Windows para Microsoft.Ink.dll. Una vez que haya encontrado el archivo DLL,  agregue el ensamblado a las referencias del proyecto: seleccione la pestaña Examinar, cambie a la carpeta que contiene Microsoft.Ink.dll, seleccione Microsoft.Ink.dll y, a continuación, haga clic en **Aceptar.** En la imagen siguiente se muestra la solución del proyecto en Windows Explorer con todos los ensamblados de referencia agregados.

![proyecto inkrecognition en el Explorador de Windows con todos los ensamblados de referencia agregados](images/project-3b-with-reference-assemblies.png)<br/>
*proyecto inkrecognition en el Explorador de Windows con todos los ensamblados de referencia agregados*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Crear un servicio WCF de Silverlight para el reconocimiento de entrada de lápiz

A continuación, agregará un servicio WCF para el reconocimiento de entrada de lápiz al proyecto. Haga clic con el botón derecho en el proyecto InkRecognition.Web, haga clic **en Agregar** y, a continuación, haga clic en **Nuevo elemento.** Seleccione la plantilla Servicio Silverlight de WCF, cambie el nombre a InkRecogitionService y, a continuación, haga clic **en Agregar**. En la imagen siguiente se muestra **el cuadro de diálogo Agregar nuevo elemento** con el servicio WCF de Silverlight seleccionado y denominado.

![Cuadro de diálogo Agregar nuevo elemento con el servicio wcf silverlight seleccionado y con nombre](images/project-4-add-wcf-service.png)<br/>
*Cuadro de diálogo Agregar nuevo elemento con el servicio wcf silverlight seleccionado y con nombre*

Después de agregar el servicio WCF Silverlight, se abrirá el código de servicio subyacente, InkRecognitionService.cs. Reemplace el código de servicio por el código siguiente.

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>Agregue la referencia de servicio al cliente Project

Ahora que tiene el servicio WCF de Silverlight para InkRecognition, consumirá el servicio desde la aplicación cliente. Haga clic con el botón derecho en el proyecto InkRecognition y **seleccione Agregar referencia de servicio**. En el **Agregar referencia de servicio** de diálogo que aparece, seleccione **Detectar** para detectar servicios de la solución actual. InkRecognitionService aparecerá en el panel Servicios. Haga doble clic en InkRecognitionService en el panel Servicios, cambie el espacio de nombres a InkRecognitionServiceReference y, a continuación, haga clic **en Aceptar.** En la imagen siguiente se muestra **el Agregar referencia de servicio** de diálogo con InkRecognitionService seleccionado y el espacio de nombres cambiado.

![Cuadro de diálogo Agregar referencia de servicio con inkrecognitionservice seleccionado y espacio de nombres cambiado](images/project-5-discover-service-reference.png)<br/>
*Cuadro de diálogo Agregar referencia de servicio con inkrecognitionservice seleccionado y espacio de nombres cambiado*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Agregue la clase InkCollector a la clase InkRecognition Project

Haga clic con el botón derecho en el proyecto InkRecognition, haga clic **en Agregar** y, a continuación, haga clic en **Nuevo elemento.** En el **menú de Visual C, \#** seleccione Clase de **C. \#** Asigne a la clase el nombre InkCollector. En la imagen siguiente se muestra el cuadro de diálogo con la \# clase C seleccionada y con nombre.

![Cuadro de diálogo Agregar nuevo elemento con la clase c \# seleccionada y con nombre](images/project-6-add-ink-collector.png)<br/>
*Cuadro de diálogo Agregar nuevo elemento con la clase c \# seleccionada y con nombre*

Después de agregar la clase InkCollector, se abrirá la definición de clase. Reemplace el código del recopilador de lápiz por el código siguiente.

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>Actualizar el XAML de la página predeterminada y agregar un código subyacente para el reconocimiento de escritura a mano

Ahora que tiene una clase que recopila entrada de lápiz, deberá actualizar el CÓDIGO XAML en page.xaml con el código XAML siguiente. El código siguiente agrega un degradado amarillo al área de entrada, un control InkCanvas y un botón que desencadenará el reconocimiento.

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

Reemplace la página de código subyacente, Page.xaml.cs, por el código siguiente que agregará un controlador de eventos para el **botón Reconocer.**

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Quitar directivas de transporte seguro de la configuración de cliente

Para poder consumir el servicio WCF, debe quitar todas las opciones de transporte seguro de la configuración del servicio porque los transportes seguros no se admiten actualmente en los servicios WCF de Silverlight 2.0. En el proyecto InkRecognition, actualice la configuración de seguridad en ServiceReferences.ClientConfig. Cambiar el XML de seguridad de

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

to

```XML
       <security mode="None"/>
```

Ahora, la aplicación debe ejecutarse. En la imagen siguiente se muestra el aspecto de la aplicación dentro de una páginaweb con alguna escritura a mano especificada en el cuadro de reconocimiento.

![Aplicación dentro de una páginawebcon alguna escritura a mano especificada en el cuadro de reconocimiento](images/demo-1.png)<br/>
*Aplicación dentro de una páginawebcon alguna escritura a mano especificada en el cuadro de reconocimiento*

En la imagen siguiente se muestra el texto reconocido en la **lista** desplegable Resultado.

![Aplicación dentro de awebpagecon texto reconocido en la lista desplegable de resultados](images/demo-2.png)<br/>
*Aplicación dentro de awebpagecon texto reconocido en la lista desplegable de resultados*

 

 



