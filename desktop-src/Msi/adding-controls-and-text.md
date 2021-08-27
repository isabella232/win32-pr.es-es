---
description: Los controles y el texto colocados en cuadros de diálogo y paneles permiten al usuario interactuar con el proceso de instalación.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Agregar controles y texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58602c4d793b25e1670373773ac8d3f5be2399c6351e56ebe2de1579c78ddcc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046035"
---
# <a name="adding-controls-and-text"></a>Agregar controles y texto

Los controles y el texto colocados en cuadros de diálogo y paneles permiten al usuario interactuar con el proceso de instalación. Agregue un cuadro de diálogo a la interfaz de usuario incluyéndolo en la [tabla Dialog](dialog-table.md) como se describe en Using [the Interfaz de usuario](using-the-user-interface.md). Rellene los cuadros de diálogo y los paneles con controles rellenando la [tabla Control](control-table.md) y la [tabla BBControl](bbcontrol-table.md), respectivamente.

Los atributos iniciales del control se pueden especificar en la columna Atributos de la [tabla Control](control-table.md). Vea [Atributos de control](control-attributes.md).

Para que los atributos de control dependan de una condición, use la [tabla ControlCondition](controlcondition-table.md) para deshabilitar, habilitar, ocultar o mostrar un control según el valor de una propiedad o instrucción condicional. También puede usar esta tabla para invalidar la especificación del control predeterminado especificado en la tabla [Dialog](dialog-table.md).

Para que un evento cambie un atributo de control, suscriba el control a un control ControlEvent en la [tabla EventMapping](eventmapping-table.md). Un control ControlEvent especifica una acción que debe realizar el instalador o un cambio en los atributos de uno o varios controles en el cuadro de diálogo. Consulte [Información general de ControlEvent.](controlevent-overview.md) Escriba el identificador del atributo en la columna Attribute y el identificador de ControlEvent en la columna Event de la [tabla EventMapping](eventmapping-table.md).

Algunos controles facilitan la recopilación de información del usuario. Por ejemplo, una casilla permite al usuario establecer el valor de una propiedad. Vea la [tabla CheckBox](checkbox-table.md), la [tabla ComboBox](combobox-table.md), la [tabla ListBox](listbox-table.md), la [tabla RadioButton](radiobutton-table.md)y la [tabla ListView](listview-table.md).

Tenga en cuenta que, por motivos de seguridad, el usuario que interactúa con la interfaz de usuario no puede cambiar las propiedades privadas. Si una propiedad se va a establecer mediante la interfaz de usuario, debe ser una propiedad pública y tener un nombre en mayúsculas. Vea [Acerca de las propiedades](about-properties.md).

Puede hacer que el cuadro de diálogo presente información al usuario o escribirla en un registro en respuesta a las acciones de instalación rellenando la [tabla ActionText](actiontext-table.md).

Los controles pueden tener un estilo de fuente predefinido. Para establecer la fuente y el estilo de fuente de una cadena de texto, antefirima la cadena de caracteres mostrados con { style} o \\ {&*style*}. Donde style es un identificador enumerado en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la [**propiedad DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.

Se recomienda establecer la propiedad [**DefaultUIFont**](defaultuifont.md) de cada paquete de instalación con una interfaz de usuario en la tabla [Property](property-table.md) en uno de los estilos predefinidos enumerados en la [tabla TextStyle](textstyle-table.md). Si no se especifica esta propiedad, el instalador usa la fuente System. Esto puede hacer que el instalador muestre incorrectamente cadenas de texto si la página de códigos del paquete es diferente de la página de códigos predeterminada de la interfaz de usuario del usuario.

Para la mayoría de los controles, el texto se muestra mediante el juego de caracteres especificado por la página de códigos de la base de datos. Esto garantiza que se usa el juego de caracteres correcto con la información contenida en la base de datos. Las excepciones a esto son los controles [Edit](edit-control.md), [DirectoryList](directorylist-control.md), [PathEdit](pathedit-control.md)y [DirectoryCombo,](directorycombo-control.md) que siempre muestran texto con el juego de caracteres de interfaz de usuario predeterminado del usuario. Los [controles Text](text-control.md), [ListBox](listbox-control.md)y [ComboBox](combobox-control.md) usan el juego de caracteres de interfaz de usuario predeterminado del usuario si se establece el atributo [de control UsersLanguage.](userslanguage-control-attribute.md)

En algunos casos, un control puede volver a dibujarse incorrectamente al cancelar un cuadro de diálogo. Esto tiene que ver con el orden en que los controles reciben mensajes \_ WM PAINT después de quitar el cuadro **de** diálogo Cancelar. Para corregirlo, intente cambiar el orden de los controles de la tabla Control.

Los controles deben ser lo suficientemente grandes como para dar cabida a todo el texto que se ve en toda la configuración de tamaño de fuente. Los controles deben ser lo suficientemente grandes como para dar cabida a todo el texto localizado, si se puede localizar el texto de la interfaz de usuario. Los tamaños de fuente más grandes o el texto localizado pueden requerir más espacio que el texto original y pueden truncarse mediante un control que se hace demasiado pequeño. Para obtener más información sobre la localización del texto de la interfaz de usuario, vea la sección: [Ejemplo de localización](a-localization-example.md).

 

 



