---
title: Funciones de alerta
description: Las funciones de alerta de administración de red notifican a las aplicaciones y programas de servicio de red los eventos de red.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fde863b27bebc8bf815c939f7edf96cd998442
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169374"
---
# <a name="alert-functions"></a>Funciones de alerta

\[Las funciones de alerta no se admiten a Windows Vista porque no se admiten los servicios de alerta y mensajería.\]

Las funciones de alerta de administración de red notifican a las aplicaciones y programas de servicio de red los eventos de red. Un *evento* es una instancia determinada de un proceso, repetición o estado de hardware definido por una aplicación. Las funciones de alerta permiten a las aplicaciones indicar cuándo se producen eventos predefinidos.

**Windows Server 2003:** Los servicios de alerta y mensajería están deshabilitados de forma predeterminada en Windows Server 2003. Debe volver a habilitar los servicios antes de llamar a las funciones de alerta de administración de red o a las funciones [de mensaje de administración de red](message-functions.md).

Las funciones de alerta se enumeran a continuación.



| Función                                   | Descripción                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica a todos los clientes registrados que se ha producido un evento determinado.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifica la notificación a los clientes registrados de que se ha producido un evento determinado, porque, a diferencia de **NetAlertRaise,** **NetAlertRaiseEx** no requiere una [**estructura DE \_ ALERTAS DE STD.**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) |



 

El servicio de alertas debe ejecutarse en el equipo cliente cuando se llama a la **función NetAlertRaise** o a la **función NetAlertRaiseEx.** Si el servicio no se está ejecutando, las funciones producirán un **error con ERROR FILE NOT \_ \_ \_ FOUND**. El servicio de alertas del cliente llama a la [**función NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) para enviar información a los destinatarios.

Las aplicaciones, los servicios de red y los componentes de red internos usan las funciones de alerta de administración de red para generar una alerta, lo que notifica a varias aplicaciones o usuarios cuando se produce un tipo determinado de evento. Las funciones de categoría de alertas, los tipos de datos, las estructuras y las constantes se definen en LMCONS. H, LMERR. H y LMALERT. Archivos de encabezado H. Para acceder a estas definiciones, defina las constantes INCL NETERRORS e INCL NETALERT e incluya el archivo de encabezado \_ \_ LM.H.

The LMALERT. El archivo H predefine las siguientes clases de alerta (tipos de eventos de red) para enviar alertas:

-   Eventos de red que requieren asistencia administrativa
-   Adición de una entrada a un archivo de registro de errores
-   Recepción de un mensaje de difusión por parte de un usuario o una aplicación
-   Finalización de un trabajo de impresión
-   Uso de determinadas aplicaciones o recursos por parte de los usuarios

Puede definir otras clases de alertas para aplicaciones de red según sea necesario. Por ejemplo, si una aplicación de un servidor escribe rutinariamente grandes cantidades de datos en una unidad de disco, la aplicación corre el riesgo de rellenar el disco. En este caso, es posible que desee agregar el evento "sin espacio libre en disco" para desencadenar una alerta que notifica a la aplicación que se detenga o finalice el proceso que está llenando el disco. El nombre del evento de una alerta puede ser cualquier cadena de texto.

Cuando se genera una alerta con una llamada a la función [**NetAlertRaise,**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) los datos del mensaje deben constar de una estructura de encabezado DE ALERTA DE [**\_ STD,**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) seguida de datos de longitud fija adicionales específicos de la alerta en una estructura ADMIN [**OTHER \_ \_ INFO,**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info) [**ERRLOG OTHER \_ \_ INFO,**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info) [**PRINT OTHER \_ \_ INFO**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)o [**USER OTHER \_ \_ INFO.**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) Los datos de longitud variable adicionales pueden seguir la estructura específica de la alerta. (Las llamadas a [**la función NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) no requieren una **estructura STD \_ ALERT).** La aplicación que realiza la llamada debe asignar la memoria para todas las estructuras y los datos de longitud variable, y liberar la memoria después de que se devuelva la llamada.

Las macros siguientes están disponibles para su uso con búferes de datos de alerta.



| Macro                                          | Descripción                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**ALERTAR \_ A OTRA \_ INFORMACIÓN**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Devuelve un puntero a los datos de longitud fija que siguen a la **estructura DE \_ ALERTAS DE STD** en un mensaje de alerta. |
| [**DATOS \_ DE VAR DE \_ ALERTA**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Devuelve un puntero a los datos de longitud variable que siguen a los datos específicos de la alerta en un mensaje de alerta.   |



 

En lugar de usar las funciones de alerta de administración de red, es posible que pueda usar el SDK Windows Management Instrumentation (WMI) para la notificación de eventos. Para obtener más información sobre las plataformas que admiten el modelo de eventos WMI, vea Eventos de infraestructura y [supervisión de](/windows/desktop/WmiSdk/monitoring-events) [WMI](/windows/desktop/WmiSdk/wmi-infrastructure) en la documentación de WMI.

 

 