---
title: Apéndice A Referencia de elementos Interfaz de usuario admitidos
description: Este apéndice contiene información sobre los elementos de interfaz de usuario proporcionados por el sistema expuestos por Microsoft Active Accessibility en Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP y Windows 2000 Server.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f75cd4251ed7d75d9aa6a2d83387a51a8b157e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070715"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Apéndice A: Referencia de elementos Interfaz de usuario admitidos

Este apéndice contiene información sobre los elementos de interfaz de usuario proporcionados por el sistema expuestos por Microsoft Active Accessibility en Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP y Windows 2000 Server. Esta compatibilidad permite a las utilidades de cliente obtener información sobre los elementos de interfaz de usuario proporcionados por el sistema en aplicaciones que no implementan Microsoft Active Accessibility.

Oleacc.dll admite controles que se definen en los elementos User32.dll, Comctl32.dll y Windows interfaz de usuario. En concreto, admite los siguientes tipos de elementos de interfaz de usuario (enumerados Windows nombre de clase).



| Windows de clase                   | Tipo de elemento de interfaz de usuario                                         | Windows Actualizaciones de Vista                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Cuadros de lista                                              | None                                                                                                                                                                                                                 |
| Botón                               | Botones de inserción, botones de radio, botones de verificación, cuadros de grupo | Los botones de división pueden tener cero o más secundarios.                                                                                                                                                                        |
| estática                               | Etiquetas                                                  | None                                                                                                                                                                                                                 |
| Editar                                 | Cuadros de texto                                              | None                                                                                                                                                                                                                 |
| ComboBox                             | Cuadros combinados, listas desplegables                            | None                                                                                                                                                                                                                 |
| ScrollBar                            | Barras de desplazamiento                                             | [**EVENT \_ OBJECT \_ CONTENTSCROLLED es**](event-constants.md) un nuevo evento para el control que tiene funcionalidad de desplazamiento pero no incluye una barra de desplazamiento estándar como parte del control. |
| \#32768                              | Menús USER                                              | None                                                                                                                                                                                                                 |
| \#32770                              | Cuadros de diálogo USER                                       | None                                                                                                                                                                                                                 |
| \#32771                              | Ventana de la pestaña Alt                                          | Solo está disponible en modo clásico.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Barras de estado                                             | None                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Barras de progreso                                           | Las nuevas opciones de color para las barras de progreso no se exponen mediante Microsoft Active Accessibility o microsoft Automatización de la interfaz de usuario propiedades.                                                                                         |
| msctls \_ hotkey32                     | Controles de tecla de acceso                                        | None                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Barras de seguimiento, controles deslizantes                                      | None                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Controles de flechas o giros                                | None                                                                                                                                                                                                                 |
| SysAnimate32                         | Animation (control)                                       | None                                                                                                                                                                                                                 |
| SysTabControl32                      | Control Tab                                             | None                                                                                                                                                                                                                 |
| SysHeader32                          | Lista de encabezados de vista                                       | None                                                                                                                                                                                                                 |
| SysListView32                        | Controles de vista de lista                                      | None                                                                                                                                                                                                                 |
| SysTreeView32                        | Controles de vista de árbol                                      | None                                                                                                                                                                                                                 |
| SysDateTimePick32 (versiones 5 y 6) | Selector de fecha y hora                                 | La versión 6 de este control en Windows Vista tiene una implementación [**nativa de IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                                                                                                           |
| SysIPAddress32                       | Controles de dirección IP                                     | None                                                                                                                                                                                                                 |
| tooltips \_ class32                    | Tooltips                                                | None                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Barras de herramientas                                                | None                                                                                                                                                                                                                 |
| RICHEDIT, RichEdit20A, RichEdit20W   | Campos de texto                                             | None                                                                                                                                                                                                                 |
| SysMonthCal32 (versiones 5 y 6)     | Calendario mensual                                          | La versión 6 de este control en Windows Vista tiene una implementación [**nativa de IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                                                                                                           |



 

Aunque Microsoft Active Accessibility en Microsoft Windows NT 4.0 con Service Pack 4 proporciona cierta compatibilidad con elementos de interfaz de usuario proporcionados por el sistema, esta compatibilidad es limitada.

En este apéndice se enumeran las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que Microsoft Active Accessibility para cada elemento de la interfaz de usuario. Si procede, en la documentación también se enumeran [los eventos WinEvent que](winevents-infrastructure.md) desencadena el elemento de interfaz de usuario e incluye información adicional sobre las propiedades y los métodos admitidos. También incluye información sobre los roles de objeto y sus métodos **y propiedades IAccessible** admitidos.

Estos detalles pueden ayudar a los desarrolladores de clientes a evitar realizar llamadas innecesarias a métodos y propiedades no admitidos. Esta información también permite a los desarrolladores de servidores saber qué propiedades y métodos deben admitir sus controles personalizados y qué WinEvents deben desencadenar sus controles.

Use la información de este apéndice como guía. Se recomienda encarecidamente usar las herramientas de Microsoft Active Accessibility para comprobar el comportamiento esperado de los elementos de la interfaz de usuario o los roles de objeto.

Para obtener más información, vea los temas siguientes:

-   [Cómo Active Accessibility expone Interfaz de usuario elementos](how-active-accessibility-exposes-user-interface-elements.md)
-   [Interfaz de usuario de elementos](user-interface-element-reference.md)

 

 




