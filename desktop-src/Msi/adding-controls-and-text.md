---
description: Los controles y el texto colocados en los cuadros de diálogo y las cartelera permiten al usuario interactuar con el proceso de instalación.
ms.assetid: 2c6204c7-535d-4dda-8394-723ddbf46b96
title: Agregar controles y texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706d071741d742205d0df2b19c4416acf355fd7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652628"
---
# <a name="adding-controls-and-text"></a>Agregar controles y texto

Los controles y el texto colocados en los cuadros de diálogo y las cartelera permiten al usuario interactuar con el proceso de instalación. Agregue un cuadro de diálogo a la interfaz de usuario incluyéndolo en la [tabla del cuadro de diálogo](dialog-table.md) , tal como se describe en [uso de la interfaz de usuario](using-the-user-interface.md). Rellene los cuadros de diálogo y las cartelera con controles rellenando la [tabla de control](control-table.md) y la [tabla BBControl](bbcontrol-table.md), respectivamente.

Los atributos iniciales de control se pueden especificar en la columna Attributes de la [tabla de control](control-table.md). Vea [atributos de control](control-attributes.md).

Para que los atributos de control dependan de una condición, utilice la [tabla ControlCondition](controlcondition-table.md) para deshabilitar, habilitar, ocultar o mostrar un control según el valor de una propiedad o una instrucción condicional. También puede usar esta tabla para invalidar la especificación del control predeterminado especificado en la [tabla del cuadro de diálogo](dialog-table.md).

Para que un evento cambie un atributo de control, suscríbase el control a un ControlEvent, en la [tabla EventMapping](eventmapping-table.md). Un ControlEvent, especifica una acción que debe realizar el instalador o un cambio en los atributos de uno o más controles del cuadro de diálogo. Consulte [información general de ControlEvent,](controlevent-overview.md). Escriba el identificador del atributo en la columna Attribute y el identificador de ControlEvent, en la columna Event de la [tabla EventMapping](eventmapping-table.md).

Algunos controles facilitan la recopilación de información del usuario. Por ejemplo, una casilla permite al usuario establecer el valor de una propiedad. Vea la [tabla CheckBox](checkbox-table.md), la [tabla ComboBox](combobox-table.md), la [tabla ListBox](listbox-table.md), la [tabla RadioButton](radiobutton-table.md)y la [tabla ListView](listview-table.md).

Tenga en cuenta que, por motivos de seguridad, las propiedades privadas no se pueden cambiar por el usuario que interactúa con la interfaz de usuario. Si la interfaz de usuario va a establecer una propiedad, debe ser una propiedad pública y tener un nombre en mayúsculas. Vea [acerca de las propiedades](about-properties.md).

Puede hacer que el cuadro de diálogo presente información al usuario o escribirlo en un registro en respuesta a las acciones de instalación rellenando la [tabla ActionText](actiontext-table.md).

Los controles pueden tener un estilo de fuente predefinido. Para establecer la fuente y el estilo de fuente de una cadena de texto, anteponga a la cadena de caracteres mostrados el prefijo { \\ style} o {&*Style*}. Donde Style es un identificador que aparece en la columna TextStyle de la [tabla TextStyle](textstyle-table.md). Si ninguno de ellos está presente, pero la propiedad [**DefaultUIFont**](defaultuifont.md) se define como un estilo de texto válido, se usará esa fuente.

Se recomienda establecer la propiedad [**DefaultUIFont**](defaultuifont.md) de cada paquete de instalación con una interfaz de usuario en la [tabla de propiedades](property-table.md) en uno de los estilos predefinidos enumerados en la [tabla de TextStyle](textstyle-table.md). Si no se especifica esta propiedad, el instalador utiliza la fuente del sistema. Esto puede hacer que el instalador muestre de forma incorrecta cadenas de texto si la página de códigos del paquete es diferente de la página de códigos predeterminada de la interfaz de usuario del usuario.

Para la mayoría de los controles, el texto se muestra utilizando el juego de caracteres que se especifica en la página de códigos de la base de datos. Esto garantiza que se usa el juego de caracteres correcto con la información contenida en la base de datos. Las excepciones a esto son los controles [Edit](edit-control.md), [DirectoryList](directorylist-control.md), [PathEdit](pathedit-control.md)y [DirectoryCombo](directorycombo-control.md) , que siempre muestran texto mediante el juego de caracteres predeterminado de la interfaz de usuario del usuario. Los controles de [texto](text-control.md), [cuadro de lista](listbox-control.md)y [cuadro combinado](combobox-control.md) utilizan el juego de caracteres predeterminado de la interfaz de usuario si se establece el [atributo de control UsersLanguage](userslanguage-control-attribute.md) .

En algunos casos, un control puede volver a dibujarse incorrectamente al cancelar un cuadro de diálogo. Esto tiene que hacer con el orden en que los controles reciben mensajes de WM \_ Paint después de quitar el cuadro de diálogo **Cancelar** . Para corregirlo, intente cambiar el orden de los controles en la tabla de control.

Los controles deben ser lo suficientemente grandes como para dar cabida a todo el texto que se ve en todas las configuraciones de tamaño de fuente. Los controles deben ser lo suficientemente grandes como para dar cabida a todo el texto localizado, si se puede localizar el texto de la interfaz de usuario. Los tamaños de fuente más grandes o el texto localizado pueden requerir más espacio que el texto original y pueden truncarse con un control que se hace demasiado pequeño. Para obtener más información sobre cómo localizar el texto de la interfaz de usuario, consulte la sección: [ejemplo de localización](a-localization-example.md).

 

 



