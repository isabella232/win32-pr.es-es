---
description: Este ejemplo muestra cómo serializar y deserializar la entrada de lápiz en varios formatos.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Ejemplo de serialización de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e898f91db17efcb7579c067e7db5c422da8213a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540411"
---
# <a name="ink-serialization-sample"></a><span data-ttu-id="ea8bd-103">Ejemplo de serialización de tinta</span><span class="sxs-lookup"><span data-stu-id="ea8bd-103">Ink Serialization Sample</span></span>

<span data-ttu-id="ea8bd-104">Este ejemplo muestra cómo serializar y deserializar la entrada de lápiz en varios formatos.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-104">This sample demonstrates how to serialize and de-serialize ink in various formats.</span></span> <span data-ttu-id="ea8bd-105">La aplicación representa un formulario con campos para insertar el nombre, el apellido y la firma.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-105">The application represents a form with fields for inputting first name, last name, and signature.</span></span> <span data-ttu-id="ea8bd-106">El usuario puede guardar estos datos como formato serializado de tinta puro (ISF), lenguaje de marcado extensible (XML) con el ISF con codificación base64 o HTML, que hace referencia a la tinta en una imagen de formato de intercambio de gráficos enriquecido (GIF) codificado en Base64.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-106">The user may save this data as pure ink serialized format (ISF), Extensible Markup Language (XML) using base64 encoded ISF, or HTML, which references ink in a base64 encoded fortified Graphics Interchange Format (GIF) image.</span></span> <span data-ttu-id="ea8bd-107">La aplicación también permite al usuario abrir archivos que se guardaron como formatos XML y ISF.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-107">The application also enables the user to open files that were saved as XML and ISF formats.</span></span> <span data-ttu-id="ea8bd-108">El formato ISF utiliza propiedades extendidas para almacenar el nombre y los apellidos, mientras que los formatos XML y HTML almacenan esta información en atributos personalizados.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-108">The ISF format uses extended properties to store the first name and last name, whereas the XML and HTML formats store this information in custom attributes.</span></span>

<span data-ttu-id="ea8bd-109">Este ejemplo no admite la carga desde el formato HTML, porque HTML no es adecuado para almacenar datos estructurados.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-109">This sample does not support loading from the HTML format, because HTML is not suitable for storing structured data.</span></span> <span data-ttu-id="ea8bd-110">Dado que los datos se separan en el nombre, la firma, etc., se requiere un formato que conserve esta separación, como XML u otro tipo de formato de base de datos.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-110">Because the data is separated into name, signature, and so on, a format that preserves this separation, such as XML or another kind of database format, is required.</span></span>

<span data-ttu-id="ea8bd-111">HTML es muy útil en un entorno en el que el formato es importante, por ejemplo, en un documento de procesamiento de texto.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-111">HTML is very useful in an environment in which formatting is important, such as in a word processing document.</span></span> <span data-ttu-id="ea8bd-112">El HTML que se guarda en este ejemplo utiliza archivos GIF enriquecidos.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-112">The HTML that is saved by this sample uses fortified GIFs.</span></span> <span data-ttu-id="ea8bd-113">Estos archivos GIF tienen ISF incrustados dentro de ellos, lo que conserva la fidelidad total de la tinta.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-113">These GIFs have ISF embedded within them, which preserves the full fidelity of the ink.</span></span> <span data-ttu-id="ea8bd-114">Una aplicación de procesamiento de texto puede guardar un documento que contenga varios tipos de datos, como imágenes, tablas, texto con formato y tinta conservadas en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-114">A word processing application can save a document containing multiple types of data, such as images, tables, formatted text, and ink persisted in an HTML format.</span></span> <span data-ttu-id="ea8bd-115">Este código HTML se representaría en exploradores que no reconocen la tinta.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-115">This HTML would render in browsers that do not recognize ink.</span></span> <span data-ttu-id="ea8bd-116">Sin embargo, cuando se carga en una aplicación que está habilitada para tinta, la fidelidad total de la tinta original está disponible y se puede representar, editar o utilizar para el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-116">However, when loaded into an application that is ink-enabled, the full fidelity of the original ink is available and can be rendered, edited, or used for recognition.</span></span>

<span data-ttu-id="ea8bd-117">En este ejemplo se usan las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="ea8bd-117">The following features are used in this sample:</span></span>

-   <span data-ttu-id="ea8bd-118">Método [Load](/previous-versions/ms569609(v=vs.100)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ea8bd-118">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method</span></span>
-   <span data-ttu-id="ea8bd-119">Método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ea8bd-119">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method</span></span>
-   <span data-ttu-id="ea8bd-120">Propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) del objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="ea8bd-120">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property</span></span>

## <a name="collecting-ink"></a><span data-ttu-id="ea8bd-121">Recopilación de entradas manuscritas</span><span class="sxs-lookup"><span data-stu-id="ea8bd-121">Collecting Ink</span></span>

