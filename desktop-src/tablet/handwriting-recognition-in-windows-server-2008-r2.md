---
description: Windows Server 2008 R2 agrega compatibilidad para el reconocimiento de escritura a mano del lado servidor a Windows. En este tema se describe cómo reconocer la escritura a mano en Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconocimiento de escritura a mano en Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078567"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Reconocimiento de escritura a mano en Windows Server 2008 R2

Windows Server 2008 R2 admite el reconocimiento de escritura a mano del lado servidor. El reconocimiento del lado servidor permite que un servidor reconozca el contenido de la entrada manuscrita en páginas Web. Esto es especialmente útil cuando los usuarios de una red van a especificar términos que se interpretan con un diccionario personalizado. Por ejemplo, si tuviera una aplicación médica que consultase una base de datos del servidor para los nombres de los pacientes, estos nombres podrían agregarse a otra base de datos a la que se haría referencia cruzada al realizar búsquedas desde un formulario de Silverlight escrito a mano.

## <a name="set-up-your-server-for-server-side-recognition"></a>Configuración del servidor para el reconocimiento de Server-Side

Se deben seguir los pasos siguientes para configurar el reconocimiento del lado servidor.

- Instalar Servicios de Escritura con lápiz y Escritura a mano
- Instalar compatibilidad con servidor Web (IIS) y servidor de aplicaciones
- Habilitar el rol experiencia de escritorio
- Iniciar el servicio de entrada de Tablet PC

### <a name="install-ink-and-handwriting-services"></a>Instalar Servicios de Escritura con lápiz y Escritura a mano

Para instalar los servicios de tinta y escritura a mano, abra el administrador del servidor haciendo clic en el icono administrador del servidor de la bandeja Inicio rápido. En el menú **características** , haga clic en **Agregar características**. Asegúrese de activar la casilla **servicios de escritura con lápiz y escritura a mano** . La siguiente imagen muestra el cuadro de diálogo **seleccionar características** con **servicios de escritura con lápiz y escritura a mano** seleccionado.

![Cuadro de diálogo Seleccionar características con la casilla servicios de tinta y escritura a mano activada](images/setup-server-1-ink-and-handwriting.png)<br/>
*Cuadro de diálogo Seleccionar características con la casilla servicios de tinta y escritura a mano activada*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Compatibilidad con la instalación de servidor Web (IIS) y servidor de aplicaciones

Abra el administrador del servidor como hizo para el primer paso. A continuación, tendrá que agregar los roles servidor Web (IIS) y servidor de aplicaciones. En el menú **roles** , haga clic en **Agregar roles**. Aparece el Asistente para agregar roles. Haga clic en **Next**. Asegúrese de que el servidor de **aplicaciones** y el **servidor Web (IIS)** están seleccionados. La siguiente imagen muestra el cuadro de diálogo **Seleccionar roles de servidor** con los roles **servidor Web (IIS)** y **servidor de aplicaciones** seleccionados.

![Cuadro de diálogo Seleccionar roles de servidor con los roles servidor Web (IIS) y servidor de aplicaciones seleccionados](images/setup-server-2-select-server-roles.png)<br/>
*Cuadro de diálogo Seleccionar roles de servidor con los roles servidor Web (IIS) y servidor de aplicaciones seleccionados*

Al seleccionar **servidor de aplicaciones**, se le pedirá que instale el marco de trabajo de ASP.net. Haga clic en el botón **Agregar las características necesarias** . Después de hacer clic en **siguiente**, aparecerá un cuadro de diálogo de información general. Haga clic en **siguiente**. Ahora debe estar disponible el cuadro de diálogo **seleccionar servicios de rol** . Asegúrese de que el **servidor Web (IIS)** está seleccionado. La siguiente imagen muestra el cuadro de diálogo **seleccionar servicios de rol** con el servidor Web (IIS) habilitado.

![Cuadro de diálogo Seleccionar servicios de rol con el servidor Web (IIS) habilitado](images/setup-server-3-select-role-services.png)<br/>
*Cuadro de diálogo Seleccionar servicios de rol con el servidor Web (IIS) habilitado*

Haga clic en **Next**. Aparece un cuadro de diálogo de información general; Vuelva a hacer clic en **siguiente** . Ahora se le presentará una página que le ofrece opciones para los roles de servidor Web (IIS). Haga clic en **Next**. En la página siguiente, el botón **instalar** se convertirá en activo. Haga clic en **instalar** y podrá instalar la compatibilidad con servidor Web (IIS) y servidor de aplicaciones.

### <a name="enable-the-desktop-experience-role"></a>Habilitar el rol experiencia de escritorio

Para habilitar la experiencia de escritorio, haga clic en **Inicio**, en **herramientas administrativas** y, a continuación, en **Administrador del servidor**. Seleccione **Agregar servicios** y, a continuación, seleccione el servicio **experiencia de escritorio** . La siguiente imagen muestra el cuadro de diálogo **seleccionar características** con el elemento experiencia de escritorio instalado.

