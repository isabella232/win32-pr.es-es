---
title: Instrucciones de Resource-Definition
description: Las instrucciones de definición de recursos definen los recursos que el compilador de recursos coloca en el recurso (. Res).
ms.assetid: f96b8c1e-8188-40b7-8eda-c13b61b8fc41
keywords:
- compilador de recursos, instrucciones de definición de recursos
- Recurso TEXTINCLUDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8887c002bc3564288eb99fdb373ac26c286d1bf7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995243"
---
# <a name="resource-definition-statements"></a>Instrucciones de Resource-Definition

Las instrucciones de definición de recursos definen los recursos que el compilador de recursos coloca en el recurso (. Res). Después de. El archivo res está vinculado al archivo ejecutable, la aplicación puede cargar sus recursos en tiempo de ejecución según sea necesario. Todas las instrucciones de recursos asocian un nombre o número de identificación a un recurso determinado.

Las instrucciones de definición de recursos se pueden dividir en las siguientes categorías:

-   Recursos
-   Controles
-   Instrucciones

En las tablas siguientes se describen las instrucciones de definición de recursos.

## <a name="resources"></a>Recursos



| Recurso                                      | Descripción                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACELERADORES**](accelerators-resource.md) | Define las teclas de aceleración del menú.                                                                                                                                                  |
| [**MYBITMAP**](bitmap-resource.md)             | Define un mapa de bits asignándole un nombre y especifica el nombre del archivo que lo contiene. (Para usar un mapa de bits determinado, la aplicación lo solicita por nombre).                          |
| [**CURSOR**](cursor-resource.md)             | Define un cursor o un cursor animado asignándole un nombre y especificando el nombre del archivo que lo contiene. (Para utilizar un cursor determinado, la aplicación lo solicita por nombre).       |
| [**DIÁLOGO**](dialog-resource.md)             | Define una plantilla que una aplicación puede utilizar para crear cuadros de diálogo.                                                                                                          |
| [**DIALOGEX**](dialogex-resource.md)         | Define una plantilla que una aplicación puede utilizar para crear cuadros de diálogo.                                                                                                          |
| [**TIPO**](font-resource.md)                 | Especifica el nombre de un archivo que contiene una fuente.                                                                                                                              |
| [**HTML**](html-resource.md)                 | Especifica un archivo HTML.                                                                                                                                                         |
| [**ICONO**](icon-resource.md)                 | Define un icono o un Icono animado asignándole un nombre y especificando el nombre del archivo que lo contiene. (Para usar un icono determinado, la aplicación lo solicita por nombre).            |
| [**MENU**](menu-resource.md)                 | Define la apariencia y la función de un menú.                                                                                                                                  |
| [**MENUEX**](menuex-resource.md)             | Define la apariencia y la función de un menú.                                                                                                                                  |
| [**MESSAGETABLE**](messagetable-resource.md) | Define una tabla de mensajes asignándole un nombre y especificando el nombre del archivo que la contiene. El archivo es un archivo de recursos binario generado por el compilador de mensajes.                |
| [**EMERGENTE**](popup-resource.md)               | Define un elemento de menú que puede contener elementos de menú y submenús.                                                                                                                   |
| **PLUGPLAY**                                  | Obsoleto.                                                                                                                                                                       |
| [**RCDATA**](rcdata-resource.md)             | Define los recursos de datos. Los recursos de datos permiten incluir datos binarios en el archivo ejecutable.                                                                                      |
| [**STRINGTABLE**](stringtable-resource.md)   | Define recursos de cadena. Los recursos de cadena son cadenas Unicode o ASCII que se pueden cargar desde el archivo ejecutable.                                                            |
| **TEXTINCLUDE**                               | Un recurso especial que se interpreta mediante Visual C++. Para obtener más información, vea [TN035](/cpp/mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp?view=vs-2019).                                        |
| **TYPELIB**                                   | Un recurso especial que se usa con las opciones del vinculador [/TLBID](/cpp/build/reference/tlbid-specify-resource-id-for-typelib?view=vs-2019) y [/tlbout](/cpp/build/reference/tlbout-name-dot-tlb-file?view=vs-2019) . |
| [**Definido por el usuario**](user-defined-resource.md) | Define un recurso que contiene datos específicos de la aplicación.                                                                                                                     |
| [**VERSIONINFO**](versioninfo-resource.md)   | Define un recurso de información de versión. Contiene información como el número de versión, el sistema operativo previsto, etc.                                                  |
| **VXD**                                       | Obsoleto.                                                                                                                                                                       |



 

