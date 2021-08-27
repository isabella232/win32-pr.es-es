---
description: Muchas aplicaciones permiten a los usuarios transferir datos a otra aplicación arrastrando y colocando los datos con el mouse o mediante el Portapapeles.
title: Transferencia de objetos de shell con arrastrar y colocar y el Portapapeles
ms.topic: article
ms.date: 05/31/2018
ms.assetid: bd73098b-2f69-48a4-bb06-e1e0a452e69d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c45fc01709c50fd309c285cb486474cab2f1d8ac0b20c56bb7e21578cb8138f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090625"
---
# <a name="transferring-shell-objects-with-drag-and-drop-and-the-clipboard"></a>Transferencia de objetos de shell con arrastrar y colocar y el Portapapeles

Muchas aplicaciones permiten a los usuarios transferir datos a otra aplicación arrastrando y colocando los datos con el mouse o mediante el Portapapeles. Entre los muchos tipos de datos que se pueden transferir se encuentran objetos de Shell, como archivos o carpetas. La transferencia de datos de Shell puede realizarse entre dos aplicaciones, pero los usuarios también pueden transferir datos de Shell hacia o desde el escritorio o Windows Explorer.

Aunque los archivos son el objeto de Shell transferido más comúnmente, la transferencia de datos de Shell puede implicar cualquiera de los diversos objetos que se encuentran en el espacio [de nombres de Shell](namespace-intro.md). Por ejemplo, es posible que la aplicación tenga que transferir un archivo a una carpeta virtual como el papelera de reciclaje o aceptar un objeto de una extensión de espacio de nombres que no sea de Microsoft. Si va a implementar una extensión de espacio de nombres, debe ser capaz de comportarse correctamente como origen y destino de colocación.

En este documento se describe cómo las aplicaciones pueden implementar transferencias de datos de arrastrar y colocar y del Portapapeles con objetos de Shell.

-   [El objeto de datos del shell](dataobject.md)
-   [Formatos del Portapapeles de Shell](clipboard.md)
-   [Control de escenarios de transferencia de datos de shell](datascenarios.md)

## <a name="how-drag-and-drop-works-with-shell-objects"></a>Funcionamiento de arrastrar y colocar con objetos de shell

Las aplicaciones a menudo necesitan proporcionar a los usuarios una manera de transferir datos de Shell. Ejemplos:

-   Arrastre un archivo desde Windows explorador o el escritorio y su colocación en una aplicación.
-   Copiar un archivo en el Portapapeles en Windows Explorer y pegarlo en una aplicación.
-   Arrastre un archivo desde una aplicación al papelera de reciclaje.

Para obtener una explicación detallada de cómo controlar estos y otros escenarios, vea [Handling Shell Data Transfer Scenarios](datascenarios.md). Este documento se centra en los principios generales de la transferencia de datos de Shell.

Windows proporciona dos maneras estándar para que las aplicaciones transfieran datos de Shell:

-   Un usuario corta o copia datos de Shell, como uno o varios archivos, en el Portapapeles. La otra aplicación recupera los datos del Portapapeles.
-   Un usuario arrastra un icono que representa los datos de la aplicación de origen y coloca el icono en una ventana propiedad del destino.

En ambos casos, los datos transferidos se encuentran en un *objeto de datos*. Los objetos de datos son objetos del Modelo de objetos componentes (COM) que exponen la [**interfaz IDataObject.**](/windows/win32/api/objidl/nn-objidl-idataobject) Esquemáticamente, hay tres pasos esenciales que deben seguir todas las transferencias de datos de Shell:

1.  El origen crea un objeto de datos que representa los datos que se transferirán.
2.  El destino recibe un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
3.  El destino llama a [**la interfaz IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) para extraer los datos de ella.

La diferencia entre el Portapapeles y las transferencias de datos de arrastrar y colocar reside principalmente en cómo se transfiere el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del origen al destino.

### <a name="clipboard-data-transfers"></a>Transferencias de datos del Portapapeles

El Portapapeles es la manera más sencilla de transferir datos de Shell. El procedimiento básico es similar a las transferencias de datos estándar del Portapapeles. Sin embargo, dado que va a transferir un puntero a un objeto de datos, no a los propios datos, debe usar la API del Portapapeles OLE en lugar de la API estándar del Portapapeles. En el procedimiento siguiente se describe cómo usar la API del Portapapeles OLE para transferir datos de Shell con el Portapapeles:

1.  El origen de datos crea un objeto de datos para contener los datos.
2.  El origen de datos llama a [**OleSetClipboard**](/windows/win32/api/ole2/nf-ole2-olesetclipboard), que coloca un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos en el Portapapeles.
3.  El destino llama [**a OleGetClipboard para**](/windows/win32/api/ole2/nf-ole2-olegetclipboard) recuperar el puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
4.  El destino extrae los datos llamando al [**método IDataObject::GetData.**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata)
5.  Con algunas transferencias de datos de Shell, es posible que el destino también tenga que llamar al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos para proporcionar comentarios al objeto de datos sobre el resultado de la transferencia de datos. Consulte [Control de operaciones de movimiento optimizadas](datascenarios.md) para obtener un ejemplo de este tipo de operación.

### <a name="drag-and-drop-data-transfers"></a>Transferencias de datos de arrastrar y colocar

Aunque es algo más complejo de implementar, la transferencia de datos de arrastrar y colocar tiene algunas ventajas significativas sobre el Portapapeles:

