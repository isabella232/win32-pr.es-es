---
title: Arrastrar y colocar
description: Arrastrar y colocar hace referencia a las transferencias de datos en las que se usa un mouse u otro dispositivo señalador para especificar el origen de datos y su destino.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704675"
---
# <a name="drag-and-drop"></a>Arrastrar y colocar

*Arrastrar y colocar* hace referencia a las transferencias de datos en las que se usa un mouse u otro dispositivo señalador para especificar el origen de datos y su destino. En una operación típica de arrastrar y colocar, un usuario selecciona el objeto que se va a transferir moviendo el puntero del mouse y manteniendo presionado el botón izquierdo o algún otro botón designado para este fin. Mientras continúa manteniendo presionado el botón, el usuario inicia la transferencia arrastrando el objeto hasta su destino, que puede ser cualquier contenedor OLE. Arrastrar y colocar proporciona exactamente la misma funcionalidad que el portapapeles OLE copiar y pegar, pero agrega comentarios visuales y elimina la necesidad de menús. De hecho, si una aplicación admite la copia y pegado del portapapeles, se necesita poco más para admitir las operaciones de arrastrar y colocar.

Durante una operación de arrastrar y colocar de OLE, se usan los siguientes tres fragmentos de código independientes.



| Origen de código de arrastrar y colocar                               | Implementación y uso                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaz [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Implementado por el objeto que contiene los datos arrastrados, a los que se hace referencia como el *origen de arrastre*.<br/>                                                                                         |
| [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) (interfaz)<br/> | Implementado por el objeto que está pensado para aceptar la eliminación, a la que se hace referencia como *destino de colocación*.<br/>                                                                                 |
| [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) , función<br/>    | Implementado por OLE y se usa para iniciar una operación de arrastrar y colocar. Una vez que la operación está en curso, facilita la comunicación entre el origen de arrastre y el destino de colocación.<br/> |



 

Las interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) se pueden implementar en un contenedor o en una aplicación de objeto. El rol de origen de arrastre o destino de colocación no se limita a un tipo de aplicación OLE.

La función [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) de OLE implementa un bucle que realiza un seguimiento de los movimientos del mouse y del teclado hasta el momento en que se cancela la acción de arrastrar o se produce una caída. **DoDragDrop** es la función clave en el proceso de arrastrar y colocar, facilitando la comunicación entre el origen de arrastre y el destino de colocación.

Durante una operación de arrastrar y colocar, se pueden mostrar tres tipos de comentarios al usuario.



| Tipo de comentarios            | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comentarios de origen<br/>  | Proporcionado por el origen de arrastre, los comentarios del origen indican que los datos se están arrastrando y no cambian durante el transcurso del arrastre. Normalmente, los datos se resaltan para indicar que se ha seleccionado.<br/>                                                                                                                                            |
| Comentarios del puntero<br/> | Proporcionado por el origen de arrastre, los comentarios del puntero indican lo que ocurre si se suelta el mouse en un momento dado. Los comentarios del puntero cambian continuamente a medida que el usuario mueve el mouse o presiona una tecla modificadora. Por ejemplo, si el puntero se mueve a una ventana que no puede aceptar una colocación, el puntero cambia al símbolo "no permitido".<br/> |
| Comentarios de destino<br/>  | Proporcionado por el destino de colocación, los comentarios de destino indican dónde debe realizarse la eliminación.<br/>                                                                                                                                                                                                                                                                    |



 

Para obtener más información, vea [arrastrar responsabilidades del origen](drag-source-responsibilities.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

 





