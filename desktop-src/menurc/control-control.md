---
title: Control CONTROL
description: Define un control definido por el usuario.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Menús de control control y otros recursos
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570596"
---
# <a name="control-control"></a>Control CONTROL

Define un control definido por el usuario.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Clase*
</dt> <dd>

Nombre redefinido, cadena de caracteres o un valor entero de 16 bits sin signo que define la clase. Puede ser cualquiera de las clases de control; Para obtener una lista de las clases de control, vea la primera lista que sigue a esta descripción. Si el valor es un nombre redefinido proporcionado por la aplicación, debe ser una cadena entre comillas dobles (").

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Nombre o valor entero redefinido que especifica el estilo del control especificado. El significado exacto del *estilo* depende del valor *de clase.* En las secciones siguientes a esta descripción se muestran las clases de control y los estilos correspondientes.

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="remarks"></a>Observaciones

Las seis clases de control posibles se describen en las secciones siguientes.

### <a name="the-button-control-class"></a>Clase de control Button

Un control de botón es una pequeña ventana secundaria rectangular que el usuario puede activar o desactivar haciendo clic con el mouse. Los controles de botón se pueden usar solos o en grupos, y se pueden etiquetar o aparecer sin texto. Los controles de botón suelen cambiar la apariencia cuando el usuario hace clic en ellos.

Los estilos de botón se describen en el tema siguiente: [Estilos de botón](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>Clase de control Combo Box

Los controles de cuadro combinado constan de un campo de selección similar a un control de edición más un cuadro de lista. El cuadro de lista se puede mostrar en todo momento o se puede descartar cuando el usuario selecciona un "cuadro emergente" junto al campo de selección.

Según el estilo del cuadro combinado, el usuario puede o no puede editar el contenido del campo de selección. Si el cuadro de lista está visible, escribir caracteres en el cuadro de selección hará que se resalte la primera entrada que coincida con los caracteres escritos. Por el contrario, al seleccionar un elemento en el cuadro de lista se muestra el texto seleccionado en el campo de selección.

Los estilos de control de cuadro combinado se describen en el tema siguiente: [Estilos de cuadro combinado](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Clase de control Edit

Un control de edición es una ventana secundaria rectangular en la que el usuario puede escribir texto desde el teclado. El usuario selecciona el control y le proporciona el foco de entrada; para ello, hace clic con el mouse dentro de él o presiona la tecla TAB. El usuario puede escribir texto cuando el control muestra un punto de inserción intermitente. El mouse se puede usar para mover el cursor y seleccionar los caracteres que se reemplazarán, o para colocar el cursor para insertar caracteres. La tecla BACKSPACE se puede usar para eliminar caracteres.

Los controles de edición usan la fuente de paso fijo y muestran caracteres Unicode. Expanden los caracteres de tabulación en tantos caracteres de espacio como sean necesarios para mover el cursor a la siguiente tabulación. Se supone que las tabulaciones están en cada posición de ocho caracteres.

Los estilos de control de edición se describen en el tema siguiente: [Editar estilos de control](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>Clase de control List Box

Los controles de cuadro de lista constan de una lista de cadenas de caracteres. El control se usa siempre que una aplicación necesita presentar una lista de nombres, como nombres de archivo, que el usuario puede ver y seleccionar. El usuario puede seleccionar una cadena si apunta a la cadena con el mouse y hace clic en un botón del mouse. Cuando se selecciona una cadena, se resalta y se pasa un mensaje de notificación a la ventana primaria. Se puede usar una barra de desplazamiento con un control de cuadro de lista para desplazar listas que son demasiado largas o demasiado anchas para la ventana de control.

Los estilos de control de cuadro de lista se describen en el tema siguiente: [Estilos de cuadro de lista](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Clase Scroll-Bar control

Un control de barra de desplazamiento es un rectángulo que contiene un control de desplazamiento y tiene flechas de dirección en ambos extremos. La barra de desplazamiento envía un mensaje de notificación a su elemento primario cada vez que el usuario hace clic en el mouse en el control. El elemento primario es responsable de actualizar la posición del control, si es necesario. Los controles de barra de desplazamiento tienen la misma apariencia y función que las barras de desplazamiento usadas en ventanas normales. Pero a diferencia de las barras de desplazamiento, los controles de barra de desplazamiento se pueden colocar en cualquier lugar dentro de una ventana y usarse siempre que sea necesario para proporcionar una entrada de desplazamiento para una ventana.

Los estilos de barra de desplazamiento se describen en el tema siguiente: Estilos [de control de barra de desplazamiento](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>Clase de control static

Los controles estáticos son campos de texto simples, cuadros y rectángulos que se pueden usar para etiquetar, box o separar otros controles. Los controles estáticos no toman ninguna entrada y no proporcionan ninguna salida.

Los estilos de control estático se describen en el tema siguiente: [Estilos de control estáticos](../controls/static-control-styles.md).

 

 