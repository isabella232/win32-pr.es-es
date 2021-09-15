---
description: Antes de Windows Vista, creó un elemento Panel de control crear un archivo .dll y asignarle un nombre con una .cpl extensión.
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: Uso de CPLApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247935"
---
# <a name="using-cplapplet"></a>Uso de CPLApplet

Antes de Windows Vista, creó un elemento Panel de control crear un archivo .dll y asignarle un nombre con una .cpl extensión. Este archivo exportó la [**función CPlApplet.**](/windows/win32/api/cpl/nc-cpl-applet_proc) Este esquema todavía se admite en Windows Vista y versiones posteriores, y se describe en este tema. Sin embargo, las directrices para los nuevos elementos Panel de control recomiendan un enfoque más sencillo con el elemento Panel de control creado como un archivo .exe que usa un diseño de flujo de tareas.

Cuando Panel de control carga un archivo .dll (o .cpl), llama a la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) para obtener información como el número de elementos Panel de control que hospeda el archivo, así como información sobre cada elemento. Panel de control llama a la función cuando se inicializa, abre o cierra la ventana del elemento.

Cuando Windows carga primero el elemento Panel de control, recupera la dirección de la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) y, posteriormente, usa esa dirección para llamar a la función y pasarle mensajes. Podría enviar los mensajes siguientes.



| Message                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DBLCLK de CPL \_**](cpl-dblclk.md)           | Se envía para notificar [**a CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un elemento Panel de control especificado. **CPlApplet** debe mostrar el cuadro de diálogo del elemento especificado y realizar las tareas especificadas por el usuario. El parámetro *LParam1 de* **CPlApplet** es un entero que representa el índice de base cero del Panel de control elemento. El *parámetro lParam2* es el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) [**o NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) en el mensaje [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE.**](cpl-newinquire.md) Se omite el valor devuelto.                                                                |
| [**SALIDA \_ de CPL**](cpl-exit.md)               | Se envía después del último mensaje STOP de CPL e inmediatamente antes de Windows usa la función FreeLibrary para liberar el archivo DLL que contiene \_ el Panel de control elemento. [](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) [**CPlApplet debe**](/windows/win32/api/cpl/nc-cpl-applet_proc) liberar la memoria restante y prepararse para cerrarse. Se omite el valor devuelto.                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CPL \_ GETCOUNT**](cpl-getcount.md)       | Se envía después del mensaje INIT de CPL para solicitar a CPlApplet que devuelva un número que indique \_ cuántos subprogramas [](/windows/win32/api/cpl/nc-cpl-applet_proc) admite.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**INIT \_ de CPL**](cpl-init.md)               | Se envía inmediatamente después de cargar el archivo DLL que Panel de control elemento. El mensaje solicita a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que realice procedimientos de inicialización, incluida la asignación de memoria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CPL \_ INQUIRE**](cpl-inquire.md)         | Se envía después del mensaje GETCOUNT de CPL \_ para solicitar a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que proporcione información sobre un subprograma especificado. El *valor lParam1* es un entero que representa el índice de base cero del subprograma sobre qué información se solicita. El *parámetro lParam2* de **CPlApplet** apunta a una [**estructura CPLINFO.**](/windows/win32/api/cpl/ns-cpl-cplinfo) Se omite el valor devuelto.                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ NEWINQUIRE**](cpl-newinquire.md)   | Se envía después del mensaje GETCOUNT de CPL para solicitar \_ a [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que proporcione información sobre un elemento Panel de control especificado. El *valor lParam1* es un entero que representa el índice de base cero del subprograma sobre qué información se solicita. El *parámetro lParam2* es un puntero a una [**estructura NEWCPLINFO.**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) CPL \_ NEWINQUIRE normalmente debe omitirse. La aplicación solo debe procesar CPL INQUIRE en Windows 95, Microsoft Windows NT 4.0 y sistemas posteriores, ya que el rendimiento de Panel de control se resiente cuando se usa \_ CPL \_ NEWINQUIRE. Esto se debe a que las cadenas e iconos devueltos no se pueden almacenar en caché. Se omite el valor devuelto. |
| [**CPL \_ SELECT**](cpl-select.md)           | Obsoleto. Las versiones actuales Windows no envían este mensaje.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ STARTWPARMS**](cpl-startwparms.md) | Se envía para notificar [**a CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que el usuario ha elegido el icono asociado a un cuadro de diálogo determinado. **CPlApplet** debe mostrar el cuadro de diálogo correspondiente y llevar a cabo las tareas especificadas por el usuario. Este mensaje es similar a \_ DBLCLK de CPL, pero puede haber alguna información adicional. El *parámetro lParam1* es Panel de control número de elemento y *lParam2* es **un LPCTSTR** para cualquier dirección adicional que pueda ser necesaria. Devuelve **TRUE** si se controla este mensaje; de lo contrario, **FALSE**. Este mensaje es válido para [la versión 5.00](versions.md) y posteriores de Shell32.dll.                                                                                         |
| [**CPL \_ STOP**](cpl-stop.md)               | Se envía una vez por Panel de control elemento del archivo .cpl antes de Windows descarga la Panel de control extensión. [**CPlApplet debe**](/windows/win32/api/cpl/nc-cpl-applet_proc) liberar cualquier memoria asociada al número de elemento proporcionado *en lParam1.* El *parámetro lParam2* es el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) en el mensaje [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE.**](cpl-newinquire.md) Se omite el valor devuelto.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Panel de control de mensajes](message-processing.md)
</dt> <dt>

[Ejecución de Panel de control elementos](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos de Panel de control sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignación de Panel de control categorías](assigning-control-panel-categories.md)
</dt> <dt>

[Crear vínculos de tareas que se pueden buscar para un elemento Panel de control búsqueda](creating-searchable-task-links.md)
</dt> <dt>

[Acceso al Panel de control en modo Caja fuerte en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
