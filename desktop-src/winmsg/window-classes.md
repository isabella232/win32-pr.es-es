---
description: En este tema se describen los tipos de clases de ventana, cómo los localiza el sistema y los elementos que definen el comportamiento predeterminado de las ventanas que pertenecen a ellas.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Clases de ventana (Windows y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77e96a06433bf6bbcb72fb76a41a29fccee27ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482651"
---
# <a name="window-classes-windows-and-messages"></a>Clases de ventana (Windows y mensajes)

En este tema se describen los tipos de clases de ventana, cómo los localiza el sistema y los elementos que definen el comportamiento predeterminado de las ventanas que pertenecen a ellas.

Una clase de ventana es un conjunto de atributos que el sistema usa como plantilla para crear una ventana. Cada ventana es miembro de una clase de ventana. Todas las clases de ventana son específicas del proceso.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                 | Descripción                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de las clases de ventana](about-window-classes.md)     | Describe las clases de ventana. Cada clase de ventana tiene un procedimiento de ventana asociado compartido por todas las ventanas de la misma clase. El procedimiento de ventana procesa mensajes para todas las ventanas de esa clase y, por tanto, controla su comportamiento y apariencia.<br/> |
| [Usar clases de ventana](using-window-classes.md)     | Muestra cómo registrar una ventana local y usarla para crear una ventana principal.<br/>                                                                                                                                                                     |
| [Referencia de la clase Window](window-class-reference.md) | Contiene la referencia de API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Funciones de la clase Window



| Nombre                                         | Descripción                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Recupera información sobre una clase de ventana, incluido un identificador para el icono pequeño asociado a la clase de ventana. La [**función GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) no recupera un identificador en el icono pequeño.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Recupera el valor de 32 bits **(long)** especificado de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) asociada a la ventana especificada. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Recupera el valor especificado de la [**estructura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) asociada a la ventana especificada.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Recupera el nombre de la clase a la que pertenece la ventana especificada. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Recupera información sobre la ventana especificada. La función también recupera el valor de 32 bits **(long**) en el desplazamiento especificado en la memoria adicional de la ventana.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Recupera información sobre la ventana especificada. La función también recupera el valor en un desplazamiento especificado en la memoria adicional de la ventana.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registra una clase de ventana para su uso posterior en las llamadas a la [**función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registra una clase de ventana para su uso posterior en las llamadas a la [**función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Reemplaza el valor especificado en el desplazamiento especificado en la memoria de clase adicional o la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) de la clase a la que pertenece la ventana especificada.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Reemplaza el valor de 16 bits (**WORD**) en el desplazamiento especificado en la memoria de clase adicional para la clase de ventana a la que pertenece la ventana especificada.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Cambia un atributo de la ventana especificada. La función también establece el valor de 32 bits (long) en el desplazamiento especificado en la memoria adicional de la ventana.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Cambia un atributo de la ventana especificada. La función también establece un valor en el desplazamiento especificado en la memoria adicional de la ventana.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Anula el registro de una clase de ventana, liberando la memoria necesaria para la clase. <br/>                                                                                                                                            |



 

Las siguientes funciones están obsoletas.




| Nombre | Descripción | 
|------|-------------|
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> | Recupera información sobre una clase de ventana. <br /><blockquote>[!Note]<br />La <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>función GetClassInfo</strong></a> ha reemplazado a la <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>función GetClassInfoEx.</strong></a> Sin embargo, puede <strong>seguir utilizando GetClassInfo</strong>si no necesita información sobre el icono pequeño de clase.</blockquote><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a> | Recupera el valor de 16 bits<strong>(WORD</strong>) en el desplazamiento especificado en la memoria de clase adicional de la clase de ventana a la que pertenece la ventana especificada.<blockquote>[!Note]<br />Esta función está en desuso para cualquier uso distinto de <em>nIndex</em> establecido en GCW_ATOM. La función solo se proporciona por compatibilidad con versiones de 16 bits de Windows. Las aplicaciones deben usar <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>la función GetClassLong.</strong></a></blockquote><br /><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a> | Reemplaza el valor de 32 bits<strong>(long)</strong>especificado en el desplazamiento especificado en la memoria de clase adicional o la estructura <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> de la clase a la que pertenece la ventana especificada.<blockquote>[!Note]<br />Esta función se ha reemplazado por la <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>función SetClassLongPtr.</strong></a> Para escribir código compatible con las versiones de 32 y 64 bits de Windows, use <strong>SetClassLongPtr</strong>.</blockquote><br /><br /> | 




 

### <a name="window-class-structures"></a>Estructuras de clase de ventana



| Nombre                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contiene los atributos de clase de ventana registrados por la [**función RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) <br/> Esta estructura se ha reemplazado por la [**estructura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) usada con la [**función RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Todavía puede usar [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) y [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) si no necesita establecer el icono pequeño asociado a la clase de ventana.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contiene información de clase de ventana. Se usa con las [**funciones RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) [**y GetClassInfoEx.**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) <br/> La [**estructura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) es similar a la [**estructura WNDCLASS.**](/windows/win32/api/winuser/ns-winuser-wndclassa) Hay dos diferencias. **WNDCLASSEX incluye** el **miembro cbSize,** que especifica el tamaño de la estructura, y el **miembro hIconSm,** que contiene un identificador para un icono pequeño asociado a la clase de ventana.<br/> |



 

 

 
