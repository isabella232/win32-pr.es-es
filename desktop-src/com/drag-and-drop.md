---
title: Arrastrar y colocar
description: Arrastrar y colocar hace referencia a las transferencias de datos en las que se usa un mouse u otro dispositivo que apunta para especificar el origen de datos y su destino.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b388fc6c051fa73c72720d1f349cd50a4fa6902b8f880fbf5ccfb4cf263a4227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993165"
---
# <a name="drag-and-drop"></a>Arrastrar y colocar

*Arrastrar y colocar* hace referencia a las transferencias de datos en las que se usa un mouse u otro dispositivo que apunta para especificar el origen de datos y su destino. En una operación típica de arrastrar y colocar, un usuario selecciona el objeto que se va a transferir moviendo el puntero del mouse a él y manteniendo presionado el botón izquierdo o algún otro botón designado para este propósito. Mientras mantiene presionado el botón, el usuario inicia la transferencia arrastrando el objeto a su destino, que puede ser cualquier contenedor OLE. Arrastrar y colocar proporciona exactamente la misma funcionalidad que copiar y pegar del Portapapeles OLE, pero agrega comentarios visuales y elimina la necesidad de menús. De hecho, si una aplicación admite la copia y pegado del Portapapeles, se necesita poco adicional para admitir la arrastrar y colocar.

Durante una operación de arrastrar y colocar de OLE, se usan los tres fragmentos de código independientes siguientes.



| Código fuente de arrastrar y colocar                               | Implementación y uso                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaz IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)<br/> | Implementado por el objeto que contiene los datos arrastrados, denominado origen *de arrastre.*<br/>                                                                                         |
| [**Interfaz IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)<br/> | Implementado por el objeto que está pensado para aceptar la colocación, denominado destino *de colocación.*<br/>                                                                                 |
| [**Función DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)<br/>    | Se implementa mediante OLE y se usa para iniciar una operación de arrastrar y colocar. Una vez que la operación está en curso, facilita la comunicación entre el origen de arrastre y el destino de colocación.<br/> |



 

Las [**interfaces IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) [**e IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) se pueden implementar en un contenedor o en una aplicación de objeto. El rol de arrastrar origen o destino de colocación no se limita a ningún tipo de aplicación OLE.

La función OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementa un bucle que realiza un seguimiento del movimiento del mouse y del teclado hasta que se cancela la arrastre o se produce una colocación. **DoDragDrop es la** función clave en el proceso de arrastrar y colocar, lo que facilita la comunicación entre el origen de arrastre y el destino de colocación.

Durante una operación de arrastrar y colocar, se pueden mostrar tres tipos de comentarios al usuario.



| Tipo de comentarios            | Descripción                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comentarios de origen<br/>  | Proporcionado por el origen de arrastre, los comentarios de origen indican que los datos se arrastran y no cambian durante el transcurso del arrastre. Normalmente, los datos se resaltan para indicar que se han seleccionado.<br/>                                                                                                                                            |
| Comentarios de puntero<br/> | Proporcionado por el origen de arrastre, los comentarios del puntero indican lo que sucede si el mouse se libera en un momento dado. Los comentarios de puntero cambian continuamente a medida que el usuario mueve el mouse o presiona una tecla modificadora. Por ejemplo, si el puntero se mueve a una ventana que no puede aceptar una colocación, el puntero cambia al símbolo "no permitido".<br/> |
| Comentarios de destino<br/>  | Proporcionado por el destino de colocación, los comentarios de destino indican dónde se va a producir la colocación.<br/>                                                                                                                                                                                                                                                                    |



 

Para obtener más información, vea [Arrastrar responsabilidades de origen.](drag-source-responsibilities.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

 





