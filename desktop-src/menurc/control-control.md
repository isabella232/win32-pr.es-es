---
title: Control CONTROL
description: Define un control definido por el usuario.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- CONTROLAR los menús de control y otros recursos
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995187"
---
# <a name="control-control"></a>Control CONTROL

Define un control definido por el usuario.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*las*
</dt> <dd>

Nombre redefinido, cadena de caracteres o valor entero sin signo de 16 bits que define la clase. Puede ser cualquiera de las clases de control. para obtener una lista de las clases de control, vea la primera lista que sigue a esta descripción. Si el valor es un nombre redefinido proporcionado por la aplicación, debe ser una cadena entre comillas dobles (").

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Nombre redefinido o valor entero que especifica el estilo del control dado. El significado exacto de *Style* depende del valor de la *clase* . En las secciones que siguen a esta descripción se muestran las clases de control y los estilos correspondientes.

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="remarks"></a>Observaciones

Las seis clases de control posibles se describen en las secciones siguientes.

### <a name="the-button-control-class"></a>La clase de control Button

Un control de botón es una pequeña ventana secundaria rectangular que el usuario puede activar o desactivar haciendo clic en él con el mouse. Los controles de botón se pueden usar solo o en grupos, y se pueden etiquetar o mostrar sin texto. Los controles de botón normalmente cambian de apariencia cuando el usuario hace clic en ellos.

Los estilos de botón se describen en el tema siguiente: [estilos de botón](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>Clase de control de cuadro combinado

Los controles de cuadro combinado constan de un campo de selección similar a un control de edición y un cuadro de lista. El cuadro de lista se puede mostrar en todo momento o se puede desplegar cuando el usuario selecciona un "cuadro de lista desplegable" junto al campo de selección.

Dependiendo del estilo del cuadro combinado, el usuario puede o no puede editar el contenido del campo de selección. Si el cuadro de lista está visible, si escribe caracteres en el cuadro de selección, se resaltará la primera entrada que coincida con los caracteres escritos. Por el contrario, al seleccionar un elemento en el cuadro de lista se muestra el texto seleccionado en el campo de selección.

Los estilos de control de cuadro combinado se describen en el tema siguiente: [estilos de cuadro combinado](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Clase Edit control

Un control de edición es una ventana secundaria rectangular en la que el usuario puede escribir texto desde el teclado. El usuario selecciona el control y le asigna el foco de entrada; para ello, hace clic en el mouse dentro de él o presiona la tecla TAB. El usuario puede escribir texto cuando el control muestra un punto de inserción parpadeante. El mouse se puede usar para mover el cursor y seleccionar los caracteres que se van a reemplazar, o para colocar el cursor para insertar caracteres. La tecla retroceso se puede utilizar para eliminar caracteres.

Los controles de edición utilizan la fuente de punto fijo y muestran caracteres Unicode. Expanden los caracteres de tabulación en tantos caracteres de espacio como sean necesarios para colocar el cursor en la siguiente posición de tabulación. Se supone que las tabulaciones están en cada octava posición de carácter.

Los estilos de control de edición se describen en el tema siguiente: [Editar estilos de control](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>Clase de control de cuadro de lista

Los controles de cuadro de lista constan de una lista de cadenas de caracteres. El control se usa siempre que una aplicación necesita presentar una lista de nombres, como nombres de archivo, que el usuario puede ver y seleccionar. El usuario puede seleccionar una cadena seleccionando la cadena con el mouse y haciendo clic en un botón del mouse. Cuando se selecciona una cadena, se resalta y se pasa un mensaje de notificación a la ventana primaria. Se puede usar una barra de desplazamiento con un control de cuadro de lista para desplazarse por las listas demasiado largas o demasiado anchas para la ventana de control.

Los estilos de control de cuadro de lista se describen en el tema siguiente: [estilos de cuadro de lista](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Clase de control Scroll-Bar

Un control de barra de desplazamiento es un rectángulo que contiene un control de desplazamiento y tiene flechas de dirección en ambos extremos. La barra de desplazamiento envía un mensaje de notificación a su elemento primario cada vez que el usuario hace clic con el mouse en el control. El elemento primario es responsable de actualizar la posición del control, si es necesario. Los controles de barra de desplazamiento tienen la misma apariencia y función que las barras de desplazamiento usadas en las ventanas normales. Pero a diferencia de las barras de desplazamiento, los controles de barra de desplazamiento se pueden colocar en cualquier parte dentro de una ventana y usarse siempre que sea necesario para proporcionar la entrada de desplazamiento para una ventana.

Los estilos de barra de desplazamiento se describen en el tema siguiente: [estilos de control de barra de desplazamiento](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>La clase de control estática

Los controles estáticos son campos de texto simples, cuadros y rectángulos que se pueden usar para etiquetar, mostrar o separar otros controles. Los controles estáticos no toman ninguna entrada y no proporcionan ninguna salida.

Los estilos de control estático se describen en el tema siguiente: [estilos de control estáticos](../controls/static-control-styles.md).

 

 