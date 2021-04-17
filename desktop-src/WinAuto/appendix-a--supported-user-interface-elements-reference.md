---
title: Apéndice A referencia de elementos de la interfaz de usuario admitidos
description: Este apéndice contiene información sobre los elementos de interfaz de usuario proporcionados por el sistema que expone Microsoft Active Accessibility en Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP y Windows 2000 Server.
ms.assetid: 5d0a81d8-5d36-4c33-bb8c-abcb8b00166e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f75cd4251ed7d75d9aa6a2d83387a51a8b157e9
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "105704887"
---
# <a name="appendix-a-supported-user-interface-elements-reference"></a>Apéndice A: referencia de elementos de la interfaz de usuario admitidos

Este apéndice contiene información sobre los elementos de interfaz de usuario proporcionados por el sistema que expone Microsoft Active Accessibility en Windows 95, Windows 98, Microsoft Windows NT, Windows 2000, Windows XP y Windows 2000 Server. Esta compatibilidad permite que las utilidades de cliente obtengan información sobre los elementos de interfaz de usuario proporcionados por el sistema en aplicaciones que no implementan Microsoft Active Accessibility.

Oleacc.dll admite controles que se definen en User32.dll, Comctl32.dll y elementos de la interfaz de usuario de Windows. En concreto, admite los siguientes tipos de elementos de interfaz de usuario (enumerados por nombre de clase de Windows).



| Nombre de clase de Windows                   | Tipo de elemento de la interfaz de usuario                                         | Actualizaciones de Windows Vista                                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ListBox                              | Cuadros de lista                                              | None                                                                                                                                                                                                                 |
| Botón                               | Botones de opción, botones de radio, botones de activación, cuadros de grupo | Los botones de expansión pueden tener cero o más elementos secundarios.                                                                                                                                                                        |
| estática                               | Etiquetas                                                  | None                                                                                                                                                                                                                 |
| Editar                                 | Cuadros de texto                                              | None                                                                                                                                                                                                                 |
| ComboBox                             | Cuadros combinados, listas desplegables                            | None                                                                                                                                                                                                                 |
| ScrollBar                            | Barras de desplazamiento                                             | [**Evento \_ de El objeto \_ CONTENTSCROLLED**](event-constants.md) es un nuevo evento para el control que tiene la funcionalidad de desplazamiento, pero no incluye una barra de desplazamiento estándar como parte del control. |
| \#32768                              | Menús de usuario                                              | None                                                                                                                                                                                                                 |
| \#32770                              | Cuadros de diálogo de usuario                                       | None                                                                                                                                                                                                                 |
| \#32771                              | Alt: ventana de ficha                                          | Solo está disponible en modo clásico.                                                                                                                                                                                      |
| msctls \_ statusbar32                  | Barras de estado                                             | None                                                                                                                                                                                                                 |
| msctls \_ progress32                   | Barras de progreso                                           | Las nuevas opciones de color de las barras de progreso no están expuestas por Microsoft Active Accessibility ni las propiedades de automatización de la interfaz de usuario de Microsoft.                                                                                         |
| msctls \_ hotkey32                     | Controles de tecla de acceso rápido                                        | None                                                                                                                                                                                                                 |
| msctls \_ trackbar32                   | Trackbars, controles deslizantes                                      | None                                                                                                                                                                                                                 |
| msctls \_ updown32                     | Controles de flechas o de número                                | None                                                                                                                                                                                                                 |
| SysAnimate32                         | Animation (control)                                       | None                                                                                                                                                                                                                 |
| SysTabControl32                      | Control Tab                                             | None                                                                                                                                                                                                                 |
| SysHeader32                          | Encabezados de vista de lista                                       | None                                                                                                                                                                                                                 |
| SysListView32                        | Controles de vista de lista                                      | None                                                                                                                                                                                                                 |
| SysTreeView32                        | Controles de vista de árbol                                      | None                                                                                                                                                                                                                 |
| SysDateTimePick32 (versiones 5 y 6) | Selector de fecha y hora                                 | La versión 6 de este control en Windows Vista tiene una implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa.                                                                                                           |
| SysIPAddress32                       | Controles de direcciones IP                                     | None                                                                                                                                                                                                                 |
| información sobre herramientas \_ Class32                    | Información sobre herramientas                                                | None                                                                                                                                                                                                                 |
| ToolbarWindow32                      | Barras de herramientas                                                | None                                                                                                                                                                                                                 |
| RICHEDIT, RichEdit20A, RichEdit20W   | Campos de texto                                             | None                                                                                                                                                                                                                 |
| SysMonthCal32 (versiones 5 y 6)     | Calendario mensual                                          | La versión 6 de este control en Windows Vista tiene una implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativa.                                                                                                           |



 

Aunque Microsoft Active Accessibility proporciona compatibilidad con los elementos de la interfaz de usuario proporcionados por el sistema en Microsoft Windows NT 4,0 con Service Pack 4, esta compatibilidad está limitada.

En este apéndice se enumeran las propiedades y los métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que Microsoft Active Accessibility admite para cada elemento de la interfaz de usuario. Si procede, la documentación también muestra el [WinEvents](winevents-infrastructure.md) que el elemento de la interfaz de usuario desencadena e incluye información adicional sobre las propiedades y los métodos admitidos. También incluye información sobre los roles de objeto y sus métodos y propiedades de **IAccessible** compatibles.

Estos detalles pueden ayudar a los desarrolladores de cliente a evitar que se realicen llamadas innecesarias a propiedades y métodos no compatibles. Esta información también permite que los desarrolladores del servidor sepan qué propiedades y métodos deben admitir sus controles personalizados y qué WinEvents deben desencadenar sus controles.

Utilice la información de este apéndice como guía. Le recomendamos encarecidamente que use las herramientas de Active Accessibility de Microsoft para comprobar el comportamiento esperado de los elementos de la interfaz de usuario o los roles de objeto.

Para obtener más información, vea los temas siguientes:

-   [Cómo expone Active Accessibility elementos de la interfaz de usuario](how-active-accessibility-exposes-user-interface-elements.md)
-   [Referencia de elementos de la interfaz de usuario](user-interface-element-reference.md)

 

 