<span data-ttu-id="ea8bd-122">En primer lugar, haga referencia a la API de Tablet PC, que se instala con el kit de desarrollo de software (SDK) de Windows Vista y Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-122">First, reference the Tablet PC API, which are installed with the Windows Vista and Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="ea8bd-123">El constructor crea y habilita [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , para el formulario.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-123">The constructor creates and enables an [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic`, for the form.</span></span>


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a><span data-ttu-id="ea8bd-124">Guardar un archivo</span><span class="sxs-lookup"><span data-stu-id="ea8bd-124">Saving a File</span></span>

<span data-ttu-id="ea8bd-125">El `SaveAsMenu_Click` método controla el cuadro de diálogo Guardar como, crea una secuencia de archivos en la que se guardan los datos de tinta y llama al método Save que corresponde a la elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-125">The `SaveAsMenu_Click` method handles the Save As dialog box, creates a file stream in which to save the ink data, and calls the save method that corresponds to the user's choice.</span></span>

## <a name="saving-to-an-isf-file"></a><span data-ttu-id="ea8bd-126">Guardar en un archivo ISF</span><span class="sxs-lookup"><span data-stu-id="ea8bd-126">Saving to an ISF File</span></span>

<span data-ttu-id="ea8bd-127">En el `SaveISF` método, se agregan los valores de nombre y apellidos a la propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de la propiedad [Ink](/previous-versions/ms836505(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , antes de que la entrada de lápiz se serialice y se escriba en el archivo.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-127">In the `SaveISF` method, the first and last name values are added to the [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property of the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [Ink](/previous-versions/ms836505(v=msdn.10)) property, before the ink is serialized and written to the file.</span></span> <span data-ttu-id="ea8bd-128">Una vez serializada la tinta, se quitan los valores de nombre y apellidos de la propiedad ExtendedProperties del objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ea8bd-128">After the ink has been serialized, the first and last name values are removed from the [Ink](/previous-versions/aa515768(v=msdn.10)) object's ExtendedProperties property.</span></span>


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a><span data-ttu-id="ea8bd-129">Guardar en un archivo XML</span><span class="sxs-lookup"><span data-stu-id="ea8bd-129">Saving to an XML File</span></span>

<span data-ttu-id="ea8bd-130">En el `SaveXML` método, se utiliza un objeto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) para crear y escribir en un documento XML.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-130">In the `SaveXML` method, an [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) object is used to create and write to an XML document.</span></span> <span data-ttu-id="ea8bd-131">Con el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10)) , la tinta se convierte primero en una matriz de bytes de formato serializado de tinta codificada en Base64 y, a continuación, la matriz de bytes se convierte en una cadena que se va a escribir en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-131">Using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, the ink is first converted to a base64 encoded Ink Serialized Format byte array, and then the byte array is converted to a string to be written out to the XML file.</span></span> <span data-ttu-id="ea8bd-132">Los datos de texto del formulario también se escriben en el archivo XML.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-132">The text data from the form is also written out to the XML file.</span></span>


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a><span data-ttu-id="ea8bd-133">Guardar en un archivo HTML</span><span class="sxs-lookup"><span data-stu-id="ea8bd-133">Saving to an HTML File</span></span>

<span data-ttu-id="ea8bd-134">El método SaveHTML usa el rectángulo de selección de la colección [Strokes](/previous-versions/ms827799(v=msdn.10)) para comprobar la presencia de una firma.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-134">The SaveHTML method uses the bounding box of the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection to test for the presence of a signature.</span></span> <span data-ttu-id="ea8bd-135">Si la firma existe, se convierte al formato GIF enriquecido mediante el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto Ink y se escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-135">If the signature exists, it is converted to the fortified GIF format using the ink object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, and written to a file.</span></span> <span data-ttu-id="ea8bd-136">A continuación, se hace referencia al GIF en el archivo HTML.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-136">The GIF is then referenced in the HTML file.</span></span>


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a><span data-ttu-id="ea8bd-137">Cargar un archivo</span><span class="sxs-lookup"><span data-stu-id="ea8bd-137">Loading a File</span></span>

<span data-ttu-id="ea8bd-138">El `OpenMenu_Click` método controla el cuadro de diálogo abrir, abre el archivo y llama al método de carga que corresponde a la elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-138">The `OpenMenu_Click` method handles the Open dialog box, opens the file, and calls the loading method that corresponds to the user's choice.</span></span>

## <a name="loading-an-isf-file"></a><span data-ttu-id="ea8bd-139">Cargar un archivo ISF</span><span class="sxs-lookup"><span data-stu-id="ea8bd-139">Loading an ISF File</span></span>

<span data-ttu-id="ea8bd-140">El `LoadISF` método lee el archivo creado previamente y convierte la matriz de bytes en tinta con el método [Load](/previous-versions/ms569609(v=vs.100)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ea8bd-140">The `LoadISF` method reads the previously created file and converts the Byte array to ink with the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="ea8bd-141">El recopilador de tinta está deshabilitado temporalmente para asignarle el objeto de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-141">The ink collector is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="ea8bd-142">`LoadISF`A continuación, el método comprueba la propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) del objeto de entrada de lápiz para la primera y la última cadena de nombre.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-142">The `LoadISF` method then checks the Ink object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property for the first and last name strings.</span></span>


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a><span data-ttu-id="ea8bd-143">Cargar un archivo XML</span><span class="sxs-lookup"><span data-stu-id="ea8bd-143">Loading an XML File</span></span>

<span data-ttu-id="ea8bd-144">El `LoadXML` método carga un archivo XML creado previamente, recupera datos del nodo de tinta y convierte los datos del nodo en tinta mediante el método [Load](/previous-versions/ms569609(v=vs.100)) del objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ea8bd-144">The `LoadXML` method loads a previously created XML file, retrieves data from the Ink node, and converts the data in the node to ink using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="ea8bd-145">[InkCollector](/previous-versions/ms836493(v=msdn.10)) está deshabilitado temporalmente para asignarle el objeto de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-145">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="ea8bd-146">Se invalida el cuadro firma y se recupera la información sobre el nombre y el apellido del documento XML.</span><span class="sxs-lookup"><span data-stu-id="ea8bd-146">The signature box is invalidated, and the first and last name information is retrieved from the XML document.</span></span>


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a><span data-ttu-id="ea8bd-147">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="ea8bd-147">Closing the Form</span></span>

<span data-ttu-id="ea8bd-148">El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="ea8bd-148">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object.</span></span>

 

 
