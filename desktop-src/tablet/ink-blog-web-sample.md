---
description: La aplicación de ejemplo Ink blog muestra cómo crear una clase de UserControl administrada que tiene la capacidad de entrada manuscrita y hospeda ese control en Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Ejemplo de blog de Ink Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153905"
---
# <a name="ink-blog-web-sample"></a>Ejemplo de blog de Ink Web

La aplicación de ejemplo Ink blog muestra cómo crear una clase de [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) administrada que tiene la capacidad de entrada manuscrita y hospeda ese control en Microsoft Internet Explorer. En el ejemplo también se muestra una técnica para enviar datos de entrada de lápiz a través de una red mediante HTTP y para conservar la entrada manuscrita en un servidor.

> [!Note]  
> Debe tener instalado Microsoft Internet Information Services (IIS) con ASP.NET para ejecutar este ejemplo. Asegúrese de que el equipo cumple los requisitos necesarios para que las aplicaciones de ASP.NET se ejecuten en el equipo.

 

> [!Note]  
> Si ejecuta este ejemplo en un equipo que no es de Tablet PC con el kit de desarrollo de Microsoft Windows XP Tablet PC Edition 1,7 instalado, la característica de reconocimiento de texto para el título de la tinta no funcionará. Esto se debe a que un equipo que no es de Tablet PC con el SDK 1,7 de Tablet PC instalado carece de reconocedores. El resto de la aplicación realiza tal como se describe.

 

## <a name="overview"></a>Información general

En el ejemplo de blog de tinta se crea un blog con tinta habilitada. InkBlogWeb es una aplicación de ASP.NET. La entrada de lápiz se consigue mediante un control de usuario al que se hace referencia desde una página ASP.NET.

El control de usuario detecta si los componentes de la plataforma de Tablet PC están instalados en el equipo cliente. Si es así, el control de usuario presenta el usuario con dos áreas habilitadas para la entrada de lápiz en la página web: una para el título de la entrada de blog y otra para el cuerpo de la entrada. Si los componentes de la plataforma de Tablet PC no están instalados, se proporciona al usuario un control de cuadro de texto estándar para el título y el cuerpo de la entrada.

Cuando el usuario termina de crear la entrada, hace clic en un botón, agregar un blog y la publicación se envía al servidor web para su almacenamiento. En el servidor, la aplicación guarda el texto del título y la fecha de publicación, así como una referencia a un archivo GIF (formato de intercambio de gráficos). El archivo GIF, que también se guarda en el servidor, contiene los datos de tinta del cuerpo en un archivo GIF enriquecido. Para obtener más información sobre el formato GIF enriquecido, vea [almacenar entradas manuscritas en HTML](storing-ink-in-html.md).

Hay dos proyectos en la solución InkBlog: el proyecto **InkBlogControls** y el proyecto **InkBlogWeb** .

## <a name="inkblogcontrols-project"></a>Proyecto InkBlogControls

El proyecto **InkBlogControls** es un proyecto de [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) que contiene el código del control de usuario que permite la entrada manuscrita en la Página Web. El código de este control, el control InkArea, se encuentra en el archivo InkArea. cs.

La `InkArea` clase hereda de la clase [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) . El constructor del `InkArea` control llama a un método auxiliar, `CreateInkCollectionSurface` .


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



El `CreateInkCollectionSurface` método determina si los componentes de entrada manuscrita de Tablet PC están disponibles en el cliente intentando crear una instancia de la clase [InkCollector](/previous-versions/ms583683(v=vs.100)) . Si la llamada al `CreateInkCollectionSurface` método se realiza correctamente, el método devuelve un objeto de [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) como el control.


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



Si se produce un error en el constructor porque no se encuentran los archivos de la plataforma de entrada manuscrita, `InputArea` se crea una instancia del control como un control de [cuadro de texto](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) en lugar de un control [InkCollector](/previous-versions/ms583683(v=vs.100)) . Después, el constructor ajusta el tamaño del control al de control de usuario primario y lo agrega a la colección de controles del elemento primario.

La clase de control InkArea implementa tres propiedades públicas interesantes: InkData, TextData y webabled.

