---
description: La aplicación de ejemplo Ink Blog muestra cómo crear una clase UserControl administrada que tiene funcionalidad de entrada manuscrita y hospeda ese control en Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Ejemplo web de blog de Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8796a05861d278015205b5ba0d3775e2e47af6a57ce1fee426c5c0c5011dacd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032363"
---
# <a name="ink-blog-web-sample"></a>Ejemplo web de blog de Ink

La aplicación de ejemplo Ink Blog muestra cómo crear una clase [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) administrada que tenga funcionalidad de entrada manuscrita y host que controle en Microsoft Internet Explorer. En el ejemplo también se muestra una técnica para enviar datos de entrada de lápiz a través de una red mediante HTTP y para conservar la entrada de lápiz en un servidor.

> [!Note]  
> Debe tener Microsoft Internet Information Services (IIS) con ASP.NET instalado para ejecutar este ejemplo. Asegúrese de que el equipo cumple los requisitos necesarios para ASP.NET que las aplicaciones se ejecuten en el equipo.

 

> [!Note]  
> Si ejecuta este ejemplo en un equipo que no es de tableta con microsoft Windows XP Tablet PC Edition Development Kit 1.7 instalado, la característica de reconocimiento de texto para el título de lápiz no funcionará. Esto se debe a que un equipo que no es de Tablet PC con el SDK de Tablet PC 1.7 instalado carece de reconocedores. El resto de la aplicación funciona como se describe.

 

## <a name="overview"></a>Información general

El ejemplo Ink Blog crea un weblog habilitado para lápiz. InkBlogWeb es una ASP.NET aplicación. La entrada de lápiz se realiza mediante un control de usuario al que se hace referencia desde una ASP.NET usuario.

El control de usuario detecta si los componentes de la plataforma tablet PC están instalados en el equipo cliente. Si es así, el control de usuario presenta al usuario dos áreas habilitadas para entrada de lápiz en la página web: una para invocar un título para la entrada de blog y otra para el cuerpo de la entrada. Si no están instalados los componentes de la plataforma de Tablet PC, se le da al usuario un control de cuadro de texto estándar para el título y el cuerpo de la entrada.

Cuando el usuario termina de crear la entrada, hace clic en un botón, Agregar blog, y la publicación se envía al servidor web para su almacenamiento. En el servidor, la aplicación guarda el texto del título y la fecha de publicación, así como una referencia a un archivo Formato de intercambio de gráficos (GIF). El archivo GIF, también guardado en el servidor, contiene los datos de entrada de lápiz del cuerpo en un archivo GIF certificado. Para obtener más información sobre el formato GIF notificado, vea [Almacenamiento de entrada manuscrita en HTML.](storing-ink-in-html.md)

Hay dos proyectos en la solución InkBlog: el proyecto **InkBlogControls** y el **proyecto InkBlogWeb.**

## <a name="inkblogcontrols-project"></a>InkBlogControls Project

El **proyecto InkBlogControls** es un [proyecto UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) que contiene el código para el control de usuario que permite la entrada manuscrita en la página web. El código de este control, el control InkArea, está en el archivo InkArea.cs.

La `InkArea` clase hereda de la [clase UserControl.](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) El constructor del `InkArea` control llama a un método auxiliar, `CreateInkCollectionSurface` .


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



El método determina si los componentes de entrada manuscrita de Tablet PC están disponibles en el cliente al intentar crear una instancia de `CreateInkCollectionSurface` la [clase InkCollector.](/previous-versions/ms583683(v=vs.100)) Si la llamada al `CreateInkCollectionSurface` método se realiza correctamente, el método devuelve un [objeto Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) como control .


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



Si se produce un error en el constructor porque no se encuentran los archivos de la plataforma de entrada manuscrita, se crea una instancia del control como control TextBox en lugar de como control `InputArea` [InkCollector.](/previous-versions/ms583683(v=vs.100)) [](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) A continuación, el constructor da tamaño al control al tamaño del control de usuario primario y lo agrega a la colección Controls del elemento primario.

La clase de control InkArea implementa tres propiedades públicas interesantes: InkData, TextData y WebEnabled.

