---
description: Antes de Windows Vista, se creaba un elemento del panel de control creando un archivo. dll y asignándole un nombre con una extensión. cpl.
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: Usar CPLApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985399"
---
# <a name="using-cplapplet"></a>Usar CPLApplet

Antes de Windows Vista, se creaba un elemento del panel de control creando un archivo. dll y asignándole un nombre con una extensión. cpl. Este archivo exportó la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) . Este esquema sigue siendo compatible con Windows Vista y versiones posteriores, y se describe en este tema. Sin embargo, las instrucciones para los nuevos elementos del panel de control recomiendan un enfoque más sencillo con el elemento del panel de control compilado como un archivo. exe que usa un diseño de flujo de tareas.

Cuando el panel de control carga un archivo. dll (o. cpl), llama a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) para obtener información como el número de elementos del panel de control que hospeda el archivo, así como información sobre cada elemento. El panel de control también llama a la función cuando la ventana del elemento se inicializa, se abre o se cierra.

Cuando Windows carga por primera vez el elemento del panel de control, recupera la dirección de la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) y, posteriormente, usa esa dirección para llamar a la función y pasar mensajes. Podría enviar los mensajes siguientes.



| Message                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPL \_ DBLCLK**](cpl-dblclk.md)           | Se envía para notificar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un determinado elemento del panel de control. **CPlApplet** debe mostrar el cuadro de diálogo para el elemento especificado y realizar las tareas especificadas por el usuario. El parámetro **CPlApplet** *lParam1* es un entero que representa el índice de base cero del elemento del panel de control. El parámetro *lParam2* es el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) del mensaje [**CPL \_ inquire**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) . Se omite el valor devuelto.                                                                |
| [**salir de CPL \_**](cpl-exit.md)               | Se envía después del último bloque de detención de CPL \_ e inmediatamente antes de que Windows use la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar el archivo DLL que contiene el elemento del panel de control. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) debe liberar cualquier memoria restante y prepararse para cerrar. Se omite el valor devuelto.                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CPL \_ GETCOUNT**](cpl-getcount.md)       | Se envía después del \_ mensaje CPL init para solicitar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que devuelva un número que indica el número de subprogramas que admite.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**CPL \_ init**](cpl-init.md)               | Se envía inmediatamente después de que se cargue el archivo DLL que contiene el elemento del panel de control. El mensaje solicita a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que realice los procedimientos de inicialización, incluida la asignación de memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CPL \_ consulta**](cpl-inquire.md)         | Se envía después del \_ mensaje CPL GETCOUNT para solicitar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que proporcione información sobre un subprograma especificado. El valor de *lParam1* es un entero que representa el índice de base cero del subprograma sobre el que se solicita información. El parámetro *lParam2* de **CPlApplet** apunta a una estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . Se omite el valor devuelto.                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ NEWINQUIRE**](cpl-newinquire.md)   | Se envía después del \_ mensaje CPL GETCOUNT para solicitar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que proporcione información sobre un elemento del panel de control especificado. El valor de *lParam1* es un entero que representa el índice de base cero del subprograma sobre el que se solicita información. El parámetro *lParam2* es un puntero a una estructura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . \_Se debe omitir CPL NEWINQUIRE normalmente. La aplicación solo debe procesar \_ los sistemas de CPL en windows 95, Microsoft Windows NT 4,0 y versiones posteriores, ya que el rendimiento del panel de control se ve afectado cuando \_ se usa CPL NEWINQUIRE. Esto se debe a que las cadenas e iconos devueltos no se pueden almacenar en caché. Se omite el valor devuelto. |
| [**CPL \_ Select**](cpl-select.md)           | Obsoleto. Las versiones actuales de Windows no envían este mensaje.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ STARTWPARMS**](cpl-startwparms.md) | Se envía para notificar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. **CPlApplet** debe mostrar el cuadro de diálogo correspondiente y realizar las tareas especificadas por el usuario. Este mensaje es similar a CPL \_ DBLCLK, pero puede haber información adicional. El parámetro *lParam1* es el número de elemento del panel de control y *LParam2* es un **LPCTSTR** a cualquier dirección adicional que pueda ser necesaria. Devuelve **true** si este mensaje está controlado; en caso contrario, **false**. Este mensaje es válido para la [versión 5,00](versions.md) y versiones posteriores de Shell32.dll.                                                                                         |
| [**CPL \_ Stop**](cpl-stop.md)               | Se envía una vez por cada elemento del panel de control del archivo. cpl antes de que Windows Descargue la extensión del panel de control. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) debe liberar cualquier memoria asociada al número de elemento proporcionado en *lParam1*. El parámetro *lParam2* es el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) del mensaje [**CPL \_ inquire**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) . Se omite el valor devuelto.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Procesamiento de mensajes del panel de control](message-processing.md)
</dt> <dt>

[Ejecutar elementos del panel de control](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos del panel de control del sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignar categorías del panel de control](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tarea que se pueden buscar para un elemento del panel de control](creating-searchable-task-links.md)
</dt> <dt>

[Acceder al panel de control en modo seguro en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