La propiedad InkData es de solo lectura y proporciona acceso a los datos de tinta serializados, si el cliente admite la entrada manuscrita. Si el cliente no admite la entrada manuscrita, la propiedad InkData obtiene una cadena vacía. La propiedad InkData llama a un método auxiliar, SerializeInkData, para determinar si el cliente admite la entrada manuscrita.


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



En el `SerializeInkData` método, la conversión a [InkCollector](/previous-versions/ms583683(v=vs.100)) es necesaria al obtener el objeto de [entrada manuscrita](/previous-versions/ms583670(v=vs.100)) , porque `inputArea` se declara como un [control](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Si el objeto de entrada manuscrita contiene trazos, los datos de la entrada de lápiz se guardan en la `inkDataBytes` matriz de bytes como GIF (se especifica mediante el valor de enumeración [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ). A continuación, el método convierte la matriz de bytes en una cadena codificada en Base64 y devuelve esta cadena.

Suponiendo que el cliente pueda realizar el reconocimiento, la `TextData` propiedad devuelve el objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) de pasar los datos de tinta a un reconocedor de escritura a mano. Si el cliente no es compatible con tinta, se devuelve el contenido del cuadro de texto, como se muestra en el código siguiente.


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



La `TextData` propiedad llama a un método auxiliar, `RecognizeInkData` , que se muestra en el código siguiente, para llevar a cabo el reconocimiento. Cuando los motores de reconocimiento están presentes en el sistema, el `RecognizeInkData` método devuelve una cadena que contiene la propiedad de la cadena de la [cadena](/previous-versions/ms572009(v=vs.100)) del objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) . En cualquier otro caso, devuelve una cadena vacía.


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



La `InkEnabled` propiedad es un valor booleano de solo lectura que indica si se admite la entrada manuscrita en el equipo cliente.

Otro miembro público importante de la `InkArea` clase control es el `DisposeResources` método. Este método llama internamente al `Dispose` método para asegurarse de que se limpian todos los recursos que aprovecha el control de usuario. Cualquier aplicación que use el `InkArea` control debe llamar al `DisposeResources` método cuando termine de utilizar el control.

## <a name="inkblogweb-project"></a>Proyecto InkBlogWeb

