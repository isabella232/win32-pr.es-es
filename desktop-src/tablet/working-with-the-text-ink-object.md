---
description: Para ayudar a la compatibilidad con la entrada de lápiz en las aplicaciones, hay dos objetos, que se pueden incrustar y son compatibles con cualquier contenedor OLE, el objeto de entrada manuscrita de texto (tInk) y el objeto de entrada de lápiz (receptor) del boceto.
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Trabajar con el objeto de entrada manuscrita de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082323f7e67e76f7ae39c6b592a86f2be0945a86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696592"
---
# <a name="working-with-the-text-ink-object"></a>Trabajar con el objeto de entrada manuscrita de texto

Para ayudar a la compatibilidad con la entrada de lápiz en las aplicaciones, hay dos objetos, que se pueden incrustar y son compatibles con cualquier contenedor OLE, el objeto de entrada manuscrita de texto (tInk) y el objeto de entrada de lápiz (receptor) del boceto.

El objeto de entrada manuscrita de texto es un objeto OLE que representa la tinta que se espera que forme palabras. Un objeto de entrada manuscrita de texto permite convertir la tinta manuscrita en texto eligiendo en una lista de alternativas. El color y el tamaño del objeto de entrada de lápiz se pueden establecer mediante programación y se pueden basar en los atributos del texto alrededor del objeto. El objeto de entrada de lápiz de texto está diseñado para que contenga una sola palabra.

El objeto de entrada manuscrita de texto admite el conjunto estándar de interfaces OLE necesarias para la incrustación y la compatibilidad con el portapapeles. La interfaz [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) Lee y escribe en una secuencia en formato serializado de tinta (ISF). El objeto de entrada manuscrita de texto proporciona la interfaz [**IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) para tener acceso a sus propiedades de presentación y a la lista de resultados de reconocimiento.

El objeto de entrada manuscrita de texto se puede usar para la interoperabilidad entre aplicaciones, ya sea colocándolo en la ranura del objeto OLE del portapapeles, mediante la inserción en formato RTF o su persistencia en una secuencia ISF.

Se puede generar un objeto de entrada de lápiz de texto de las siguientes maneras.

-   El control [InkEdit](inkedit-control-reference.md) usa el objeto de entrada manuscrita de texto. La funcionalidad del control InkEdit es un superconjunto de la funcionalidad del control RichEdit estándar. La entrada de lápiz se inserta en el flujo RTF del control InkEdit como un objeto de entrada manuscrita de texto.
-   Cuando una aplicación copia un objeto [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) o [InkEdit](inkedit-control-reference.md) en el portapapeles y se establece el formato de [**enumeración InkClipboardFormats**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) , la ranura del portapapeles OLE contiene un objeto OLE de entrada manuscrita.
-   El panel de entrada de Tablet PC puede generar objetos de texto manuscrito.

Por ejemplo, la aplicación puede reconocer la escritura a mano y agregar el resultado del reconocimiento a los trazos. Después, si copia y pega los trazos en Microsoft Word como un objeto de entrada de lápiz de texto, las alternativas para esa palabra estarán disponibles en Word 2003 y versiones posteriores.

Para contener correctamente objetos de entrada de lápiz de texto, una aplicación debe implementar la compatibilidad con contenedores OLE para los objetos incrustados. A continuación, para que el contenedor sea totalmente compatible con la tinta de texto, debe establecer lo siguiente:

-   Modificaciones en la aplicación para buscar y reemplazar. En lugar de omitir los objetos incrustados en la búsqueda, estos objetos se deben interrogar para el tipo. Si se trata de un objeto de entrada manuscrita de texto, se les debe crear una instancia y consultar su texto correspondiente.
-   Modificaciones en el comportamiento de la selección. La selección de los objetos de lápiz de texto nunca debe aparecer con los controladores de tamaño. Deben seleccionarse de la misma manera en que se selecciona texto en el documento. El código de selección de los objetos debe detectar si el tipo es una entrada de lápiz de texto y mostrar la selección adecuadamente.
-   Uso de propiedades de ambiente. Las propiedades de ambiente como el tamaño de fuente, el color y el formato de negrita deben transmitirse al objeto de entrada manuscrita de texto. La aplicación de estas propiedades cambia el ancho de la tinta manuscrita, por lo que se requiere una actualización del tamaño llamando al método [**IInkLineInfo:: GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o [**IOleObject:: GetExtent**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent) .

## <a name="in-this-section"></a>En esta sección

-   [Convertir un objeto de entrada de lápiz de texto en tinta](converting-a-text-ink-object-to-ink.md)
-   [API de entrada manuscrita de texto](text-ink-apis.md)
-   [Objetos sInk y tInk](sink-and-tink-objects.md)

 

 