Para obtener más información sobre los recursos predefinidos de MFC, vea [TN023](/cpp/mfc/tn023-standard-mfc-resources?view=vs-2019) y [TN024](/cpp/mfc/tn024-mfc-defined-messages-and-resources?view=vs-2019).

## <a name="controls"></a>Controles



| Control                                            | Descripción                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**AUTO3STATE**](auto3state-control.md)           | Crea un control de casilla de tres Estados automático.                         |
| [**Autocheckbox**](autocheckbox-control.md)       | Crea un control de casilla automática.                                     |
| [**Autoradiobutton**](autoradiobutton-control.md) | Crea un control de botón de radio automático.                                  |
| [**CASILLA**](checkbox-control.md)               | Crea un control de casilla.                                                |
| [**COMBOBOX**](combobox-control.md)               | Crea un control de cuadro combinado.                                                |
| [**CONTROL**](control-control.md)                 | Crea un control definido por la aplicación.                                     |
| [**CTEXT**](ctext-control.md)                     | Crea un control de texto centrado.                                            |
| [**DEFPUSHBUTTON**](defpushbutton-control.md)     | Crea un control de pulsador predeterminado.                                       |
| [**EDITTEXT**](edittext-control.md)               | Crea un control de edición.                                                    |
| [**GROUPBOX**](groupbox-control.md)               | Crea un control de cuadro de grupo.                                                |
| [**ICONO**](icon-control.md)                       | Crea un control de icono. Este control es un icono que se muestra en un cuadro de diálogo. |
| [**IDENTIFICACIÓN**](listbox-control.md)                 | Crea un control de cuadro de lista.                                                 |
| [**LTEXT**](ltext-control.md)                     | Crea un control de texto alineado a la izquierda.                                        |
| [**PUSHBOX**](pushbox-control.md)                 | Crea un control de cuadro de control.                                                 |
| [**BOTONES**](pushbutton-control.md)           | Crea un control de botón de control.                                              |
| [**ÍNDICES**](radiobutton-control.md)         | Crea un control de botón de radio.                                             |
| [**RTEXT**](rtext-control.md)                     | Crea un control alineado a la derecha.                                            |
| [**SCROLLBAR**](scrollbar-control.md)             | Crea un control de barra de desplazamiento.                                               |
| [**STATE3**](state3-control.md)                   | Crea un control de casilla de tres Estados.                                    |



 

## <a name="statements"></a>Instrucciones



| .                                            | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HAYAN**](caption-statement.md)                 | Establece el título de un cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**SUS**](characteristics-statement.md) | Especifica información sobre un recurso que puede ser utilizada por la herramienta que puede leer o escribir archivos de definición de recursos.                                                                                                                                                                                                                                                                                                                                                                           |
| [**LAS**](class-statement.md)                     | Establece la clase del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**EXSTYLE**](exstyle-statement.md)                 | Establece el estilo de ventana extendida del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**TIPO**](font-statement.md)                       | Establece la fuente con la que el sistema dibujará texto para el cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**MÓDULO**](language-statement.md)               | Establece el idioma de todos los recursos hasta la siguiente instrucción de [**lenguaje**](language-statement.md) o hasta el final del archivo. Cuando la instrucción del **lenguaje** aparece antes del principio del cuerpo de una definición de recursos [**Accelerators**](accelerators-resource.md), [**Dialog**](dialog-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**stringtable**](stringtable-resource.md) , el idioma especificado solo se aplica a ese recurso. |
| [**MENU**](menu-statement.md)                       | Establece el menú del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**OBJETOS**](menuitem-statement.md)               | Define un elemento de menú.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**APLICAR**](style-statement.md)                     | Establece el estilo de ventana para el cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**Versión**](version-statement.md)                 | Especifica la información de versión de un recurso que puede ser utilizada por la herramienta que puede leer o escribir archivos de definición de recursos.                                                                                                                                                                                                                                                                                                                                                                     |



 

 

 