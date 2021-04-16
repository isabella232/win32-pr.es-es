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
# <a name="ink-serialization-sample"></a>Ejemplo de serialización de tinta

Este ejemplo muestra cómo serializar y deserializar la entrada de lápiz en varios formatos. La aplicación representa un formulario con campos para insertar el nombre, el apellido y la firma. El usuario puede guardar estos datos como formato serializado de tinta puro (ISF), lenguaje de marcado extensible (XML) con el ISF con codificación base64 o HTML, que hace referencia a la tinta en una imagen de formato de intercambio de gráficos enriquecido (GIF) codificado en Base64. La aplicación también permite al usuario abrir archivos que se guardaron como formatos XML y ISF. El formato ISF utiliza propiedades extendidas para almacenar el nombre y los apellidos, mientras que los formatos XML y HTML almacenan esta información en atributos personalizados.

Este ejemplo no admite la carga desde el formato HTML, porque HTML no es adecuado para almacenar datos estructurados. Dado que los datos se separan en el nombre, la firma, etc., se requiere un formato que conserve esta separación, como XML u otro tipo de formato de base de datos.

HTML es muy útil en un entorno en el que el formato es importante, por ejemplo, en un documento de procesamiento de texto. El HTML que se guarda en este ejemplo utiliza archivos GIF enriquecidos. Estos archivos GIF tienen ISF incrustados dentro de ellos, lo que conserva la fidelidad total de la tinta. Una aplicación de procesamiento de texto puede guardar un documento que contenga varios tipos de datos, como imágenes, tablas, texto con formato y tinta conservadas en formato HTML. Este código HTML se representaría en exploradores que no reconocen la tinta. Sin embargo, cuando se carga en una aplicación que está habilitada para tinta, la fidelidad total de la tinta original está disponible y se puede representar, editar o utilizar para el reconocimiento.

En este ejemplo se usan las siguientes características:

-   Método [Load](/previous-versions/ms569609(v=vs.100)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10))
-   Método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10))
-   Propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) del objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10))

## <a name="collecting-ink"></a>Recopilación de entradas manuscritas

En primer lugar, haga referencia a la API de Tablet PC, que se instala con el kit de desarrollo de software (SDK) de Windows Vista y Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



El constructor crea y habilita [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , para el formulario.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Guardar un archivo

El `SaveAsMenu_Click` método controla el cuadro de diálogo Guardar como, crea una secuencia de archivos en la que se guardan los datos de tinta y llama al método Save que corresponde a la elección del usuario.

## <a name="saving-to-an-isf-file"></a>Guardar en un archivo ISF

En el `SaveISF` método, se agregan los valores de nombre y apellidos a la propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de la propiedad [Ink](/previous-versions/ms836505(v=msdn.10)) del objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , antes de que la entrada de lápiz se serialice y se escriba en el archivo. Una vez serializada la tinta, se quitan los valores de nombre y apellidos de la propiedad ExtendedProperties del objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) .


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



## <a name="saving-to-an-xml-file"></a>Guardar en un archivo XML

En el `SaveXML` método, se utiliza un objeto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) para crear y escribir en un documento XML. Con el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10)) , la tinta se convierte primero en una matriz de bytes de formato serializado de tinta codificada en Base64 y, a continuación, la matriz de bytes se convierte en una cadena que se va a escribir en el archivo XML. Los datos de texto del formulario también se escriben en el archivo XML.


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



## <a name="saving-to-an-html-file"></a>Guardar en un archivo HTML

El método SaveHTML usa el rectángulo de selección de la colección [Strokes](/previous-versions/ms827799(v=msdn.10)) para comprobar la presencia de una firma. Si la firma existe, se convierte al formato GIF enriquecido mediante el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto Ink y se escribe en un archivo. A continuación, se hace referencia al GIF en el archivo HTML.


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



## <a name="loading-a-file"></a>Cargar un archivo

El `OpenMenu_Click` método controla el cuadro de diálogo abrir, abre el archivo y llama al método de carga que corresponde a la elección del usuario.

## <a name="loading-an-isf-file"></a>Cargar un archivo ISF

El `LoadISF` método lee el archivo creado previamente y convierte la matriz de bytes en tinta con el método [Load](/previous-versions/ms569609(v=vs.100)) del objeto [Ink](/previous-versions/aa515768(v=msdn.10)) . El recopilador de tinta está deshabilitado temporalmente para asignarle el objeto de entrada manuscrita. `LoadISF`A continuación, el método comprueba la propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) del objeto de entrada de lápiz para la primera y la última cadena de nombre.


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



## <a name="loading-an-xml-file"></a>Cargar un archivo XML

El `LoadXML` método carga un archivo XML creado previamente, recupera datos del nodo de tinta y convierte los datos del nodo en tinta mediante el método [Load](/previous-versions/ms569609(v=vs.100)) del objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) . [InkCollector](/previous-versions/ms836493(v=msdn.10)) está deshabilitado temporalmente para asignarle el objeto de entrada manuscrita. Se invalida el cuadro firma y se recupera la información sobre el nombre y el apellido del documento XML.


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



## <a name="closing-the-form"></a>Cierre del formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario desecha el objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) .

 

 
