---
description: En este tema se describen los tipos de clases de ventana, cómo las localiza el sistema y los elementos que definen el comportamiento predeterminado de las ventanas que pertenecen a ellas.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Clases de ventana (ventanas y mensajes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da95fc54a9527bade0d925c1f993cf853b0ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716781"
---
# <a name="window-classes-windows-and-messages"></a>Clases de ventana (ventanas y mensajes)

En este tema se describen los tipos de clases de ventana, cómo las localiza el sistema y los elementos que definen el comportamiento predeterminado de las ventanas que pertenecen a ellas.

Una clase de ventana es un conjunto de atributos que el sistema utiliza como plantilla para crear una ventana. Cada ventana es un miembro de una clase de ventana. Todas las clases de ventana son específicas del proceso.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                 | Descripción                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de las clases de ventana](about-window-classes.md)     | Describe las clases de ventana. Cada clase de ventana tiene un procedimiento de ventana asociado compartido por todas las ventanas de la misma clase. El procedimiento de ventana procesa los mensajes de todas las ventanas de esa clase y, por tanto, controla su comportamiento y apariencia.<br/> |
| [Usar clases de ventana](using-window-classes.md)     | Muestra cómo registrar una ventana local y utilizarla para crear una ventana principal.<br/>                                                                                                                                                                     |
| [Referencia de clase de ventana](window-class-reference.md) | Contiene la referencia de la API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Funciones de clase de ventana



| Nombre                                         | Descripción                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Recupera información sobre una clase de ventana, incluido un identificador del icono pequeño asociado a la clase de ventana. La función [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) no recupera un identificador para el icono pequeño.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Recupera el valor de 32 bits (**Long**) especificado de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) asociada a la ventana especificada. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Recupera el valor especificado de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) asociada a la ventana especificada.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Recupera el nombre de la clase a la que pertenece la ventana especificada. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Recupera información sobre la ventana especificada. La función también recupera el valor de 32 bits (**Long**) en el desplazamiento especificado en la memoria de ventana adicional.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Recupera información sobre la ventana especificada. La función también recupera el valor en un desplazamiento especificado en la memoria de ventana adicional.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registra una clase de ventana para su uso posterior en las llamadas a la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registra una clase de ventana para su uso posterior en las llamadas a la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Reemplaza el valor especificado en el desplazamiento especificado en la memoria de clase adicional o la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) para la clase a la que pertenece la ventana especificada.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Reemplaza el valor de 16 bits (**Word**) en el desplazamiento especificado en la memoria de clase adicional para la clase de ventana a la que pertenece la ventana especificada.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Cambia un atributo de la ventana especificada. La función también establece el valor de 32 bits (Long) en el desplazamiento especificado en la memoria de ventana adicional.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Cambia un atributo de la ventana especificada. La función también establece un valor en el desplazamiento especificado en la memoria de ventana adicional.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Anula el registro de una clase de ventana, liberando la memoria necesaria para la clase. <br/>                                                                                                                                            |



 

Las siguientes funciones están obsoletas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></td>
<td>Recupera información sobre una clase de ventana. <br/>
<blockquote>
[!Note]<br />
La función <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> ha reemplazado a la función <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a> . Sin embargo, puede seguir usando <strong>GetClassInfo</strong>si no necesita información sobre el icono de clase pequeña.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></td>
<td>Recupera el valor de 16 bits (<strong>Word</strong>) en el desplazamiento especificado en la memoria de clase adicional para la clase de ventana a la que pertenece la ventana especificada.
<blockquote>
[!Note]<br />
Esta función está en desuso para cualquier otro uso que no sea <em>NINDEX</em> establecido en GCW_ATOM. La función se proporciona solo para la compatibilidad con las versiones de 16 bits de Windows. Las aplicaciones deben usar la función <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></td>
<td>Reemplaza el valor de 32 bits (<strong>Long</strong>) especificado en el desplazamiento especificado en la memoria de clase adicional o la estructura <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> para la clase a la que pertenece la ventana especificada.
<blockquote>
[!Note]<br />
Esta función se ha sustituido por la función <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> . Para escribir código que sea compatible con las versiones de Windows de 32 y 64 bits, use <strong>SetClassLongPtr</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a>Estructuras de clase de ventana



| Nombre                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contiene los atributos de clase de ventana registrados por la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . <br/> Esta estructura se ha sustituido por la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) utilizada con la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Puede seguir usando [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) y [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) si no necesita establecer el icono pequeño asociado a la clase de ventana.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contiene información de la clase de ventana. Se usa con las funciones [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) y [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  . <br/> La estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) es similar a la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Hay dos diferencias. **WNDCLASSEX** incluye el miembro **cbSize** , que especifica el tamaño de la estructura y el miembro **hIconSm** , que contiene un identificador de un icono pequeño asociado a la clase Window.<br/> |



 

 

 
