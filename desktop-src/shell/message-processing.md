---
description: La función de devolución de llamada CPlApplet procesa todos los mensajes enviados a un elemento del panel de control por Windows. Los mensajes enviados a la función se encuentran en un orden específico. Con el mismo token, el elemento. cpl requiere que los mensajes se procesen de una forma específica.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Procesamiento de mensajes del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8b43c6e265030279a6644547f41e3630208325
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002505"
---
# <a name="control-panel-message-processing"></a>Procesamiento de mensajes del panel de control

La función de devolución de llamada [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) procesa todos los mensajes enviados a un elemento del panel de control por Windows. Los mensajes enviados a la función se encuentran en un orden específico. Con el mismo token, el elemento. cpl requiere que los mensajes se procesen de una forma específica.

En primer lugar, la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe el \_ mensaje CPL init cuando Windows carga por primera vez el elemento del panel de control. La función debe llevar a cabo cualquier inicialización, como la asignación de memoria, y devolver un valor distinto de cero. Si **CPlApplet** no puede completar la inicialización, debe devolver cero, dirigirse a Windows para finalizar la comunicación y liberar el archivo dll.

Después, si el \_ mensaje CPL init se ejecutó correctamente, Windows envía el \_ mensaje CPL GETCOUNT. A continuación, la función debe devolver el número de elementos del panel de control que admite el archivo. dll.

A continuación, la función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe un \_ mensaje CPL de consulta y un \_ mensaje CPL NEWINQUIRE para cada elemento del panel de control que admite el archivo. dll. La función rellena una estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) con información sobre el elemento, como su nombre, icono y una cadena descriptiva. La mayoría de las aplicaciones deben procesar el \_ mensaje CPL consulta y omitir el \_ mensaje CPL NEWINQUIRE. El \_ mensaje CPL consulta proporciona información en un formulario que Windows puede almacenar en caché, lo que da como resultado un rendimiento mucho mejor. El \_ mensaje CPL NEWINQUIRE se usa solo si necesita cambiar el icono o las cadenas de visualización del elemento en función del estado del equipo. Los elementos del panel de control que usan CPL \_ NEWINQUIRE no se pueden encontrar en una búsqueda en el menú **Inicio** en Windows Vista porque se basa en el almacenamiento en caché.

La función [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) siguiente recibe un \_ mensaje CPL DBLCLK como notificación de que el usuario ha elegido el icono que representa el elemento del panel de control. La función podría recibir este mensaje varias veces. El mensaje incluye el identificador de elemento y el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) en la llamada a [**CPL \_ require**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). La función debe mostrar el cuadro de diálogo correspondiente y procesar la entrada de usuario subsiguiente.

Además de CPL \_ DBLCLK, el \_ mensaje CPL STARTWPARMS se puede enviar si se invoca un elemento del panel de control con parámetros de entrada, como desde un símbolo del sistema o desde otro programa. El mensaje incluye el identificador de elemento junto con la cadena de parámetro adicional.

Antes de que finalice la aplicación de control, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe el \_ mensaje CPL STOP una vez por cada elemento del panel de control admitido por el archivo. dll. El mensaje incluye el identificador del elemento del panel de control y el puntero **lpData** devuelto en la estructura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) o [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) en la llamada a [**CPL \_ require**](cpl-inquire.md) o [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). La función debe liberar cualquier memoria asignada para el cuadro de diálogo especificado.

Después del último CPL \_ Stop Message, [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recibe un \_ mensaje CPL EXIT. La función debe liberar toda la memoria asignada restante y anular el registro de cualquier clase de ventana privada que pueda haber registrado. Inmediatamente después de que la función vuelva de este mensaje, Windows libera el elemento del panel de control llamando a la función [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Usar CPLApplet](using-cplapplet.md)
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

 

 
