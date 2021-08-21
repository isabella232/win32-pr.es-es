---
description: En este ejemplo se muestra cómo serializar y deserializar la entrada de lápiz en varios formatos.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Ejemplo de serialización de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e71eed5c91bf4fa1524cc52af163516ced0c7362d0d20b8ecf52ac1a08ccd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032273"
---
# <a name="ink-serialization-sample"></a>Ejemplo de serialización de entrada de lápiz

En este ejemplo se muestra cómo serializar y deserializar la entrada de lápiz en varios formatos. La aplicación representa un formulario con campos para introducir el nombre, el apellido y la firma. El usuario puede guardar estos datos como formato serializado de lápiz puro (ISF), lenguaje de marcado extensible (XML) mediante ISF codificado en Base64 o HTML, que hace referencia a la entrada de lápiz en una imagen de Formato de intercambio de gráficos (GIF) codificada en base64. La aplicación también permite al usuario abrir los archivos que se guardaron como formatos XML e ISF. El formato ISF usa propiedades extendidas para almacenar el nombre y los apellidos, mientras que los formatos XML y HTML almacenan esta información en atributos personalizados.

Este ejemplo no admite la carga desde el formato HTML, porque HTML no es adecuado para almacenar datos estructurados. Dado que los datos se separan en nombre, firma, entre otros, se requiere un formato que conserve esta separación, como XML u otro tipo de formato de base de datos.

HTML es muy útil en un entorno en el que el formato es importante, como en un documento de procesamiento de palabras. El CÓDIGO HTML que se guarda en este ejemplo usa ARCHIVOS GIF con notificación. Estos GIF tienen ISF insertado en ellos, lo que conserva la fidelidad total de la entrada de lápiz. Una aplicación de procesamiento de palabras puede guardar un documento que contiene varios tipos de datos, como imágenes, tablas, texto con formato y entrada de lápiz persistentes en formato HTML. Este CÓDIGO HTML se representaría en exploradores que no reconocen la entrada de lápiz. Sin embargo, cuando se carga en una aplicación habilitada para la entrada de lápiz, la fidelidad total de la entrada de lápiz original está disponible y se puede representar, editar o usar para el reconocimiento.

En este ejemplo se usan las siguientes características:

-   Método Load del [objeto](/previous-versions/ms569609(v=vs.100)) [Ink](/previous-versions/aa515768(v=msdn.10))
-   Método Save del [objeto](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) [Ink](/previous-versions/aa515768(v=msdn.10))
-   Propiedad [ExtendedProperties](/previous-versions/aa515768(v=msdn.10)) del [objeto Ink](/previous-versions/ms582214(v=vs.100))

## <a name="collecting-ink"></a>Recopilación de entradas manuscritas

En primer lugar, haga referencia a Tablet PC API, que se instala con Windows Vista y Windows XP Tablet PC Edition Software Development Kit (SDK).


```C++
using Microsoft.Ink;
```



El constructor crea y habilita [un elemento InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , para el formulario.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Guardar un archivo

El método controla el cuadro de diálogo Guardar como, crea una secuencia de archivos en la que guardar los datos de entrada de lápiz y llama al método save que corresponde a la elección `SaveAsMenu_Click` del usuario.

## <a name="saving-to-an-isf-file"></a>Guardar en un archivo ISF

En el método , los valores de nombre y apellido se agregan a la propiedad ExtendedProperties de la propiedad Ink del objeto `SaveISF` [InkCollector,](/previous-versions/ms836493(v=msdn.10)) [](/previous-versions/ms582214(v=vs.100)) antes de serializar y escribir la entrada de lápiz en el archivo. [](/previous-versions/ms836505(v=msdn.10)) Una vez serializada la entrada de lápiz, los [](/previous-versions/aa515768(v=msdn.10)) valores de nombre y apellido se quitan de la propiedad ExtendedProperties del objeto Ink.


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

En el `SaveXML` método , se usa un objeto [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) para crear y escribir en un documento XML. Con el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto [Ink,](/previous-versions/aa515768(v=msdn.10)) la entrada de lápiz se convierte primero en una matriz de bytes Ink Serialized Format codificada en Base64 y, a continuación, la matriz de bytes se convierte en una cadena que se va a escribir en el archivo XML. Los datos de texto del formulario también se escriben en el archivo XML.


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

El método SaveHTML usa el cuadro de límite de la [colección Strokes](/previous-versions/ms827799(v=msdn.10)) para comprobar la presencia de una firma. Si la firma existe, se convierte al formato GIF con notificación mediante el método [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) del objeto ink y se escribe en un archivo. A continuación, se hace referencia al GIF en el archivo HTML.


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

El método controla el cuadro de diálogo Abrir, abre el archivo y llama al método de carga correspondiente `OpenMenu_Click` a la elección del usuario.

## <a name="loading-an-isf-file"></a>Carga de un archivo ISF

El método lee el archivo creado anteriormente y convierte la matriz Byte en ink con el método `LoadISF` [Load del objeto Ink.](/previous-versions/ms569609(v=vs.100)) [](/previous-versions/aa515768(v=msdn.10)) El recopilador de entrada de lápiz está deshabilitado temporalmente para asignarle el objeto Ink. A `LoadISF` continuación, el método comprueba la propiedad [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) del objeto Ink para las cadenas de nombre y apellidos.


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



## <a name="loading-an-xml-file"></a>Carga de un archivo XML

El método carga un archivo XML creado previamente, recupera datos del nodo Ink y convierte los datos del nodo en ink mediante el método Load del `LoadXML` [objeto Ink.](/previous-versions/ms569609(v=vs.100)) [](/previous-versions/aa515768(v=msdn.10)) [InkCollector está](/previous-versions/ms836493(v=msdn.10)) deshabilitado temporalmente para asignarle el objeto Ink. El cuadro de firma se invalida y la información de nombre y apellidos se recupera del documento XML.


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



## <a name="closing-the-form"></a>Cerrar el formulario

El método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario elimina el [objeto InkCollector.](/previous-versions/ms836493(v=msdn.10))

 

 
