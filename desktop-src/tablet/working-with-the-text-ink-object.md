---
description: Para ayudar a admitir la entrada de lápiz en las aplicaciones, hay dos objetos, los cuales se pueden incrustar y son compatibles con cualquier contenedor OLE, el objeto de entrada de lápiz de texto (tInk) y el objeto de lápiz de boceto (sInk).
ms.assetid: 0202e91c-c7a0-4e7b-a1c6-a2f58c11c0be
title: Trabajar con el objeto Text Ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938d7e68795147913b64cad399f70ac6c1d2fdb06edc19e6d0c0b6c64add6422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449268"
---
# <a name="working-with-the-text-ink-object"></a>Trabajar con el objeto Text Ink

Para ayudar a admitir la entrada de lápiz en las aplicaciones, hay dos objetos, los cuales se pueden incrustar y son compatibles con cualquier contenedor OLE, el objeto de entrada de lápiz de texto (tInk) y el objeto de lápiz de boceto (sInk).

El objeto de entrada de lápiz de texto es un objeto OLE que representa la entrada de lápiz que se espera que forme palabras. Un objeto de entrada de lápiz de texto permite convertir la entrada manuscrita en texto eligiendo entre una lista de alternativas. El color y el tamaño del objeto de entrada de lápiz de texto se pueden establecer mediante programación y se pueden basar en los atributos del texto alrededor del objeto. El objeto de entrada de lápiz de texto está pensado para contener una sola palabra.

El objeto text ink admite el conjunto estándar de interfaces OLE necesarias para la inserción y la compatibilidad con el Portapapeles. La [**interfaz IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) lee y escribe en una secuencia en formato serializado de entrada de lápiz (ISF). El objeto text ink proporciona la [**interfaz IInkLineInfo**](/windows/desktop/api/msinkaut/nn-msinkaut-iinklineinfo) para acceder a sus propiedades de presentación y a la lista de resultados de reconocimiento.

El objeto de entrada de lápiz de texto se puede usar para la interoperabilidad entre aplicaciones, ya sea si se coloca en la ranura de objetos OLE en el Portapapeles, se inserta en RTF o se conserva en una secuencia de ISF.

Un objeto de entrada de lápiz de texto se puede generar de las maneras siguientes.

-   El [control InkEdit](inkedit-control-reference.md) usa el objeto de entrada manuscrita de texto. La funcionalidad del control InkEdit es un superconso de la funcionalidad de control RichEdit estándar. Ink se inserta en la secuencia RTF del control InkEdit como un objeto de entrada de lápiz de texto.
-   Cuando una aplicación copia un [objeto InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) o [InkEdit](inkedit-control-reference.md) en el Portapapeles y se establece el formato de enumeración [**InkClipboardFormats,**](/windows/desktop/api/msinkaut/ne-msinkaut-inkclipboardformats) la ranura del Portapapeles del objeto OLE contiene un objeto OLE de entrada manuscrita de texto.
-   El Panel de entrada de tablet PC puede generar objetos de entrada de lápiz de texto.

Por ejemplo, la aplicación puede reconocer la escritura a mano y agregar el resultado del reconocimiento a los trazos. A continuación, si copia y pega los trazos en Microsoft Word como un objeto de entrada de lápiz de texto, las alternativas para esa palabra están disponibles en Word 2003 y versiones posteriores.

Para contener correctamente objetos de entrada de lápiz de texto, una aplicación debe implementar la compatibilidad con contenedores OLE para objetos incrustados. A continuación, para que el contenedor sea totalmente compatible con la entrada de lápiz de texto, debe establecer:

-   Modificaciones en la aplicación para Buscar y reemplazar. En lugar de omitir objetos incrustados en la búsqueda, estos objetos se deben interrogar para el tipo. Si son un objeto de entrada de lápiz de texto, se deben crear instancias de ellos y consultar su texto correspondiente.
-   Modificaciones en el comportamiento de selección. La selección de objetos de entrada de lápiz de texto nunca debe aparecer con identificadores de tamaño. Deben seleccionarse de la misma manera que el texto que se selecciona en el documento. El código de selección de los objetos debe detectar si el tipo es entrada de lápiz de texto y mostrar la selección correctamente.
-   Uso de propiedades ambientales. Las propiedades ambientales, como el tamaño de fuente, el color y el formato en negrita, deben transmitirse al objeto de entrada manuscrita de texto. La aplicación de estas propiedades cambia el ancho de la entrada manuscrita, por lo que se requiere una actualización de tamaño mediante una llamada al método [**IInkLineInfo::GetInkExtent**](/windows/desktop/api/msinkaut/nf-msinkaut-iinklineinfo-getinkextent) o [**IOleObject::GetExtent.**](/windows/win32/api/oleidl/nf-oleidl-ioleobject-getextent)

## <a name="in-this-section"></a>En esta sección

-   [Convertir un objeto text ink en ink](converting-a-text-ink-object-to-ink.md)
-   [API de Text Ink](text-ink-apis.md)
-   [Objetos sInk y tInk](sink-and-tink-objects.md)

 

 
