---
title: Usar Tree-View controles
description: Esta sección contiene detalles de implementación y código de ejemplo para trabajar con controles de vista de árbol.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ed8d1040a635964e772b8399a5c476e67f9aba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165277"
---
# <a name="using-tree-view-controls"></a>Usar Tree-View controles

Esta sección contiene detalles de implementación y código de ejemplo para trabajar con controles de vista de árbol.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo crear un control Tree-View control](create-a-tree-view-control.md)<br/>       | Para crear un control de vista de árbol, use la [**función CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) y especifique el valor [**\_ TREEVIEW de WC**](common-control-window-classes.md) para la clase de ventana. La clase de ventana de vista de árbol se registra en el espacio de direcciones de la aplicación cuando se carga la DLL de control común. Para asegurarse de que se carga el archivo DLL, use la [**función InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) <br/>                                                                    |
| [Inicialización de la lista de imágenes](initialize-the-image-list.md)<br/>         | Cada elemento de un control de vista de árbol puede tener dos imágenes asociadas. Un elemento muestra una imagen cuando se selecciona y la otra cuando no lo está. Para incluir imágenes con elementos de vista de árbol, use primero las funciones [Listas](image-lists.md) de imágenes para crear una lista de imágenes y agregarle imágenes. A continuación, asocie la lista de imágenes con el control de vista de árbol mediante el mensaje [**\_ SETIMAGELIST de TVM.**](tvm-setimagelist.md) <br/>                                                                     |
| [Cómo agregar elementos Tree-View datos](add-tree-view-items.md)<br/>                     | Para agregar un elemento a un control de vista de árbol, envíe el mensaje [**\_ INSERTITEM**](tvm-insertitem.md) de TVM al control. El mensaje incluye la dirección de una estructura [**TVINSERTSTRUCT,**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) especificando el elemento primario, el elemento después del cual se inserta el nuevo elemento y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define los atributos del elemento. Los atributos incluyen la etiqueta del elemento, sus imágenes seleccionadas y no seleccionadas, y un valor definido por la aplicación de 32 bits. <br/> |
| [Cómo arrastrar un elemento Tree-View datos](drag-a-tree-view-item.md)<br/>                 | En este tema se muestra el código para controlar el arrastre y la colocación de elementos de vista de árbol. El código de ejemplo consta de tres funciones. La primera función comienza la operación de arrastre, la segunda función arrastra la imagen y la tercera finaliza la operación de arrastre. <br/>                                                                                                                                                                                                                                  |
| [Cómo trabajar con índices de imagen de estado](work-with-state-image-indexes.md)<br/> | A menudo hay confusión sobre cómo establecer y recuperar el índice de imagen de estado en un control de vista de árbol. En los ejemplos siguientes se muestra el método adecuado para establecer y recuperar el índice de imagen de estado. En los ejemplos se supone que solo hay dos índices de imagen de estado en el control de vista de árbol, desactivados y activados. Si la aplicación contiene más de dos, estas funciones tendrán que modificarse para controlar ese caso. <br/>                                                               |
| [Cómo usar información Tree-View datos](use-tree-view-infotips.md)<br/>               | Al aplicar el estilo [**\_ INFOTIP**](tree-view-control-window-styles.md) de TVS a un control de vista de árbol, genera notificaciones [ \_ GETINFOTIP](tvn-getinfotip.md) de TVN cuando el cursor está sobre un elemento de la vista de árbol. Al responder a esta notificación, puede establecer el texto que aparece en la información. <br/>                                                                                                                                                                                    |



 

 