![Cuadro de diálogo Seleccionar características con el servicio experiencia de escritorio seleccionado](images/setup-server-4-desktop-experience.png)<br/>
*Cuadro de diálogo Seleccionar características con el servicio experiencia de escritorio seleccionado*

Haga clic en **siguiente** para instalar la experiencia de escritorio.

### <a name="start-the-tablet-service"></a>Iniciar el servicio de tableta

Una vez instalado el servicio de experiencia de escritorio, el servicio de entrada de Tablet PC aparecerá en el menú **servicios** . Para tener acceso al menú **servicios** , haga clic en **Inicio**, en **herramientas administrativas** y, a continuación, haga clic en **servicios**. Para iniciar el servicio, haga clic con el botón secundario en **servicio de entrada de Tablet PC** y, a continuación, haga clic en **iniciar**. La imagen siguiente muestra el menú **servicios** con el servicio de entrada de Tablet PC iniciado.

![Menú servicios con el servicio de entrada de Tablet PC iniciado](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Menú servicios con el servicio de entrada de Tablet PC iniciado*

## <a name="performing-server-side-recognition-using-silverlight"></a>Realización del reconocimiento de Server-Side con Silverlight

En esta sección se muestra cómo crear una aplicación web que usa Silverlight para capturar entradas de escritura a mano. Siga los pasos que se indican a continuación para programar el reconocedor en Visual Studio 2008.

- Instale y actualice Visual Studio 2008 para agregar compatibilidad con Silverlight.
- Cree un nuevo proyecto de Silverlight en Visual Studio 2008.
- Agregue las referencias de servicio necesarias al proyecto.
- Cree un servicio WCF de Silverlight para el reconocimiento de tinta.
- Agregue la referencia de servicio al proyecto de cliente.
- Agregue la clase InkCollector al proyecto InkRecognition.
- Quitar directivas de transporte seguro de la configuración del cliente

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Instalación y actualización de Visual Studio 2008 para agregar compatibilidad con Silverlight

Antes de comenzar, debe realizar los siguientes pasos en el servidor de Windows Server 2008 R2.

- Instale Visual Studio 2008.
- Instale [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).
- Instale el [SDK de Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).

Después de instalar estas aplicaciones y actualizaciones, está listo para crear la aplicación Web de reconocimiento del lado servidor.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Crear un nuevo proyecto Web de Silverlight en Visual Studio 2008

En el menú **Archivo**, haga clic en **Nuevo proyecto**. Seleccione la plantilla aplicación de Silverlight en la lista proyecto de Visual C \# . Asigne al proyecto el nombre InkRecognition y haga clic en **Aceptar**. En la imagen siguiente se muestra el proyecto de Silverlight de C \# seleccionado y denominado InkRecognition.

![proyecto de Silverlight de c \# seleccionado, con el nombre InkRecognition](images/project-1-new-project.png)<br/>
*proyecto de Silverlight de c \# seleccionado, con el nombre InkRecognition*

Después de hacer clic en **Aceptar**, un cuadro de diálogo le pedirá que agregue una aplicación de Silverlight al proyecto. Seleccione **Agregar un nuevo proyecto Web ASP.net a la solución para hospedar Silverlight** y haga clic en **Aceptar**. En la imagen siguiente se muestra cómo configurar el proyecto de ejemplo antes de hacer clic en **Aceptar**.

![Cuadro de diálogo con el símbolo del sistema para agregar una aplicación de Silverlight a un proyecto](images/project-2-add-a-new-aspnetproject.png)<br/>
*Cuadro de diálogo con el símbolo del sistema para agregar una aplicación de Silverlight a un proyecto*

### <a name="add-the-necessary-service-references-to-your-project"></a>Agregue las referencias de servicio necesarias al proyecto

Ahora tiene un proyecto de cliente de Silverlight genérico (InkRecognition) con un proyecto web (InkRecognition. Web) configurado en la solución. El proyecto se abrirá con Page. XAML y default. aspx abierto. Cierre estas ventanas y agregue las referencias System. Runtime. Serialization y System. ServiceModel al proyecto InkRecognition haciendo clic con el botón derecho en la carpeta referencias del proyecto InkRecognition y seleccionando **Agregar referencia**. La siguiente imagen muestra el cuadro de diálogo con las referencias de requisitos seleccionadas.

![Cuadro de diálogo Agregar referencias con System. Runtime. Serialization y System. ServiceModel seleccionado](images/project-3a-add-references-to-inkreco.png)<br/>
*Cuadro de diálogo Agregar referencias con System. Runtime. Serialization y System. ServiceModel seleccionado*

A continuación, debe agregar las referencias a System. ServiceModel y Microsoft. Ink al proyecto InkRecognition. Web. La referencia de Microsoft. Ink no aparecerá en las referencias de .NET de forma predeterminada, por lo que busque Microsoft.Ink.dll en la carpeta de Windows. Una vez localizado el archivo DLL, agregue el ensamblado a las referencias del proyecto: seleccione la pestaña **examinar** , cambie a la carpeta que contiene Microsoft.Ink.dll, seleccione Microsoft.Ink.dll y, a continuación, haga clic en **Aceptar**. La siguiente imagen muestra la solución del proyecto en el explorador de Windows con todos los ensamblados de referencia agregados.

![proyecto InkRecognition en el explorador de Windows con todos los ensamblados de referencia agregados](images/project-3b-with-reference-assemblies.png)<br/>
*proyecto InkRecognition en el explorador de Windows con todos los ensamblados de referencia agregados*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Crear un servicio WCF de Silverlight para el reconocimiento de tinta

A continuación, agregará un servicio WCF para el reconocimiento de entradas manuscritas en el proyecto. Haga clic con el botón derecho en el proyecto InkRecognition. Web, haga clic en **Agregar** y, a continuación, haga clic en **nuevo elemento**. Seleccione la plantilla de servicio WCF Silverlight, cambie el nombre a InkRecogitionService y, a continuación, haga clic en **Agregar**. La siguiente imagen muestra el cuadro de diálogo **Agregar nuevo elemento** con el servicio WCF de Silverlight seleccionado y denominado.

![Cuadro de diálogo Agregar nuevo elemento con el servicio WCF de Silverlight seleccionado y con nombre](images/project-4-add-wcf-service.png)<br/>
*Cuadro de diálogo Agregar nuevo elemento con el servicio WCF de Silverlight seleccionado y con nombre*

Después de agregar el servicio WCF Silverlight, se abrirá el código de servicio subyacente, InkRecognitionService. cs. Reemplace el código del servicio por el código siguiente.

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

### <a name="add-the-service-reference-to-your-client-project"></a>Agregar la referencia de servicio al proyecto de cliente

Ahora que tiene el servicio WCF de Silverlight para InkRecognition, consumirá el servicio desde la aplicación cliente. Haga clic con el botón derecho en el proyecto InkRecognition y seleccione **Agregar referencia de servicio**. En el cuadro de diálogo **Agregar referencia de servicio** que aparece, seleccione **detectar** para detectar los servicios de la solución actual. InkRecognitionService aparecerá en el panel servicios. Haga doble clic en InkRecognitionService en el panel servicios, cambie el espacio de nombres a InkRecognitionServiceReference y, a continuación, haga clic en **Aceptar**. La siguiente imagen muestra el cuadro de diálogo **Agregar referencia de servicio** con InkRecognitionService seleccionado y el espacio de nombres cambiado.

![Cuadro de diálogo Agregar referencia de servicio con el inkrecognitionservice seleccionado y el espacio de nombres cambiado](images/project-5-discover-service-reference.png)<br/>
*Cuadro de diálogo Agregar referencia de servicio con el inkrecognitionservice seleccionado y el espacio de nombres cambiado*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Agregue la clase InkCollector al proyecto InkRecognition

Haga clic con el botón secundario en el proyecto InkRecognition, haga clic en **Agregar** y, a continuación, haga clic en **nuevo elemento**. En el menú de **Visual c \#** , **Seleccione \# clase c**. Asigne a la clase el nombre InkCollector. La siguiente imagen muestra el cuadro de diálogo con la \# clase C seleccionada y con el nombre.

![Cuadro de diálogo Agregar nuevo elemento con la \# clase c seleccionada y con el nombre](images/project-6-add-ink-collector.png)<br/>
*Cuadro de diálogo Agregar nuevo elemento con la \# clase c seleccionada y con el nombre*

Después de agregar la clase InkCollector, se abrirá la definición de clase. Reemplace el código del recopilador de tinta con el código siguiente.

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

Ahora que tiene una clase que recopila entradas manuscritas, deberá actualizar el código XAML en Page. XAML con el código XAML siguiente. En el código siguiente se agrega un degradado amarillo al área de entrada, un control InkCanvas y un botón que desencadenará el reconocimiento.

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

Reemplace la página de código subyacente, Page. Xaml. CS, por el siguiente código que agregará un controlador de eventos para el botón **Recognize** .

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

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Quitar directivas de transporte seguro de la configuración del cliente

Antes de que pueda consumir el servicio WCF, debe quitar todas las opciones de transporte seguro de la configuración del servicio, ya que los transportes seguros no se admiten actualmente en los servicios WCF de Silverlight 2,0. En el proyecto InkRecognition, actualice la configuración de seguridad en ServiceReferences. ClientConfig. Cambiar el código XML de seguridad de

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

Ahora, la aplicación debe ejecutarse. En la imagen siguiente se muestra el aspecto de la aplicación dentro de awebpagewith alguna escritura a mano escrita en el cuadro reconocimiento.

![Aplicación en awebpagewith alguna escritura a mano escrita en el cuadro de reconocimiento](images/demo-1.png)<br/>
*Aplicación en awebpagewith alguna escritura a mano escrita en el cuadro de reconocimiento*

En la imagen siguiente se muestra el texto reconocido en la lista desplegable **resultado** .

![Aplicación dentro de awebpagewith reconocimiento de texto en la lista desplegable de resultados](images/demo-2.png)<br/>
*Aplicación dentro de awebpagewith reconocimiento de texto en la lista desplegable de resultados*

 

 