El proyecto InkBlogWeb es un proyecto de implementación de instalación web que hace referencia al `InkArea` control para proporcionar la funcionalidad de blog. Para obtener más información sobre los proyectos de implementación de la instalación Web, vea [implementación de un proyecto de instalación web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Hay dos archivos. aspx que implementan el ejemplo de blog: default. aspx y AddBlog. aspx. Default. aspx es la página predeterminada de la aplicación InkBlogWeb. El archivo de código subyacente de esta página es default. aspx. cs. En esta página se proporciona un vínculo a la página que contiene el nuevo formulario de entrada de blog y se muestran las entradas de blog existentes. Este proceso se describe más adelante, después del examen siguiente de la página del formulario de entrada de blog, AddBlog. aspx.

AddBlog. aspx y su archivo de código subyacente, AddBlog. aspx. CS, contienen la lógica y el código de la interfaz de usuario para crear nuevas entradas de blog. AddBlox. aspx hace referencia a dos instancias de la clase de control InkArea creadas en el proyecto InkBlogControls mediante el elemento de objeto HTML, tal como se muestra en el ejemplo siguiente. Una instancia tiene un `id` atributo de inkBlogTitle y la otra tiene un atributo ID de inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

El ensamblado de InkBlogControls.dll debe estar presente en el mismo directorio que la página. aspx que hace referencia a él. El proyecto de implementación de la instalación web se asegura de que este es el caso, como se demuestra en la presencia del elemento "resultado principal de InkBlogControls" en el proyecto de implementación.

El control de título tiene solo 48 píxeles de alto para facilitar la entrada de una sola línea de entrada de lápiz para el título. El control de cuerpo es de 296 píxeles de alto para dejar espacio para entradas de blog mayores de varias líneas o quizás dibujos.

Los controles InkArea se conectan a una función de script de cliente, AddBlog, por medio de un controlador de eventos onclick del elemento BUTTON de HTML estándar.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

También hay un formulario HTML en la página que contiene tres elementos de entrada ocultos: BlogTitleText, BlogBodyText y BlogBodyInkData. Este formulario se usa para devolver los datos de la entrada de blog al servidor. AddBlog. aspx es el controlador posterior que se ha definido para el formulario.

La función AddBlog, escrita en Microsoft JScript <entity type="reg"/> , extrae los datos del blog de los controles InkArea y envía los resultados al servidor.


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



Cuando los datos llegan al servidor, el código de AddBlog. aspx. CS comprueba el controlador de \_ eventos de carga de página para ver si la propiedad de formulario del objeto HttpRequest contiene datos. Si es así, crea un nombre de archivo basado en la hora actual del sistema, coloca los datos del formulario en tres variables de cadena y escribe los datos en un archivo HTML y un archivo GIF que contiene los datos de tinta, si están presentes, tal y como se muestra en el código siguiente.


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



Para obtener más información sobre los métodos auxiliares, consulte el código fuente de ejemplo.

## <a name="running-the-sample"></a>Ejecutar el ejemplo

El SDK de Tablet PC 1,7 instala el ejemplo de Web de blog de tinta de forma predeterminada. Para ejecutar el ejemplo, en Internet Explorer, vaya a https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Si está ejecutando Windows Server 2003, sustituya el nombre del equipo por "localhost".

> [!Note]  
> Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK. Debe completar una instalación personalizada y seleccionar la subopción "ejemplos web precompilados" para instalarlas.

 

También puede ejecutar el ejemplo abriendo y compilando el proyecto en Microsoft Visual Studio <entity type="reg"/> .net y, a continuación, impleméntelo en un equipo independiente que ejecute IIS.

## <a name="troubleshooting-the-sample"></a>Solución de problemas de los ejemplos

Tres áreas que pueden causar problemas al ejecutar o hospedar el ejemplo son los permisos y el reconocimiento.

### <a name="permissions"></a>Permisos

El ejemplo requiere permisos de escritura en la carpeta raíz virtual para la cuenta que está intentando crear una nueva entrada de blog. De forma predeterminada, la versión compilada del ejemplo proporcionada en el SDK de Tablet PC 1,7 tiene los permisos correctos establecidos para cumplir este requisito.

Si compila e implementa el ejemplo mediante el proyecto de implementación de instalación web proporcionado, debe conceder al grupo de usuarios% MACHINENAME% \\ de escritura en la carpeta del sistema de archivos a la que apunta la raíz virtual de InkBlogWeb (por ejemplo, C: \\ InetPub \\ WWWRoot \\ InkBlogWeb). El grupo usuarios incluye la cuenta anónima que usa IIS, lo que permite que la aplicación ASP.NET escriba las nuevas entradas de blog en el sistema de archivos. Una alternativa es quitar el acceso anónimo a la raíz virtual y forzar la autenticación.

### <a name="recognition"></a>Reconocimiento

Los reconocedores de escritura a mano deben instalarse para reconocer la tinta en el título del blog. Si tiene acceso a la aplicación InkBlog desde un equipo con un sistema operativo que no sea Windows XP Tablet PC Edition pero con el SDK 1,7 de Tablet PC instalado, puede escribir en la entrada manuscrita en los controles InkArea, pero los motores de reconocimiento no estarán presentes y no aparecerán títulos para las entradas de blog. No obstante, el contenido de la tinta del cuerpo todavía aparece.

### <a name="machine-configuration"></a>Configuración de la máquina

Si ha instalado ASP.NET y el .NET Framework en un equipo y, a continuación, desinstala y reinstala IIS, las asignaciones de script se interrumpirán y ASP.NET no funcionará. Si esto ocurre, puede reparar las asignaciones de scripts de ASP.NET con la herramienta de registro de IIS de ASP.NET (ASPNET \_regiis.exe-i).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Entrada manuscrita en la web](ink-on-the-web.md)
</dt> <dt>

[Formatos de datos de tinta](ink-data-formats.md)
</dt> <dt>

[System. Windows. Forms. UserControl (clase)](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
