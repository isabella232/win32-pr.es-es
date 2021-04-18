---
description: Para ayudar a la compatibilidad con la entrada de lápiz en las aplicaciones, hay dos objetos, que se pueden incrustar y son compatibles con cualquier contenedor OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Objetos sInk y tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef7ed1c06d256fe8eda9fad4bf15afa19fcb833
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678497"
---
# <a name="sink-and-tink-objects"></a>Objetos sInk y tInk

Para ayudar a la compatibilidad con la entrada de lápiz en las aplicaciones, hay dos objetos, que se pueden incrustar y son compatibles con cualquier contenedor OLE. Se generan llamando al método **Ink. ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** o el método **Ink. ClipboardCopy (Strokes, InkClipboardFormats, InkClipboardModes)** y son:

-   Objeto de entrada manuscrita de texto (tInk). Se trata de un objeto OLE que representa la tinta que se espera que forme palabras. Un objeto tInk permite convertir la tinta manuscrita en texto, como el texto devuelto por un reconocedor o la elección tomada de una lista de alternativas de reconocimiento. El color y el tamaño de la tinta se pueden establecer mediante programación y se pueden basar en los atributos del texto alrededor del objeto. El objeto tInk está pensado para que contenga una sola palabra. El objeto tInk es un pequeño objeto ligero que puede realizar operaciones sencillas, como la representación (dado un identificador a un contexto de dispositivo (HDC) y un rectángulo), y conservarse (dado un flujo). El uso de un objeto tInk permite una experiencia de usuario sin problemas al trabajar en una aplicación que utiliza la entrada de escritura a mano y texto.
-   Esboce (objeto de entrada manuscrita). Se trata de un objeto OLE que representa la tinta que no se espera que forme palabras. Un objeto receptor se interpreta como un dibujo. Un objeto receptor también es útil para representar varias palabras.

Estos objetos se pueden utilizar para la interoperabilidad entre aplicaciones, ya sea colocándolas en la ranura del objeto OLE del portapapeles o incluyéndolos en formato de texto enriquecido (RTF).

Puede usar los objetos tInk y sInk de las siguientes maneras:

-   Los objetos tInk y sInk se admiten en Microsoft Word 2002. Los usuarios pueden insertar entradas manuscritas en un documento de Word mediante los paneles de entrada de texto de escritura y dibujo que se proporcionan en Word 2002. Esta entrada de lápiz se incrusta en el archivo de Word como un objeto OLE con el CLSID del objeto sInk o tInk.
-   El control [InkEdit](/previous-versions/ms552265(v=vs.100)) de Tablet PC hace uso del objeto tInk. El control InkEdit es una subclase del control [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) estándar. La entrada de lápiz se inserta en el flujo RTF del control InkEdit como un objeto tInk.
-   Cuando una aplicación mueve un objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) seleccionado en el portapapeles, la ranura del portapapeles OLE contiene un objeto OLE TInk o sInk.

Por ejemplo, la aplicación puede reconocer escritura a mano y marcar cualquier objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) como un objeto tInk. Después, si selecciona una palabra en la entrada de lápiz y la copia y pega en Word, se mostrarán alternativas para esa palabra en Word 2002.

> [!Note]  
> La compatibilidad con el portapapeles de la plataforma de Tablet PC selecciona automáticamente la marca de metarchivo mejorado (EMF) cuando se coloca un objeto sInk o tInk en el portapapeles como un objeto OLE. El propio objeto se almacena en el portapapeles en el origen de inserción y en los descriptores de objeto.

 

Otro ejemplo: mediante el uso del objeto sInk, puede dibujar un boceto de tinta en una aplicación, copiar y pegar el boceto en Word 2002 y, a continuación, editar el dibujo mediante el panel de entrada de Tablet PC en Word.

Para contener correctamente objetos tInk, una aplicación debe implementar la compatibilidad con contenedores OLE para objetos incrustados. A continuación, para que el contenedor sea totalmente compatible con tInk, debe establecer lo siguiente:

-   Modificaciones en el código para buscar y reemplazar. En lugar de omitir los objetos incrustados en la búsqueda, estos objetos se deben interrogar para el tipo. Si se trata de un objeto tInk, se les debe crear una instancia y consultar su texto correspondiente.
-   Modificaciones en el comportamiento de la selección. La selección de objetos tInk nunca debe aparecer con los controladores de tamaño. Deben seleccionarse de la misma manera en que se selecciona texto en el documento. El código de selección de los objetos debe detectar si el tipo es tInk y mostrar la selección adecuadamente.
-   Uso de propiedades de ambiente. Las propiedades de ambiente como el tamaño de fuente, el color y el formato de negrita deben transmitirse al objeto tInk. La aplicación de estas propiedades cambia el ancho de la tinta manuscrita, por lo que se requiere una actualización del tamaño llamando al método [**GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o al método [IOleObject:: GetExtent](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) .
-   Invalide el procesamiento de método [IOleObject::D overb](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) predeterminado. Esto permite convertir a texto para pasar un lote de objetos tInk al reconocedor, que puede dividir las palabras en segmentos de reconocimiento.

Para obtener más información acerca de la división de palabras en segmentos de reconocimiento, consulte [segmentos de reconocimiento](recognition-segments.md).

 

 
