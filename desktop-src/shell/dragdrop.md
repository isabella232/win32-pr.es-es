---
description: Muchas aplicaciones permiten a los usuarios transferir datos a otra aplicación arrastrando y colocando los datos con el mouse o usando el portapapeles.
title: Transferir objetos de Shell con arrastrar y colocar y el portapapeles
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b04523d0ae22eac7bef68f37a6d22ac94b21e303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985534"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Transferir objetos de Shell con arrastrar y colocar y el portapapeles

Muchas aplicaciones permiten a los usuarios transferir datos a otra aplicación arrastrando y colocando los datos con el mouse o usando el portapapeles. Entre los diversos tipos de datos que se pueden transferir se encuentran los objetos de Shell, como archivos o carpetas. La transferencia de datos de Shell puede tener lugar entre dos aplicaciones, pero los usuarios también pueden transferir datos de Shell hacia o desde el escritorio o el explorador de Windows.

Aunque los archivos son el objeto de Shell que se transfiere con mayor frecuencia, la transferencia de datos de Shell puede incluir cualquiera de los diversos objetos que se encuentran en el [espacio de nombres del shell](namespace-intro.md). Por ejemplo, es posible que la aplicación necesite transferir un archivo a una carpeta virtual como la papelera de reciclaje o acepte un objeto de una extensión de espacio de nombres que no sea de Microsoft. Si está implementando una extensión de espacio de nombres, debe ser capaz de comportarse correctamente como un origen y un destino de colocación.

En este documento se explica cómo las aplicaciones pueden implementar las transferencias de datos de arrastrar y colocar y del Portapapeles con objetos de Shell.

-   [Objeto de datos de Shell](dataobject.md)
-   [Formatos del portapapeles de Shell](clipboard.md)
-   [Control de escenarios de transferencia de datos de shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Cómo funciona la función de arrastrar y colocar con objetos de Shell

Las aplicaciones a menudo necesitan proporcionar a los usuarios una manera de transferir los datos de Shell. Ejemplos:

-   Arrastrar un archivo desde el explorador de Windows o el escritorio y colocarlo en una aplicación.
-   Copiar un archivo en el portapapeles en el explorador de Windows y pegarlo en una aplicación.
-   Arrastrar un archivo desde una aplicación a la papelera de reciclaje.

Para obtener una explicación detallada sobre cómo administrar estos y otros escenarios, vea [administrar escenarios de transferencia de datos de Shell](datascenarios.md). Este documento se centra en los principios generales detrás de la transferencia de datos de Shell.

Windows proporciona dos formas estándar para que las aplicaciones transfieran datos de Shell:

-   Un usuario corta o copia en el portapapeles los datos de Shell, como uno o varios archivos. La otra aplicación recupera los datos del portapapeles.
-   Un usuario arrastra un icono que representa los datos de la aplicación de origen y coloca el icono en una ventana propiedad del destino.

En ambos casos, los datos transferidos se incluyen en un *objeto de datos*. Los objetos de datos son objetos del modelo de objetos componentes (COM) que exponen la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) . Esquemáticamente, hay tres pasos esenciales que deben seguir todas las transferencias de datos de Shell:

1.  El origen crea un objeto de datos que representa los datos que se van a transferir.
2.  El destino recibe un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
3.  El destino llama a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extraer los datos de ella.

La diferencia entre las transferencias de datos del portapapeles y de arrastrar y colocar radica principalmente en cómo se transfiere el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) desde el origen al destino.

### <a name="clipboard-data-transfers"></a>Transferencias de datos del portapapeles

El portapapeles es la forma más sencilla de transferir datos de Shell. El procedimiento básico es similar a las transferencias de datos estándar del portapapeles. Sin embargo, dado que está transfiriendo un puntero a un objeto de datos, no los propios datos, debe utilizar la API del portapapeles OLE en lugar de la API del portapapeles estándar. En el procedimiento siguiente se describe cómo usar la API del portapapeles OLE para transferir datos de Shell con el portapapeles:

1.  El origen de datos crea un objeto de datos que contiene los datos.
2.  El origen de datos llama a [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), que coloca un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos en el portapapeles.
3.  El destino llama a [**OleGetClipboard**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) para recuperar el puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
4.  El destino extrae los datos llamando al método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) .
5.  Con algunas transferencias de datos del shell, el destino podría tener que llamar al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos para proporcionar comentarios al objeto de datos sobre el resultado de la transferencia de datos. Consulte [control de operaciones de movimiento optimizado](datascenarios.md) para obtener un ejemplo de este tipo de operación.

### <a name="drag-and-drop-data-transfers"></a>Transferencias de datos de arrastrar y colocar

Aunque es algo más complejo de implementar, la transferencia de datos de arrastrar y colocar tiene algunas ventajas significativas en el portapapeles:

