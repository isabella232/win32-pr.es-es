---
description: Para ayudar a admitir la entrada de lápiz en las aplicaciones, hay dos objetos, ambos se pueden incrustar y son compatibles con cualquier contenedor OLE.
ms.assetid: fbd7bdf0-63b4-48d1-be91-eabbbb3f1618
title: Objetos sInk y tInk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8e25e1f258ac789382475666878c986f5053323a1b19bf8f4b6110c096f2fd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091328"
---
# <a name="sink-and-tink-objects"></a>Objetos sInk y tInk

Para ayudar a admitir la entrada de lápiz en las aplicaciones, hay dos objetos, ambos se pueden incrustar y son compatibles con cualquier contenedor OLE. Se generan llamando al método **Ink.ClipboardCopy (Rectangle, InkClipboardFormats, InkClipboardModes)** o al método **Ink.ClipboardCopy (Strokes, InkClipboardFormats, InkClipboardModes)** y son:

-   Objeto de entrada manuscrita de texto (tInk). Se trata de un objeto OLE que representa la entrada de lápiz que se espera que forme palabras. Un objeto tInk permite convertir la entrada manuscrita en texto, ya sea como el texto devuelto por un reconocedor o la elección que se toma de una lista de alternativas de reconocimiento. El color y el tamaño de la entrada de lápiz se pueden establecer mediante programación y se pueden basar en los atributos del texto alrededor del objeto. El objeto tInk está diseñado para contener una sola palabra. El objeto tInk es un objeto pequeño y ligero que puede realizar operaciones sencillas como la representación (dado un identificador a un contexto de dispositivo (HDC) y un RECT) y la persistencia (dada una secuencia). El uso de un objeto tInk permite una experiencia de usuario sin problemas al trabajar en una aplicación que usa la entrada de escritura a mano y texto.
-   Esboce el objeto de entrada de lápiz (sInk). Se trata de un objeto OLE que representa la entrada de lápiz que no se espera que forme palabras. Un objeto sInk se interpreta como un dibujo. Un objeto sInk también es útil para representar varias palabras.

Estos objetos se pueden usar para la interoperabilidad entre aplicaciones, ya sea colocándolos en la ranura de objetos OLE en el Portapapeles o insertándolos en formato de texto enriquecido (RTF).

Puede usar los objetos tInk y sInk de las maneras siguientes:

-   Los objetos tInk y sInk se admiten en Microsoft Word 2002. Los usuarios pueden insertar entrada de lápiz en un documento de Word mediante los paneles de entrada de texto de escritura y dibujo proporcionados en Word 2002. Esta entrada de lápiz se inserta en el archivo de Word como un objeto OLE con el CLSID del objeto sInk o tInk.
-   El control [InkEdit de](/previous-versions/ms552265(v=vs.100)) Tablet PC usa el objeto tInk. El control InkEdit es una subclase del control [RichTextBox](/dotnet/api/system.windows.forms.richtextbox?view=netcore-3.1) estándar. Ink se inserta en la secuencia RTF del control InkEdit como un objeto tInk.
-   Cuando una aplicación mueve un objeto [Ink](/previous-versions/aa515768(v=msdn.10)) seleccionado al Portapapeles, la ranura del Portapapeles del objeto OLE contiene un objeto OLE tInk o sInk.

Por ejemplo, la aplicación puede reconocer la escritura a mano y marcar cualquier [objeto Ink](/previous-versions/aa515768(v=msdn.10)) como un objeto tInk. A continuación, si selecciona una palabra en lápiz y la copia y la pega en Word, las alternativas para esa palabra se muestran en Word 2002.

> [!Note]  
> La compatibilidad con el Portapapeles de tablet PC Platform selecciona automáticamente la marca Metarchivo mejorado (EMF) cuando se coloca un objeto sInk o tInk en el Portapapeles como un objeto OLE. El propio objeto se almacena en el Portapapeles en las ranuras de origen de inserción y descriptor de objetos.

 

Como otro ejemplo, mediante el uso del objeto sInk, puede dibujar un boceto de lápiz en una aplicación, copiar y pegar el boceto en Word 2002 y, a continuación, editar el dibujo mediante el Panel de entrada de Tablet PC en Word.

Para contener correctamente objetos tInk, una aplicación debe implementar la compatibilidad con contenedores OLE para objetos incrustados. A continuación, para que el contenedor sea totalmente compatible con tInk, debe establecer:

-   Modificaciones en el código para Buscar y reemplazar. En lugar de omitir los objetos incrustados en la búsqueda, estos objetos se deben interrogar para el tipo . Si son un objeto tInk, se deben crear instancias de ellos y consultar su texto correspondiente.
-   Modificaciones en el comportamiento de selección. La selección de objetos tInk nunca debe aparecer con identificadores de tamaño. Se deben seleccionar de la misma manera que el texto que se selecciona en el documento. El código de selección de los objetos debe detectar si el tipo es tInk y mostrar la selección correctamente.
-   Uso de propiedades ambientales. Las propiedades ambientales, como el tamaño de fuente, el color y el formato en negrita, deben transmitirse al objeto tInk. La aplicación de estas propiedades cambia el ancho de la entrada manuscrita, por lo que se requiere una actualización de tamaño mediante una llamada al método [**GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o al método [IOleObject::GetExtent.](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent)
-   Invalide el procesamiento predeterminado del método [IOleObject::D oVerb.](/windows/win32/api/oleidl/nf-oleidl-ioleobject-doverb) Esto permite que la conversión a texto pase un lote de objetos tInk al reconocedor, lo que puede dividir las palabras en segmentos de reconocimiento.

Para obtener más información sobre cómo dividir las palabras en segmentos de reconocimiento, vea [Segmentos de reconocimiento](recognition-segments.md).

 

 
