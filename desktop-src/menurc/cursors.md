---
title: Cursores
description: En esta sección se de abordan cursores que son imágenes pequeñas cuya ubicación en la pantalla se controla mediante un dispositivo que apunta, como un mouse, un lápiz o un trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- resources,cursors
- cursores,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7be5b8e213dd1911d2227a3dce4b61078ab1a22711d4e765525c7fbd5bd08d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712615"
---
# <a name="cursors"></a>Cursores

Un cursor es una imagen pequeña cuya ubicación en la pantalla se controla mediante un dispositivo que apunta, como un mouse, un lápiz o un trackball. En el resto de esta información general, el término mouse hace referencia a cualquier dispositivo que apunta.

Cuando el usuario mueve el mouse, el sistema mueve el cursor en consecuencia. Las funciones de cursor permiten a las aplicaciones crear, cargar, mostrar, animar, mover, confinar y destruir cursores.

### <a name="in-this-section"></a>En esta sección



| Nombre                                     | Descripción                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [Acerca de los cursores](about-cursors.md)       | Describe los cursores estándar.<br/>                    |
| [Uso de cursores](using-cursors.md)       | Describe cómo realizar tareas relacionadas con cursores.<br/> |
| [Referencia de cursor](cursor-reference.md) | Contiene la referencia de API.<br/>                        |



 

### <a name="cursor-functions"></a>Funciones del cursor



| Nombre                                                 | Descripción                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Limita el cursor a un área rectangular de la pantalla. Si una posición de cursor posterior (establecida por la función [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) o el mouse) se encuentra fuera del rectángulo, el sistema ajusta automáticamente la posición para mantener el cursor dentro del área rectangular. <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Copia el cursor especificado. <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Crea un cursor con el tamaño, los patrones de bits y la zona de acceso directo especificados. <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Destruye un cursor y libera cualquier memoria ocupada por el cursor. No use esta función para destruir un cursor compartido.<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Recupera las coordenadas de pantalla del área rectangular a la que se limita el cursor. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Recupera un identificador del cursor actual. <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Recupera información sobre el cursor global.<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Recupera la posición del cursor, en coordenadas de pantalla.<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Recupera la posición del cursor en coordenadas físicas.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Carga el recurso de cursor especificado desde el archivo ejecutable (.EXE) asociado a una instancia de aplicación.<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Crea un cursor basado en los datos contenidos en un archivo. <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Establece la forma del cursor. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Mueve el cursor a las coordenadas de pantalla especificadas. Si las nuevas coordenadas no están dentro del rectángulo de pantalla establecido por la llamada de función [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) más reciente, el sistema ajusta automáticamente las coordenadas para que el cursor permanezca dentro del rectángulo. <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Establece la posición del cursor en coordenadas físicas.<br/>                                                                                                                                                                                                                                    |
| [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Permite que una aplicación personalice los cursores del sistema. Reemplaza el contenido del cursor del sistema especificado por el parámetro *id* por el contenido del cursor especificado por el *parámetro hcur* y, a continuación, destruye *hcur*. <br/>                                                          |
| [**ShowCursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Muestra u oculta el cursor. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Notificaciones de cursor



| Nombre                                  | Descripción                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**WM \_ SETCURSOR**](wm-setcursor.md) | Se envía a una ventana si el mouse hace que el cursor se mueva dentro de una ventana y no se captura la entrada del mouse. <br/> |



 

### <a name="cursor-structures"></a>Estructuras de cursor



| Nombre                             | Descripción                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Contiene información global del cursor.<br/> |



 

 

 





