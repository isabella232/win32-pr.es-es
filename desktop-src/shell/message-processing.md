---
description: La función de devolución de llamada CPlApplet procesa todos los mensajes enviados a un elemento Panel de control por Windows. Los mensajes enviados a la función están en un orden específico. Con el mismo token, el .cpl requiere que los mensajes se procese de una manera específica.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Panel de control de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b43c6e265030279a6644547f41e3630208325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256970"
---
# <a name="control-panel-message-processing"></a>Panel de control de mensajes

La [**función de devolución de llamada CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa todos los mensajes enviados a un Panel de control por Windows. Los mensajes enviados a la función están en un orden específico. Con el mismo token, el .cpl requiere que los mensajes se procese de una manera específica.

En primer lugar, [**la función CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe el mensaje INIT de CPL \_ Windows carga primero el Panel de control elemento. La función debe llevar a cabo cualquier inicialización, como asignar memoria, y devolver un valor distinto de cero. Si **CPlApplet** no puede completar la inicialización, debe devolver cero, lo que Windows para finalizar la comunicación y liberar el archivo DLL.

A continuación, si el mensaje INIT de CPL se ha Windows \_ el mensaje \_ GETCOUNT de CPL. A continuación, la función debe devolver el número de Panel de control admitidos por el .dll archivo.

A continuación, la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe un mensaje CPL INQUIRE y un mensaje \_ CPL NEWINQUIRE para cada elemento Panel de control compatible con el .dll \_ archivo. La función rellena una estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) con información sobre el elemento, como su nombre, icono y una cadena descriptiva. La mayoría de las aplicaciones deben procesar el mensaje \_ CPL INQUIRE e ignorar el mensaje \_ NEWINQUIRE de CPL. El mensaje CPL INQUIRE proporciona información de forma que Windows almacenar en caché, lo que da como resultado \_ un rendimiento mucho mejor. El mensaje NEWINQUIRE de CPL solo se usa si necesita cambiar el icono del elemento o mostrar cadenas en función del \_ estado del equipo. Panel de control elementos que usan CPL NEWINQUIRE no se pueden encontrar mediante una búsqueda de menú Inicio en Windows Vista porque se basa en el almacenamiento \_ en caché. 

A continuación, la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe un mensaje DBLCLK de CPL como una notificación en la que se indica que el usuario ha elegido el icono que representa Panel de control \_ elemento. La función puede recibir este mensaje varias veces. El mensaje incluye el identificador de elemento y el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) [**o NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) en la llamada a [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). La función debe mostrar el cuadro de diálogo correspondiente y procesar la entrada posterior del usuario.

Además de DBLCLK de CPL, se puede enviar el mensaje \_ STARTWPARMS de CPL si se invoca un elemento de Panel de control con parámetros de entrada, como desde un símbolo del sistema o desde otro \_ programa. El mensaje incluye el identificador de elemento junto con la cadena de parámetro adicional.

Antes de que finalice la aplicación de control, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe el mensaje CPL STOP una vez por cada elemento Panel de control compatible con \_ el .dll archivo. El mensaje incluye el identificador del elemento Panel de control y el puntero **lpData** devuelto en la [**estructura CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) [**o NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) en la llamada a [**CPL \_ INQUIRE**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE.**](cpl-newinquire.md) La función debe liberar cualquier memoria que haya asignado para el cuadro de diálogo especificado.

Después del último mensaje STOP \_ de CPL, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe un mensaje EXIT de CPL. \_ La función debe liberar toda la memoria asignada restante y anular el registro de las clases de ventana privadas que pueda haber registrado. Inmediatamente después de que la función vuelva de este mensaje, Windows libera el Panel de control mediante una llamada a [**la función FreeLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Uso de CPLApplet](using-cplapplet.md)
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

 

 
