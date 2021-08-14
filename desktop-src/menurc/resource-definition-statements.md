---
title: Resource-Definition instrucciones
description: Las instrucciones de definición de recursos definen los recursos que el compilador de recursos coloca en el recurso (. Archivo Res).
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- compilador de recursos, instrucciones de definición de recursos
- Recurso TEXTINCLUDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4937eb9d5fb9bba7b174aa9543be8b3f2eb41c90c6bc20a72650114f57fb4fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869911"
---
# <a name="resource-definition-statements"></a>Resource-Definition instrucciones

Las instrucciones de definición de recursos definen los recursos que el compilador de recursos coloca en el recurso (. Archivo Res). Después de . El archivo Res está vinculado al archivo ejecutable; la aplicación puede cargar sus recursos en tiempo de ejecución según sea necesario. Todas las instrucciones de recursos asocian un nombre o número de identificación a un recurso determinado.

Las instrucciones de definición de recursos se pueden dividir en las siguientes categorías:

-   Recursos
-   Controles
-   Instrucciones

En las tablas siguientes se describen las instrucciones de definición de recursos.

## <a name="resources"></a>Recursos



| Recurso                                      | Descripción                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aceleradores**](accelerators-resource.md) | Define las teclas de aceleración del menú.                                                                                                                                                  |
| [**Bits**](bitmap-resource.md)             | Define un mapa de bits al asignarle un nombre y especificar el nombre del archivo que lo contiene. (Para usar un mapa de bits determinado, la aplicación lo solicita por nombre).                          |
| [**Cursor**](cursor-resource.md)             | Define un cursor o cursor animado al asignarle un nombre y especificar el nombre del archivo que lo contiene. (Para usar un cursor determinado, la aplicación lo solicita por nombre).       |
| [**Diálogo**](dialog-resource.md)             | Define una plantilla que una aplicación puede usar para crear cuadros de diálogo.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Define una plantilla que una aplicación puede usar para crear cuadros de diálogo.                                                                                                          |
| [**Fuente**](font-resource.md)                 | Especifica el nombre de un archivo que contiene una fuente.                                                                                                                              |
| [**Html**](html-resource.md)                 | Especifica un archivo HTML.                                                                                                                                                         |
| [**Icono**](icon-resource.md)                 | Define un icono o icono animado al asignarle un nombre y especificar el nombre del archivo que lo contiene. (Para usar un icono determinado, la aplicación lo solicita por nombre).            |
| [**Menú**](menu-resource.md)                 | Define la apariencia y la función de un menú.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Define la apariencia y la función de un menú.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Define una tabla de mensajes naming it and specifying the name of the file that contains it. El archivo es un archivo de recursos binarios generado por el compilador de mensajes.                |
| [**Popup**](popup-resource.md)               | Define un elemento de menú que puede contener elementos de menú y submenús.                                                                                                                   |
| **PLUGPLAY**                                  | Obsoleto.                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | Define los recursos de datos. Los recursos de datos permiten incluir datos binarios en el archivo ejecutable.                                                                                      |
| [**STRINGTABLE**](stringtable-resource.md)   | Define los recursos de cadena. Los recursos de cadena son cadenas Unicode o ASCII que se pueden cargar desde el archivo ejecutable.                                                            |
| **TEXTINCLUDE**                               | Un recurso especial interpretado por Visual C++. Para obtener más información, vea [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Un recurso especial que se usa con las opciones del vinculador [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) y [/TLBOUT.](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) |
| [**Definido por el usuario**](user-defined-resource.md) | Define un recurso que contiene datos específicos de la aplicación.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Define un recurso de información de versión. Contiene información como el número de versión, el sistema operativo previsto, y así sucesivamente.                                                  |
| **Vxd**                                       | Obsoleto.                                                                                                                                                                       |



 

Para obtener más información sobre los recursos de MFC predefinidos, vea [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) y [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Controles



| Control                                            | Descripción                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Crea un control de casilla automático de tres estados.                         |
| [**AUTOCHECKBOX**](autocheckbox-control.md)       | Crea un control de casilla automático.                                     |
| [**AUTORADIOBUTTON**](autoradiobutton-control.md) | Crea un control de botón de radio automático.                                  |
| [**Casilla**](checkbox-control.md)               | Crea un control de casilla.                                                |
| [**Combobox**](combobox-control.md)               | Crea un control de cuadro combinado.                                                |
| [**Control**](control-control.md)                 | Crea un control definido por la aplicación.                                     |
| [**CTEXT**](ctext-control.md)                     | Crea un control de texto centrado.                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | Crea un control pushbutton predeterminado.                                       |
| [**EDITTEXT**](edittext-control.md)               | Crea un control de edición.                                                    |
| [**Groupbox**](groupbox-control.md)               | Crea un control de cuadro de grupo.                                                |
| [**Icono**](icon-control.md)                       | Crea un control de icono. Este control es un icono que se muestra en un cuadro de diálogo. |
| [**Listbox**](listbox-control.md)                 | Crea un control de cuadro de lista.                                                 |
| [**LTEXT**](ltext-control.md)                     | Crea un control de texto alineado a la izquierda.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Crea un control de cuadro de inserción.                                                 |
| [**Pulsador**](pushbutton-control.md)           | Crea un control de botón de inserción.                                              |
| [**Radiobutton**](radiobutton-control.md)         | Crea un control de botón de radio.                                             |
| [**Rtext**](rtext-control.md)                     | Crea un control alineado a la derecha.                                            |
| [**SCROLLBAR**](scrollbar-control.md)             | Crea un control de barra de desplazamiento.                                               |
| [**STATE3**](state3-control.md)                   | Crea un control de casilla de tres estados.                                    |



 

## <a name="statements"></a>Instrucciones



| .                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Título**](caption-statement.md)                 | Establece el título de un cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Características**](characteristics-statement.md) | Especifica información sobre un recurso que puede usar la herramienta que puede leer o escribir archivos de definición de recursos.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Clase**](class-statement.md)                     | Establece la clase del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Establece el estilo de ventana extendido del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Fuente**](font-statement.md)                       | Establece la fuente con la que el sistema dibujará texto para el cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Lengua**](language-statement.md)               | Establece el idioma de todos los recursos hasta la siguiente [**instrucción LANGUAGE**](language-statement.md) o hasta el final del archivo. Cuando la **instrucción LANGUAGE** aparece antes del principio del cuerpo de una definición de recursos [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU,**](menu-resource.md) [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE,**](stringtable-resource.md) el idioma especificado solo se aplica a ese recurso. |
| [**Menú**](menu-statement.md)                       | Establece el menú del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Menuitem**](menuitem-statement.md)               | Define un elemento de menú.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Estilo**](style-statement.md)                     | Establece el estilo de ventana del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Versión**](version-statement.md)                 | Especifica la información de versión de un recurso que puede usar la herramienta que puede leer o escribir archivos de definición de recursos.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 