La propiedad InkData es de solo lectura y proporciona acceso a los datos de entrada de lápiz serializados, si el cliente admite la entrada manuscrita. Si el cliente no admite la entrada manuscrita, la propiedad InkData obtiene una cadena vacía. La propiedad InkData llama a un método auxiliar, SerializeInkData, para determinar si el cliente admite la entrada manuscrita.


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



En el `SerializeInkData` método , la conversión a [InkCollector](/previous-versions/ms583683(v=vs.100)) es necesaria al obtener el objeto [Ink,](/previous-versions/ms583670(v=vs.100)) porque `inputArea` se declara como [control](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Si el objeto Ink contiene trazos, los datos de entrada manuscrita se guardan en la matriz de bytes como un GIF (especificado mediante el valor de enumeración `inkDataBytes` [PersistenceFormat).](/previous-versions/ms552503(v=vs.100)) A continuación, el método convierte la matriz de bytes en una cadena codificada en Base64 y devuelve esta cadena.

Suponiendo que el cliente puede realizar el reconocimiento, la propiedad devuelve el objeto RecognitionResult al pasar los datos de entrada de lápiz `TextData` a un reconocedor de escritura a [](/previous-versions/ms552537(v=vs.100)) mano. Si el cliente no tiene en cuenta la entrada de lápiz, se devuelve el contenido del cuadro de texto, como se muestra en el código siguiente.


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



La `TextData` propiedad llama a un método auxiliar, , que se muestra en el código siguiente, para llevar a cabo el `RecognizeInkData` reconocimiento. Cuando los motores de reconocimiento están presentes en el sistema, el método devuelve una cadena que contiene la propiedad `RecognizeInkData` [TopString](/previous-versions/ms572009(v=vs.100)) del objeto [RecognitionResult.](/previous-versions/ms552537(v=vs.100)) En cualquier otro caso, devuelve una cadena vacía.


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



La propiedad es un valor booleano de solo lectura que indica si se admite la invocación `InkEnabled` en el equipo cliente.

Otro miembro público importante de la `InkArea` clase de control es el método `DisposeResources` . Este método llama internamente al método para asegurarse de que se limpian todos los recursos aprovechados `Dispose` por el control de usuario. Cualquier aplicación que use el `InkArea` control debe llamar al método cuando termine de usar el control `DisposeResources` .

## <a name="inkblogweb-project"></a>InkBlogWeb Project

El proyecto InkBlogWeb es un proyecto de implementación del programa de instalación web que hace referencia al `InkArea` control para proporcionar la funcionalidad de registro. Para obtener más información sobre los proyectos de implementación del programa de instalación web, vea Implementación de una instalación [web Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Hay dos archivos .aspx que implementan el ejemplo de registro: Default.aspx y AddBlog.aspx. Default.aspx es la página predeterminada de la aplicación InkBlogWeb. El archivo de código subyacente de esta página es Default.aspx.cs. Esta página proporciona un vínculo a la página que contiene el nuevo formulario de entrada de blog y muestra las entradas de blog existentes. Este proceso se describe más adelante, después del siguiente examen de la nueva página del formulario de entrada de blog, AddBlog.aspx.

AddBlog.aspx y su archivo de código subyacente, AddBlog.aspx.cs, contienen el código de la interfaz de usuario y la lógica para crear nuevas entradas de blog. AddBlox.aspx hace referencia a dos instancias de la clase de control InkArea creada en el proyecto InkBlogControls mediante el elemento HTML OBJECT, como se muestra en el ejemplo siguiente. Una instancia tiene un `id` atributo inkBlogTitle y la otra tiene un atributo id de inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

El InkBlogControls.dll ensamblado debe estar presente en el mismo directorio que la página .aspx que hace referencia a él. El proyecto de implementación del programa de instalación web garantiza que este es el caso, como lo demuestra la presencia del elemento "Salida principal de InkBlogControls" en el cuadro de diálogo Implementación Project.

El control de título tiene solo 48 píxeles de alto para facilitar la entrada de una sola línea de entrada de lápiz para el título. El control de cuerpo tiene 296 píxeles de alto para hacer espacio para entradas de blog más grandes de varias líneas o quizás dibujos.

Los controles InkArea están conectados a una función de script del lado cliente, AddBlog, mediante un controlador de eventos onclick de un elemento HTML BUTTON estándar.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

También hay un formulario HTML en la página que contiene tres elementos INPUT ocultos: BlogTitleText, BlogBodyText y BlogBodyInkData. Este formulario se usa para volver a publicar los datos de entrada de blog en el servidor. AddBlog.aspx es el controlador posterior definido para el formulario.

La función AddBlog escrita en Microsoft JScript extrae los datos del blog de los controles InkArea y publica los <entity type="reg"/> resultados en el servidor.


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



Cuando los datos llegan al servidor, el código de AddBlog.aspx.cs comprueba el controlador de eventos Page Load para ver si la propiedad Form del objeto HttpRequest contiene \_ datos. Si es así, crea un nombre de archivo basado en la hora actual del sistema, coloca los datos del formulario en tres variables de cadena y escribe los datos en un archivo HTML y un archivo GIF que contiene los datos de entrada de lápiz, si están presentes, como se muestra en el código siguiente.


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

El SDK de Tablet PC 1.7 instala el ejemplo web ink blog de forma predeterminada. Para ejecutar el ejemplo, en Internet Explorer, vaya a https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Si está ejecutando Windows Server 2003, sustituya el nombre del equipo por "localhost".

> [!Note]  
> Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK. Debe completar una instalación personalizada y seleccionar la subla opción "Ejemplos web compilados previamente" para instalarlos.

 

También puede ejecutar el ejemplo abriendo y creando el proyecto en Microsoft Visual Studio .NET y, a continuación, implementando en un <entity type="reg"/> equipo independiente que ejecute IIS.

## <a name="troubleshooting-the-sample"></a>Solución de problemas de los ejemplos

Tres áreas que pueden causar dificultades al ejecutar o hospedar el ejemplo son los permisos y el reconocimiento.

### <a name="permissions"></a>Permisos

El ejemplo requiere permisos de escritura dentro de la carpeta raíz virtual para la cuenta que está intentando crear una nueva entrada de blog. De forma predeterminada, la versión compilada del ejemplo que se proporciona en el SDK de Tablet PC 1.7 tiene los permisos correctos establecidos para cumplir este requisito.

Si compila e implementa el ejemplo mediante el proyecto de implementación de instalación web proporcionado, debe proporcionar al grupo %MACHINENAME% Usuarios acceso de escritura a la carpeta del sistema de archivos a la que apunta la raíz \\ virtual InkBlogWeb (por ejemplo, C: \\ InetPub \\ WWWRoot \\ InkBlogWeb). El grupo Usuarios incluye la cuenta anónima usada por IIS, lo que permite a la aplicación ASP.NET escribir las nuevas entradas de blog en el sistema de archivos. Una alternativa es quitar el acceso anónimo a la raíz virtual y forzar la autenticación.

### <a name="recognition"></a>Reconocimiento

Los reconocedores de escritura a mano deben instalarse para reconocer la entrada de lápiz en el título del blog. Si accede a la aplicación InkBlog desde un equipo con un sistema operativo distinto de Windows XP Tablet PC Edition pero con el SDK de Tablet PC 1.7 instalado, puede escribir en la entrada de lápiz en los controles InkArea, pero los motores de reconocimiento no estarán presentes y no aparecerá ningún título para las entradas de blog. Sin embargo, el contenido de entrada de lápiz en el cuerpo todavía aparece.

### <a name="machine-configuration"></a>Configuración de la máquina

Si ha instalado ASP.NET y el .NET Framework en un equipo y, a continuación, desinstala y reinstala IIS, las asignaciones de script se interrumpirán y ASP.NET no funcionará. Si esto sucede, puede reparar el script de ASP.NET con la herramienta ASP.NET registro de IIS (Aspnet \_regiis.exe -i).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Entrada manuscrita en la Web](ink-on-the-web.md)
</dt> <dt>

[Formatos de datos de entrada manuscrita](ink-data-formats.md)
</dt> <dt>

[Sistema. Windows. Forms.UserControl (clase)](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
