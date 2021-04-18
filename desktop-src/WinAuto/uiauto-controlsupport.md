---
title: Compatibilidad de UI Automation con controles estándar
description: En este tema se identifican los controles estándar de Windows compatibles con la automatización de la interfaz de usuario de Microsoft. La compatibilidad completa solo se proporciona para los controles de la versión 6 de ComCtrl32.dll (disponibles con Windows XP y versiones posteriores).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- clientes, compatibilidad de UI Automation con controles estándar
- clientes, compatibilidad con controles estándar
- clientes, controles Win32
- Automatización de la interfaz de usuario, compatibilidad con controles estándar
- Automatización de la interfaz de usuario, compatibilidad con controles estándar
- Automatización de la interfaz de usuario, controles Win32
- compatibilidad con controles estándar
- compatibilidad con controles estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531918"
---
# <a name="ui-automation-support-for-standard-controls"></a>Compatibilidad de UI Automation con controles estándar

En este tema se identifican los controles estándar de Windows compatibles con la automatización de la interfaz de usuario de Microsoft. La compatibilidad completa solo se proporciona para los controles de la versión 6 de ComCtrl32.dll (disponibles con Windows XP y versiones posteriores).

> [!Note]  
> El control RichEdit solo se admite para las versiones incluidas con Windows Vista (en RichEd20.dll versión 3,1 y posteriores, y MsftEdit.dll versión 4,1 y posteriores).

 

En la tabla siguiente se enumeran los nombres de clase de los controles estándar admitidos, junto con los tipos de control de automatización de la interfaz de usuario correspondientes.



| Class Name (Nombre de clase)          | Tipo de control        |
|---------------------|---------------------|
| Button              | Button              |
| Button              | RadioButton         |
| Botón              | Grupo               |
| Botón              | CheckBox            |
| Botón              | Hyperlink           |
| Botón              | SplitButton         |
| Botón              | CheckBox            |
| ComboBoxEx32        | ComboBox            |
| ComboBox            | ComboBox            |
| Editar                | Documento            |
| Editar                | Editar                |
| SysLink             | Hyperlink           |
| estática              | Texto                |
| estática              | Imagen               |
| SysIPAddress32      | Personalizados              |
| SysHeader32         | Header/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | List                |
| ListBox             | List                |
| ListBox             | ListItem            |
| \#32768             | Menú                |
| \#32768             | MenuItem            |
| msctls \_ progress32  | ProgressBar         |
| RichEdit            | Documentar. Ver nota. |
| RichEdit20A         | Documento            |
| RichEdit20W         | Documento            |
| RichEdit50W         | Documento            |
| ScrollBar           | Control deslizante              |
| msctls \_ trackbar32  | Control deslizante              |
| msctls \_ updown32    | Spinner             |
| msctls \_ statusbar32 | StatusBar           |
| SysTabControl32     | Pestaña                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | Botón              |
| ToolbarWindow32     | CheckBox            |
| ToolbarWindow32     | RadioButton         |
| ToolbarWindow32     | Separador           |
| información sobre herramientas \_ Class32   | Información sobre herramientas             |
| \#32774             | Información sobre herramientas             |
| ReBarWindow32       | Barra de herramientas             |
| SysTreeView32       | Árbol                |
| SysTreeView32       | TreeItem            |



 

No se admiten los controles que se muestran en la tabla siguiente.



| Class Name (Nombre de clase)                                    | Tipo de control |
|-----------------------------------------------|--------------|
| SysAnimate32                                  | Imagen        |
| SysPager                                      | Spinner      |
| SysDateTimePick32                             | Personalizados       |
| SysMonthCal32                                 | Calendario     |
| MS \_ WINNOTE                                   | Información sobre herramientas      |
| VBBubble                                      | Información sobre herramientas      |
| ScrollBar (cuando se usa como control independiente) | Control deslizante       |
| SuperGrid                                     | Personalizados       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




