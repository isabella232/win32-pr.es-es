---
description: Los objetos de interfaz de usuario solo admiten un identificador por objeto. Los procesos no pueden heredar ni duplicar identificadores a objetos de usuario. Los procesos de una sesión no pueden hacer referencia a un identificador de usuario en otra sesión.
ms.assetid: 07edc049-26d9-4f42-a5e7-e1f4c8435a6c
title: Objetos de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c3cdb5c0927a5773bad818064442f654159fefba2b2dfa4d0cb4c08d17ff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884335"
---
# <a name="user-objects"></a>Objetos de usuario

Los objetos de interfaz de usuario solo admiten un identificador por objeto. Los procesos no pueden heredar ni duplicar identificadores a objetos de usuario. Los procesos de una sesión no pueden hacer referencia a un identificador de usuario en otra sesión.

Hay un límite teórico de 65 536 identificadores de usuario por sesión. Sin embargo, el número máximo de identificadores de usuario que se pueden abrir por sesión suele ser menor, ya que se ve afectado por la memoria disponible. También hay un límite predeterminado por proceso de identificadores de usuario. Para cambiar este límite, establezca el siguiente valor del Registro:

**HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** Windows \\ **NT** \\ **CurrentVersion** \\ **Windows** \\ **USERProcessHandleQuota**

Este valor se puede establecer en un número entre 200 y 18 000.

## <a name="handles-to-user-objects"></a>Identificadores de objetos de usuario

Los identificadores de los objetos de usuario son públicos para todos los procesos. Es decir, cualquier proceso puede usar el identificador de objeto de usuario, siempre que el proceso tenga acceso de seguridad al objeto.

En la ilustración siguiente, una aplicación crea un objeto de ventana. La [**función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) crea el objeto de ventana y devuelve un identificador de objeto.

![aplicación que crea un objeto de ventana](images/cshob-01.png)

Una vez creado el objeto de ventana, la aplicación puede usar el identificador de ventana para mostrar o cambiar la ventana. El identificador sigue siendo válido hasta que se destruye el objeto de ventana.

En la siguiente ilustración, la aplicación destruye el objeto de ventana. La [**función DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) quita el objeto de ventana de la memoria, lo que invalida el identificador de ventana.

![destruir un objeto de ventana](images/cshob-02.png)

## <a name="managing-user-objects"></a>Administración de objetos de usuario

En la tabla siguiente se enumeran los objetos de usuario, junto con las funciones creador y destructor de cada objeto. Las funciones del creador crean el objeto y un identificador de objeto o simplemente devuelven el identificador de objeto existente. Las funciones destructoras quitan el objeto de la memoria, lo que invalida el identificador del objeto.



| Objeto de usuario       | Función Creator                                                                                                                                                                                                                                                              | Función Destroyer                                                                                   |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Tabla de aceleradores | [**CreateAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-createacceleratortablea)                                                                                                                                                                                                               | [**DestroyAcceleratorTable**](/windows/win32/api/winuser/nf-winuser-destroyacceleratortable)                                    |
| Símbolo de intercalación             | [**CreateCaret**](/windows/win32/api/winuser/nf-winuser-createcaret)                                                                                                                                                                                                                                     | [**DestroyCaret**](/windows/win32/api/winuser/nf-winuser-destroycaret)                                                          |
| Cursor            | [**CreateCursor,**](/windows/win32/api/winuser/nf-winuser-createcursor) [**LoadCursor,**](/windows/win32/api/winuser/nf-winuser-loadcursora) [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                                   | [**DestroyCursor**](/windows/win32/api/winuser/nf-winuser-destroycursor)                                                        |
| Conversación de DDE  | [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect), [ **DdeConnectList**](/windows/win32/api/ddeml/nf-ddeml-ddeconnectlist)                                                                                                                                                                                      | [**DdeDisconnect**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnect), [ **DdeDisconnectList**](/windows/win32/api/ddeml/nf-ddeml-ddedisconnectlist) |
| Enlace              | [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)                                                                                                                                                                                                                           | [**UnhookWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-unhookwindowshookex)                                            |
| Icono              | [**CreateIconIndirect,**](/windows/win32/api/winuser/nf-winuser-createiconindirect) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)                                                                                                                                           | [**Destroyicon**](/windows/win32/api/winuser/nf-winuser-destroyicon)                                                            |
| Menú              | [**CreateMenu,**](/windows/win32/api/winuser/nf-winuser-createmenu) [**CreatePopupMenu,**](/windows/win32/api/winuser/nf-winuser-createpopupmenu) [**LoadMenu,**](/windows/win32/api/winuser/nf-winuser-loadmenua) [**LoadMenuIndirect**](/windows/win32/api/winuser/nf-winuser-loadmenuindirecta)                                                                                          | [**DestroyMenu**](/windows/win32/api/winuser/nf-winuser-destroymenu)                                                            |
| Periodo            | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**CreateDialogParam,**](/windows/win32/api/winuser/nf-winuser-createdialogparama) [**CreateDialogIndirectParam**](/windows/win32/api/winuser/nf-winuser-createdialogindirectparama), [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) | [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)                                                        |
| Posición de la ventana   | [**BeginDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-begindeferwindowpos)                                                                                                                                                                                                                     | [**EndDeferWindowPos**](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)                                                |



 

 

 
