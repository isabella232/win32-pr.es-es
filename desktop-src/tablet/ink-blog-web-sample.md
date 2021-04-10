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
# <a name="ink-blog-web-sample"></a><span data-ttu-id="c8ff3-103">Ejemplo de blog de Ink Web</span><span class="sxs-lookup"><span data-stu-id="c8ff3-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="c8ff3-104">La aplicación de ejemplo Ink blog muestra cómo crear una clase de [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) administrada que tiene la capacidad de entrada manuscrita y hospeda ese control en Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="c8ff3-105">En el ejemplo también se muestra una técnica para enviar datos de entrada de lápiz a través de una red mediante HTTP y para conservar la entrada manuscrita en un servidor.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="c8ff3-106">Debe tener instalado Microsoft Internet Information Services (IIS) con ASP.NET para ejecutar este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="c8ff3-107">Asegúrese de que el equipo cumple los requisitos necesarios para que las aplicaciones de ASP.NET se ejecuten en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="c8ff3-108">Si ejecuta este ejemplo en un equipo que no es de Tablet PC con el kit de desarrollo de Microsoft Windows XP Tablet PC Edition 1,7 instalado, la característica de reconocimiento de texto para el título de la tinta no funcionará.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="c8ff3-109">Esto se debe a que un equipo que no es de Tablet PC con el SDK 1,7 de Tablet PC instalado carece de reconocedores.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="c8ff3-110">El resto de la aplicación realiza tal como se describe.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="c8ff3-111">Información general</span><span class="sxs-lookup"><span data-stu-id="c8ff3-111">Overview</span></span>

<span data-ttu-id="c8ff3-112">En el ejemplo de blog de tinta se crea un blog con tinta habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="c8ff3-113">InkBlogWeb es una aplicación de ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="c8ff3-114">La entrada de lápiz se consigue mediante un control de usuario al que se hace referencia desde una página ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="c8ff3-115">El control de usuario detecta si los componentes de la plataforma de Tablet PC están instalados en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="c8ff3-116">Si es así, el control de usuario presenta el usuario con dos áreas habilitadas para la entrada de lápiz en la página web: una para el título de la entrada de blog y otra para el cuerpo de la entrada.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="c8ff3-117">Si los componentes de la plataforma de Tablet PC no están instalados, se proporciona al usuario un control de cuadro de texto estándar para el título y el cuerpo de la entrada.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="c8ff3-118">Cuando el usuario termina de crear la entrada, hace clic en un botón, agregar un blog y la publicación se envía al servidor web para su almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="c8ff3-119">En el servidor, la aplicación guarda el texto del título y la fecha de publicación, así como una referencia a un archivo GIF (formato de intercambio de gráficos).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="c8ff3-120">El archivo GIF, que también se guarda en el servidor, contiene los datos de tinta del cuerpo en un archivo GIF enriquecido.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="c8ff3-121">Para obtener más información sobre el formato GIF enriquecido, vea [almacenar entradas manuscritas en HTML](storing-ink-in-html.md).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="c8ff3-122">Hay dos proyectos en la solución InkBlog: el proyecto **InkBlogControls** y el proyecto **InkBlogWeb** .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="c8ff3-123">Proyecto InkBlogControls</span><span class="sxs-lookup"><span data-stu-id="c8ff3-123">InkBlogControls Project</span></span>

