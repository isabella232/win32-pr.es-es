---
title: Funciones de alerta
description: Las funciones de alerta de administración de red notifican a los programas de servicio de red y a las aplicaciones de eventos de red.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fde863b27bebc8bf815c939f7edf96cd998442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487942"
---
# <a name="alert-functions"></a>Funciones de alerta

\[No se admiten las funciones de alerta en Windows Vista porque no se admiten los servicios de alerta y mensajería.\]

Las funciones de alerta de administración de red notifican a los programas de servicio de red y a las aplicaciones de eventos de red. Un *evento* es una instancia concreta de un proceso, una aparición o un estado de hardware, tal como se define en una aplicación. Las funciones de alerta permiten a las aplicaciones indicar cuándo se producen eventos predefinidos.

**Windows Server 2003:** Los servicios de alerta y mensajería están deshabilitados de forma predeterminada en Windows Server 2003. Debe volver a habilitar los servicios antes de llamar a las funciones de alerta de administración de redes o a las [funciones de mensajes](message-functions.md)de administración de redes.

A continuación se enumeran las funciones de alerta.



| Función                                   | Descripción                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica a todos los clientes registrados que se ha producido un evento determinado.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifica la notificación a los clientes registrados de que se ha producido un evento determinado, porque, a diferencia de **NetAlertRaise**, **NetAlertRaiseEx** no requiere una estructura de [**\_ alerta STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

El servicio de alerta debe ejecutarse en el equipo cliente cuando se llama a la función **NetAlertRaise** o a la función **NetAlertRaiseEx** . Si el servicio no se está ejecutando, se produce un error en las funciones con el **\_ archivo \_ no \_ encontrado**. El servicio de alerta en el cliente llama a la función [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) para enviar información a los destinatarios.

Las aplicaciones, los servicios de red y los componentes de red interna usan las funciones de alerta de administración de red para generar una alerta, notificando a varias aplicaciones o usuarios cuando se produce un tipo de evento determinado. Las funciones de categoría de alerta, los tipos de datos, las estructuras y las constantes se definen en LMCONS. H, LMERR. H y LMALERT. Archivos de encabezado H. Para obtener acceso a estas definiciones, defina las constantes INCL \_ . NETERRORS y incl \_ NETALERT e incluya el archivo de encabezado LM. H.

LMALERT. El archivo H predefine las siguientes clases de alerta (tipos de eventos de red) para el envío de alertas:

-   Eventos de red que requieren asistencia administrativa
-   Adición de una entrada a un archivo de registro de errores
-   Recepción de un mensaje de difusión por parte de un usuario o una aplicación
-   Finalización de un trabajo de impresión
-   Uso de ciertas aplicaciones o recursos por parte de los usuarios

Puede definir otras clases de alertas para las aplicaciones de red según sea necesario. Por ejemplo, si una aplicación de un servidor escribe rutinariamente grandes cantidades de datos en una unidad de disco, la aplicación corre el riesgo de llenar el disco. En este caso, es posible que desee agregar el evento "no hay espacio libre en disco" para desencadenar una alerta que notifique a la aplicación que se ponga en pausa o termine el proceso que está rellenando el disco. El nombre de un evento para una alerta puede ser cualquier cadena de texto.

Cuando se genera una alerta con una llamada a la función [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) , los datos del mensaje deben constar de una estructura de encabezado de [**\_ alerta STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) , seguida de datos de longitud fija adicionales que son específicos de la alerta en una [**\_ otra \_ información de administración**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info), de [**ERRLOG \_ otra \_**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info)información, de [**impresión de \_ otra \_ información**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)o de [**\_ otro \_ usuario**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) . Los datos adicionales de longitud variable pueden seguir la estructura específica de la alerta. (Las llamadas a la función [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) no requieren una estructura de **\_ alerta STD** ). La aplicación que realiza la llamada debe asignar la memoria para todas las estructuras y datos de longitud variable, y liberar la memoria después de que se devuelva la llamada.

Las siguientes macros están disponibles para su uso con búferes de datos de alerta.



| Macro                                          | Descripción                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**información de alerta \_ adicional \_**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Devuelve un puntero a los datos de longitud fija que siguen la estructura de **\_ alerta STD** en un mensaje de alerta. |
| [**\_datos de var de alerta \_**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Devuelve un puntero a los datos de longitud variable que siguen a los datos específicos de la alerta en un mensaje de alerta.   |



 

En lugar de usar las funciones de alerta de administración de red, es posible que pueda usar el SDK de Instrumental de administración de Windows (WMI) para la notificación de eventos. Para obtener más información acerca de las plataformas que admiten el modelo de eventos de WMI, vea [WMI Infrastructure](/windows/desktop/WmiSdk/wmi-infrastructure) and [Monitoring Events](/windows/desktop/WmiSdk/monitoring-events) en la documentación de WMI.

 

 