-   Las transferencias de arrastrar y colocar se pueden realizar con un simple movimiento del mouse, lo que hace que la operación sea más flexible e intuitiva de usar que el Portapapeles.
-   Arrastrar y colocar proporciona al usuario una representación visual de la operación. El usuario puede seguir el icono a medida que se mueve de origen a destino.
-   Al arrastrar y colocar se notifica al destino cuando los datos están disponibles.

Las operaciones de arrastrar y colocar también usan objetos de datos para transferir datos. Sin embargo, el origen de colocación debe proporcionar funcionalidad más allá de la necesaria para las transferencias del Portapapeles:

-   El origen de colocación también debe crear un objeto que exponga una [**interfaz IDropSource.**](/windows/win32/api/oleidl/nn-oleidl-idropsource) El sistema usa **IDropSource para** comunicarse con el origen mientras la operación está en curso.
-   El objeto de datos de arrastrar y colocar es responsable de realizar el seguimiento del movimiento del cursor y mostrar un icono para representar el objeto de datos.

Los destinos de colocación también deben proporcionar más funcionalidad de la necesaria para controlar las transferencias del Portapapeles:

-   El destino drop debe exponer una [**interfaz IDropTarget.**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) Cuando el cursor está sobre una ventana de destino, el sistema usa **IDropTarget** para proporcionar al destino información como la posición del cursor y para notificarle cuándo se descartan los datos.
-   El destino de colocación debe registrarse en el sistema mediante una [**llamada a RegisterDragDrop**](/windows/win32/api/ole2/nf-ole2-registerdragdrop). Esta función proporciona al sistema el identificador de una ventana de destino y un puntero a la interfaz [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) de la aplicación de destino.

> [!Note]  
> Para las operaciones de arrastrar y colocar, la aplicación debe inicializar COM con [**OleInitialize,**](/windows/win32/api/ole2/nf-ole2-oleinitialize)no [**con CoInitialize.**](/windows/win32/api/objbase/nf-objbase-coinitialize)

 

En el procedimiento siguiente se describen los pasos esenciales que normalmente se usan para transferir datos de Shell con arrastrar y colocar:

1.  El destino llama [**a RegisterDragDrop para**](/windows/win32/api/ole2/nf-ole2-registerdragdrop) proporcionar al sistema un puntero a su [**interfaz IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y registrar una ventana como destino de colocación.
2.  Cuando el usuario inicia una operación de arrastrar y colocar, el origen crea un objeto de datos e inicia un bucle *de* arrastre mediante una llamada a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop).
3.  Cuando el cursor está sobre la ventana de destino, el sistema lo notifica mediante una llamada a uno de los métodos [**IDropTarget del**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) destino. El sistema llama a [**IDropTarget::D ragEnter**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter) cuando el cursor entra en la ventana de destino e [**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) a medida que el cursor pasa sobre la ventana de destino. Ambos métodos proporcionan al destino de colocación la posición actual del cursor y el estado de las teclas modificadoras de teclado, como CTRL o ALT. Cuando el cursor sale de la ventana de destino, el sistema notifica al destino mediante una llamada a [**IDropTarget::D ragLeave**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave). Cuando se devuelve cualquiera de estos métodos, el sistema llama a la [**interfaz IDropSource**](/windows/win32/api/oleidl/nn-oleidl-idropsource) para pasar el valor devuelto al origen.
4.  Cuando el usuario suelta el botón del mouse para quitar los datos, el sistema llama al método [**IDropTarget::D rop del**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop) destino. Entre los parámetros del método se encuentra un puntero a la interfaz [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) del objeto de datos.
5.  El destino llama al método [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) del objeto de datos para extraer los datos.
6.  Con algunas transferencias de datos de Shell, es posible que el destino también tenga que llamar al método [**IDataObject::SetData**](/windows/win32/api/objidl/nf-objidl-idataobject-setdata) del objeto de datos para proporcionar comentarios al origen sobre el resultado de la transferencia de datos.
7.  Cuando el destino finaliza con el objeto de datos, devuelve de [**IDropTarget::D rop**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop). El sistema devuelve la llamada a [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) del origen para notificar al origen que la transferencia de datos se ha completado.
8.  En función del escenario [de](datascenarios.md)transferencia de datos determinado, es posible que el origen deba realizar una acción adicional en función del valor devuelto por [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) y los valores que el destino pasa al objeto de datos. Por ejemplo, cuando se mueve un archivo, el origen debe comprobar estos valores para determinar si debe eliminar el archivo original.
9.  El origen libera el objeto de datos.

Aunque los procedimientos descritos anteriormente proporcionan un buen modelo general para la transferencia de datos de Shell, hay muchos tipos diferentes de datos que pueden incluirse en un objeto de datos de Shell. También hay una serie de escenarios de transferencia de datos diferentes que la aplicación podría necesitar controlar. Cada tipo de datos y escenario requiere un enfoque ligeramente diferente a los tres pasos clave del procedimiento:

-   Cómo construye un origen un objeto de datos para contener los datos de Shell.
-   Cómo un destino extrae datos de Shell del objeto de datos.
-   Cómo finaliza el origen la operación de transferencia de datos.

El [objeto de datos de shell](dataobject.md) proporciona una explicación general de cómo un origen construye un objeto de datos de Shell y cómo el destino puede controlar ese objeto de datos. [En Control de escenarios de transferencia](datascenarios.md) de datos de Shell se describe en detalle cómo controlar una serie de escenarios comunes de transferencia de datos de Shell.

 

 
