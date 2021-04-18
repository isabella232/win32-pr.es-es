---
title: Usar controles Tree-View
description: Esta sección contiene detalles de implementación y código de ejemplo para trabajar con controles de vista de árbol.
ms.assetid: 37736770-5030-4f8a-a020-6897ed5f4e96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ed8d1040a635964e772b8399a5c476e67f9aba
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656425"
---
# <a name="using-tree-view-controls"></a>Usar controles Tree-View

Esta sección contiene detalles de implementación y código de ejemplo para trabajar con controles de vista de árbol.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo crear un control de Tree-View](create-a-tree-view-control.md)<br/>       | Para crear un control de vista de árbol, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando el valor [**\_ TREEVIEW de CT**](common-control-window-classes.md) para la clase de ventana. La clase de ventana de vista de árbol se registra en el espacio de direcciones de la aplicación cuando se carga el archivo DLL de control común. Para asegurarse de que se carga el archivo DLL, utilice la función [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) . <br/>                                                                    |
| [Cómo inicializar la lista de imágenes](initialize-the-image-list.md)<br/>         | Cada elemento de un control de vista de árbol puede tener dos imágenes asociadas a él. Un elemento muestra una imagen cuando se selecciona y la otra cuando no lo está. Para incluir imágenes con elementos de vista de árbol, use primero las funciones de las [listas de imágenes](image-lists.md) para crear una lista de imágenes y agregarle imágenes. A continuación, asocie la lista de imágenes con el control de vista de árbol mediante el mensaje [**TVM \_ SETIMAGELIST**](tvm-setimagelist.md) . <br/>                                                                     |
| [Cómo agregar elementos de Tree-View](add-tree-view-items.md)<br/>                     | Un elemento se agrega a un control de vista de árbol mediante el envío del mensaje de la [**\_ INSERTITEM de TVM**](tvm-insertitem.md) al control. El mensaje incluye la dirección de una estructura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , especificando el elemento primario, el elemento después del cual se inserta el nuevo elemento y una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define los atributos del elemento. Los atributos incluyen la etiqueta del elemento, sus imágenes seleccionadas y no seleccionadas y un valor definido por la aplicación de 32 bits. <br/> |
| [Cómo arrastrar un elemento de Tree-View](drag-a-tree-view-item.md)<br/>                 | En este tema se muestra el código para controlar el arrastre y la colocación de los elementos de la vista de árbol. El código de ejemplo consta de tres funciones. La primera función comienza la operación de arrastre, la segunda función arrastra la imagen y la tercera función finaliza la operación de arrastre. <br/>                                                                                                                                                                                                                                  |
| [Cómo trabajar con índices de imagen de estado](work-with-state-image-indexes.md)<br/> | A menudo hay confusión sobre cómo establecer y recuperar el índice de la imagen de estado en un control de vista de árbol. En los siguientes ejemplos se muestra el método adecuado para establecer y recuperar el índice de la imagen de estado. En los ejemplos se da por hecho que solo hay dos índices de imagen de estado en el control de vista de árbol, desactivados y comprobados. Si la aplicación contiene más de dos, estas funciones deberán modificarse para controlar ese caso. <br/>                                                               |
| [Cómo usar Tree-View recuadros informativos](use-tree-view-infotips.md)<br/>               | Cuando se aplica el estilo de recuadro de [**TV \_**](tree-view-control-window-styles.md) a un control de vista de árbol, genera notificaciones de [TVN \_ GETINFOTIP](tvn-getinfotip.md) cuando el cursor está sobre un elemento de la vista de árbol. Al responder a esta notificación, puede establecer el texto que aparece en el recuadro informativo. <br/>                                                                                                                                                                                    |



 

 