<span data-ttu-id="c8ff3-124">El proyecto **InkBlogControls** es un proyecto de [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) que contiene el código del control de usuario que permite la entrada manuscrita en la Página Web.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="c8ff3-125">El código de este control, el control InkArea, se encuentra en el archivo InkArea. cs.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="c8ff3-126">La `InkArea` clase hereda de la clase [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="c8ff3-127">El constructor del `InkArea` control llama a un método auxiliar, `CreateInkCollectionSurface` .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


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



<span data-ttu-id="c8ff3-128">El `CreateInkCollectionSurface` método determina si los componentes de entrada manuscrita de Tablet PC están disponibles en el cliente intentando crear una instancia de la clase [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="c8ff3-129">Si la llamada al `CreateInkCollectionSurface` método se realiza correctamente, el método devuelve un objeto de [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) como el control.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


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



<span data-ttu-id="c8ff3-130">Si se produce un error en el constructor porque no se encuentran los archivos de la plataforma de entrada manuscrita, `InputArea` se crea una instancia del control como un control de [cuadro de texto](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) en lugar de un control [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="c8ff3-131">Después, el constructor ajusta el tamaño del control al de control de usuario primario y lo agrega a la colección de controles del elemento primario.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="c8ff3-132">La clase de control InkArea implementa tres propiedades públicas interesantes: InkData, TextData y webabled.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="c8ff3-133">La propiedad InkData es de solo lectura y proporciona acceso a los datos de tinta serializados, si el cliente admite la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="c8ff3-134">Si el cliente no admite la entrada manuscrita, la propiedad InkData obtiene una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="c8ff3-135">La propiedad InkData llama a un método auxiliar, SerializeInkData, para determinar si el cliente admite la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


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



<span data-ttu-id="c8ff3-136">En el `SerializeInkData` método, la conversión a [InkCollector](/previous-versions/ms583683(v=vs.100)) es necesaria al obtener el objeto de [entrada manuscrita](/previous-versions/ms583670(v=vs.100)) , porque `inputArea` se declara como un [control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="c8ff3-137">Si el objeto de entrada manuscrita contiene trazos, los datos de la entrada de lápiz se guardan en la `inkDataBytes` matriz de bytes como GIF (se especifica mediante el valor de enumeración [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="c8ff3-138">A continuación, el método convierte la matriz de bytes en una cadena codificada en Base64 y devuelve esta cadena.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="c8ff3-139">Suponiendo que el cliente pueda realizar el reconocimiento, la `TextData` propiedad devuelve el objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) de pasar los datos de tinta a un reconocedor de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="c8ff3-140">Si el cliente no es compatible con tinta, se devuelve el contenido del cuadro de texto, como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


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



<span data-ttu-id="c8ff3-141">La `TextData` propiedad llama a un método auxiliar, `RecognizeInkData` , que se muestra en el código siguiente, para llevar a cabo el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="c8ff3-142">Cuando los motores de reconocimiento están presentes en el sistema, el `RecognizeInkData` método devuelve una cadena que contiene la propiedad de la cadena de la [cadena](/previous-versions/ms572009(v=vs.100)) del objeto [RecognitionResult](/previous-versions/ms552537(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="c8ff3-143">En cualquier otro caso, devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-143">Otherwise, it returns an empty string.</span></span>


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



<span data-ttu-id="c8ff3-144">La `InkEnabled` propiedad es un valor booleano de solo lectura que indica si se admite la entrada manuscrita en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="c8ff3-145">Otro miembro público importante de la `InkArea` clase control es el `DisposeResources` método.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="c8ff3-146">Este método llama internamente al `Dispose` método para asegurarse de que se limpian todos los recursos que aprovecha el control de usuario.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="c8ff3-147">Cualquier aplicación que use el `InkArea` control debe llamar al `DisposeResources` método cuando termine de utilizar el control.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="c8ff3-148">Proyecto InkBlogWeb</span><span class="sxs-lookup"><span data-stu-id="c8ff3-148">InkBlogWeb Project</span></span>

<span data-ttu-id="c8ff3-149">El proyecto InkBlogWeb es un proyecto de implementación de instalación web que hace referencia al `InkArea` control para proporcionar la funcionalidad de blog.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="c8ff3-150">Para obtener más información sobre los proyectos de implementación de la instalación Web, vea [implementación de un proyecto de instalación web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="c8ff3-151">Hay dos archivos. aspx que implementan el ejemplo de blog: default. aspx y AddBlog. aspx.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="c8ff3-152">Default. aspx es la página predeterminada de la aplicación InkBlogWeb.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="c8ff3-153">El archivo de código subyacente de esta página es default. aspx. cs.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="c8ff3-154">En esta página se proporciona un vínculo a la página que contiene el nuevo formulario de entrada de blog y se muestran las entradas de blog existentes.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="c8ff3-155">Este proceso se describe más adelante, después del examen siguiente de la página del formulario de entrada de blog, AddBlog. aspx.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="c8ff3-156">AddBlog. aspx y su archivo de código subyacente, AddBlog. aspx. CS, contienen la lógica y el código de la interfaz de usuario para crear nuevas entradas de blog.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="c8ff3-157">AddBlox. aspx hace referencia a dos instancias de la clase de control InkArea creadas en el proyecto InkBlogControls mediante el elemento de objeto HTML, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="c8ff3-158">Una instancia tiene un `id` atributo de inkBlogTitle y la otra tiene un atributo ID de inkBlogBody.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="c8ff3-159">El ensamblado de InkBlogControls.dll debe estar presente en el mismo directorio que la página. aspx que hace referencia a él.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="c8ff3-160">El proyecto de implementación de la instalación web se asegura de que este es el caso, como se demuestra en la presencia del elemento "resultado principal de InkBlogControls" en el proyecto de implementación.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="c8ff3-161">El control de título tiene solo 48 píxeles de alto para facilitar la entrada de una sola línea de entrada de lápiz para el título.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="c8ff3-162">El control de cuerpo es de 296 píxeles de alto para dejar espacio para entradas de blog mayores de varias líneas o quizás dibujos.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="c8ff3-163">Los controles InkArea se conectan a una función de script de cliente, AddBlog, por medio de un controlador de eventos onclick del elemento BUTTON de HTML estándar.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="c8ff3-164">También hay un formulario HTML en la página que contiene tres elementos de entrada ocultos: BlogTitleText, BlogBodyText y BlogBodyInkData.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="c8ff3-165">Este formulario se usa para devolver los datos de la entrada de blog al servidor.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="c8ff3-166">AddBlog. aspx es el controlador posterior que se ha definido para el formulario.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="c8ff3-167">La función AddBlog, escrita en Microsoft JScript <entity type="reg"/> , extrae los datos del blog de los controles InkArea y envía los resultados al servidor.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


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



<span data-ttu-id="c8ff3-168">Cuando los datos llegan al servidor, el código de AddBlog. aspx. CS comprueba el controlador de \_ eventos de carga de página para ver si la propiedad de formulario del objeto HttpRequest contiene datos.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="c8ff3-169">Si es así, crea un nombre de archivo basado en la hora actual del sistema, coloca los datos del formulario en tres variables de cadena y escribe los datos en un archivo HTML y un archivo GIF que contiene los datos de tinta, si están presentes, tal y como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


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



<span data-ttu-id="c8ff3-170">Para obtener más información sobre los métodos auxiliares, consulte el código fuente de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c8ff3-171">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="c8ff3-171">Running the Sample</span></span>

<span data-ttu-id="c8ff3-172">El SDK de Tablet PC 1,7 instala el ejemplo de Web de blog de tinta de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="c8ff3-173">Para ejecutar el ejemplo, en Internet Explorer, vaya a https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx .</span><span class="sxs-lookup"><span data-stu-id="c8ff3-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="c8ff3-174">Si está ejecutando Windows Server 2003, sustituya el nombre del equipo por "localhost".</span><span class="sxs-lookup"><span data-stu-id="c8ff3-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="c8ff3-175">Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="c8ff3-176">Debe completar una instalación personalizada y seleccionar la subopción "ejemplos web precompilados" para instalarlas.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="c8ff3-177">También puede ejecutar el ejemplo abriendo y compilando el proyecto en Microsoft Visual Studio <entity type="reg"/> .net y, a continuación, impleméntelo en un equipo independiente que ejecute IIS.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="c8ff3-178">Solución de problemas de los ejemplos</span><span class="sxs-lookup"><span data-stu-id="c8ff3-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="c8ff3-179">Tres áreas que pueden causar problemas al ejecutar o hospedar el ejemplo son los permisos y el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="c8ff3-180">Permisos</span><span class="sxs-lookup"><span data-stu-id="c8ff3-180">Permissions</span></span>

<span data-ttu-id="c8ff3-181">El ejemplo requiere permisos de escritura en la carpeta raíz virtual para la cuenta que está intentando crear una nueva entrada de blog.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="c8ff3-182">De forma predeterminada, la versión compilada del ejemplo proporcionada en el SDK de Tablet PC 1,7 tiene los permisos correctos establecidos para cumplir este requisito.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="c8ff3-183">Si compila e implementa el ejemplo mediante el proyecto de implementación de instalación web proporcionado, debe conceder al grupo de usuarios% MACHINENAME% \\ de escritura en la carpeta del sistema de archivos a la que apunta la raíz virtual de InkBlogWeb (por ejemplo, C: \\ InetPub \\ WWWRoot \\ InkBlogWeb).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="c8ff3-184">El grupo usuarios incluye la cuenta anónima que usa IIS, lo que permite que la aplicación ASP.NET escriba las nuevas entradas de blog en el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="c8ff3-185">Una alternativa es quitar el acceso anónimo a la raíz virtual y forzar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="c8ff3-186">Reconocimiento</span><span class="sxs-lookup"><span data-stu-id="c8ff3-186">Recognition</span></span>

<span data-ttu-id="c8ff3-187">Los reconocedores de escritura a mano deben instalarse para reconocer la tinta en el título del blog.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="c8ff3-188">Si tiene acceso a la aplicación InkBlog desde un equipo con un sistema operativo que no sea Windows XP Tablet PC Edition pero con el SDK 1,7 de Tablet PC instalado, puede escribir en la entrada manuscrita en los controles InkArea, pero los motores de reconocimiento no estarán presentes y no aparecerán títulos para las entradas de blog.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="c8ff3-189">No obstante, el contenido de la tinta del cuerpo todavía aparece.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="c8ff3-190">Configuración de la máquina</span><span class="sxs-lookup"><span data-stu-id="c8ff3-190">Machine Configuration</span></span>

<span data-ttu-id="c8ff3-191">Si ha instalado ASP.NET y el .NET Framework en un equipo y, a continuación, desinstala y reinstala IIS, las asignaciones de script se interrumpirán y ASP.NET no funcionará.</span><span class="sxs-lookup"><span data-stu-id="c8ff3-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="c8ff3-192">Si esto ocurre, puede reparar las asignaciones de scripts de ASP.NET con la herramienta de registro de IIS de ASP.NET (ASPNET \_regiis.exe-i).</span><span class="sxs-lookup"><span data-stu-id="c8ff3-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8ff3-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8ff3-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8ff3-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c8ff3-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="c8ff3-195">Entrada manuscrita en la web</span><span class="sxs-lookup"><span data-stu-id="c8ff3-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="c8ff3-196">Formatos de datos de tinta</span><span class="sxs-lookup"><span data-stu-id="c8ff3-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="c8ff3-197">System. Windows. Forms. UserControl (clase)</span><span class="sxs-lookup"><span data-stu-id="c8ff3-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