-   Las transferencias de arrastrar y colocar se pueden realizar con un sencillo movimiento del mouse, lo que hace que la operación sea más flexible e intuitiva de usar que el portapapeles.
-   Arrastrar y colocar proporciona al usuario una representación visual de la operación. El usuario puede seguir el icono cuando se mueve de un origen a un destino.
-   Arrastrar y colocar notifica al destino cuando los datos están disponibles.

Las operaciones de arrastrar y colocar también usan objetos de datos para transferir datos. Sin embargo, el origen de colocación debe proporcionar la funcionalidad más allá de la necesaria para las transferencias del portapapeles:

-   El origen de colocación también debe crear un objeto que exponga una interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) . El sistema usa **IDropSource** para comunicarse con el origen mientras la operación está en curso.
-   El objeto de datos de arrastrar y colocar es responsable de realizar el seguimiento del movimiento del cursor y de mostrar un icono para representar el objeto de datos.

Los destinos de colocación también deben proporcionar más funcionalidad de la necesaria para controlar las transferencias del portapapeles:

-   El destino de colocación debe exponer una interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Cuando el cursor se encuentra sobre una ventana de destino, el sistema utiliza **IDropTarget** para proporcionar al destino información como la posición del cursor y para notificárselo cuando se quitan los datos.
-   El destino de colocación debe registrarse en el sistema llamando a [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop). Esta función proporciona al sistema el identificador de una ventana de destino y un puntero a la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la aplicación de destino.

> [!Note]  
> En el caso de las operaciones de arrastrar y colocar, la aplicación debe inicializar COM con [**OleInitialize**](/windows/win32/api/ole2/nf-ole2-oleinitialize), no [**coinicializarse**](/windows/win32/api/objbase/nf-objbase-coinitialize).

 

En el procedimiento siguiente se describen los pasos esenciales que se suelen usar para transferir datos de Shell con arrastrar y colocar:

1.  El destino llama a [**RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) para proporcionar al sistema un puntero a su interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y registrar una ventana como destino de colocación.
2.  Cuando el usuario inicia una operación de arrastrar y colocar, el origen crea un objeto de datos e inicia un *bucle de arrastre* llamando a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Cuando el cursor está sobre la ventana de destino, el sistema notifica al destino llamando a uno de los métodos [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) del destino. El sistema llama a [**IDropTarget::D ragenter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) cuando el cursor entra en la ventana de destino e [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) cuando el cursor pasa sobre la ventana de destino. Ambos métodos proporcionan el destino de colocación con la posición actual del cursor y el estado de las teclas modificadoras del teclado, como CTRL o ALT. Cuando el cursor sale de la ventana de destino, el sistema lo notifica al destino llamando a [**IDropTarget::D ragleave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Cuando cualquiera de estos métodos devuelve, el sistema llama a la interfaz [**IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) para pasar el valor devuelto al origen.
4.  Cuando el usuario suelta el botón del mouse para colocar los datos, el sistema llama al método [**ROP::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) del destino. Entre los parámetros del método se encuentra un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
5.  El destino llama al método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos para extraer los datos.
6.  Con algunas transferencias de datos del shell, es posible que el destino también tenga que llamar al método [**IDataObject:: SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos para proporcionar comentarios al origen sobre el resultado de la transferencia de datos.
7.  Cuando el destino termina con el objeto de datos, vuelve de [**IDropTarget::D ROP**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). El sistema devuelve la llamada [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) del origen para notificar al origen que la transferencia de datos se ha completado.
8.  Dependiendo del [escenario de transferencia de datos](datascenarios.md)determinado, es posible que el origen tenga que realizar una acción adicional basada en el valor devuelto por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) y los valores que el destino pasa al objeto de datos. Por ejemplo, cuando se mueve un archivo, el origen debe comprobar estos valores para determinar si debe eliminar el archivo original.
9.  El origen libera el objeto de datos.

Aunque los procedimientos descritos anteriormente proporcionan un buen modelo general para la transferencia de datos de Shell, hay muchos tipos diferentes de datos que se pueden incluir en un objeto de datos de Shell. También hay una serie de escenarios de transferencia de datos diferentes que es posible que la aplicación necesite controlar. Cada tipo de datos y escenario requiere un enfoque algo diferente en tres pasos clave del procedimiento:

-   Cómo crea un origen un objeto de datos que contiene los datos del shell.
-   Cómo un destino extrae datos de Shell del objeto de datos.
-   Cómo el origen completa la operación de transferencia de datos.

El [objeto de datos de Shell](dataobject.md) proporciona una explicación general de cómo un origen crea un objeto de datos de Shell y cómo puede controlar ese objeto de datos el destino. [Administrar escenarios de transferencia de datos de Shell](datascenarios.md) describe en detalle cómo controlar una serie de escenarios comunes de transferencia de datos de Shell.

 

 
