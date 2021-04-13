---
description: Solución de problemas de COM+ CRM
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: Solución de problemas de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539051"
---
# <a name="troubleshooting-the-com-crm"></a>Solución de problemas de COM+ CRM

A continuación se muestran los problemas más comunes que se producen al desarrollar y usar el CRM de COM+:

-   **Mensajes del registro de eventos.** Si la aplicación de servidor CRM detecta un error interno grave, se mostrará FailFast (finalizará el proceso de aplicación de servidor CRM) y escribirá un mensaje en el registro de eventos de Windows. Si encuentra algún problema, consulte el registro de eventos.

-   **Excepciones del compensador de CRM.** La infraestructura de CRM crea el compensador de CRM y lo pasa a las notificaciones de resultados de la transacción y a las entradas de registro escritas por el trabajador de CRM. Si el compensador de CRM devuelve un error o inicia una excepción, la infraestructura de CRM lo detecta y genera FailFast. Un mensaje en el registro de eventos indica que se ha recibido una excepción del compensador de CRM. Es posible forzar la omisión de estas excepciones. (Consulte [configuración del registro de com+ CRM](com--crm-registry-settings.md)). Lo más probable es que las excepciones del compensador de CRM signifiquen un problema en el componente de compensador de CRM específico y no en la propia infraestructura de CRM.

-   **Seguimiento de recuperación.** El seguimiento de recuperación puede ser muy útil para determinar los problemas durante la recuperación. Para obtener información acerca de cómo habilitar el seguimiento de recuperación, consulte [configuración del registro de com+ CRM](com--crm-registry-settings.md).

-   **Intentando ejecutar con el CRM no habilitado.** No basta con colocar los componentes de trabajo de CRM y compensador de CRM en la aplicación de servidor COM+. La compatibilidad con CRMs debe estar habilitada específicamente para la aplicación de servidor COM+ específica mediante la opción **Habilitar administradores de compensación de recursos** en la pestaña **Opciones avanzadas** de las páginas de propiedades de la aplicación com+. (Consulte [configuración de componentes com+ CRM](configuring-com--crm-components.md) para obtener más información). Si se realiza un intento de usar un CRM dentro de una aplicación de servidor que no tiene el CRM habilitado, se devuelve un código de error al trabajo de CRM.

-   **Intentando ejecutar CRMs en procesos de cliente.** CRMs no se ejecutan en procesos de cliente; deben ejecutarse en un proceso de aplicación de servidor COM+. Los componentes de CRM se pueden colocar en un paquete de biblioteca para que puedan usarse en varias aplicaciones de servidor COM+, pero no están disponibles para su uso en procesos de cliente. Al intentar usar las interfaces de CRM dentro de un proceso de cliente, se devuelve un código de error al trabajo de CRM.

-   **Recuperación en curso.** La recuperación se inicia cuando se inicia una aplicación de servidor CRM. Sin embargo, la recuperación se produce en segundo plano durante el procesamiento normal de la aplicación de servidor CRM. El trabajo de CRM se puede crear antes de que se complete la recuperación. CRMs no se puede usar en un proceso de aplicación de servidor CRM hasta que la recuperación se haya completado correctamente. En este caso, el trabajo de CRM recibe un código de error "recuperación en curso" mientras intenta registrar el compensador de CRM. El trabajo de CRM debe sondear o retrasar de otro modo hasta que se haya completado la recuperación. El tiempo de recuperación es específico de un tipo determinado de CRM y debe tenerse en cuenta al diseñar el CRM. No se recomiendan las recuperaciones de larga duración.

-   **Seguridad en el archivo de registro de CRM.** Si se deniega el acceso al archivo de registro de CRM, consulte [consideraciones de seguridad de com+ CRM](com--crm-security-considerations.md) para obtener una descripción de cómo se establece la seguridad en el archivo de registro de CRM.

-   **Transacciones dudosas.** En raras ocasiones, una transacción DTC podría entrar en el estado dudoso; es decir, el DTC no puede determinar el resultado de la transacción. En estos casos, durante la recuperación, el CRM mantiene las entradas de registro para esa transacción en el archivo de registro de CRM. Cuando el DTC ha resuelto la transacción dudosa, al realizar otra recuperación de CRM se completa la transacción.

-   **Creación y liberación del compensador de CRM.** La primera vez que un compensador de CRM está registrado por un trabajador de CRM, se crea mediante la infraestructura de CRM y se consulta para determinar cuál de las interfaces compensadoras de CRM admite. Después se libera inmediatamente. Los compensadores de CRM necesitan admitir la capacidad de crear y liberar sin que haya ninguna llamada de método intermedia. Si el compensador CRM no se puede crear correctamente, quizás debido a un registro COM incorrecto, o si no admite al menos una de las interfaces compensadas de CRM correctas, se devuelve un código de error al trabajo CRM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



