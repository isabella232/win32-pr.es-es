---
description: Solución de problemas de COM+ CRM
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: Solución de problemas de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361600"
---
# <a name="troubleshooting-the-com-crm"></a>Solución de problemas de COM+ CRM

A continuación se presentan los problemas más comunes que se encuentran al desarrollar y usar EL CRM de COM+:

-   **Mensajes del registro de eventos.** Si la aplicación del servidor CRM encuentra un error interno grave, se producirá un error (finalizará el proceso de aplicación del servidor CRM) y escribirá un mensaje en el Windows de eventos. Consulte el registro de eventos si se encuentra algún problema.

-   **Excepciones del compensador de CRM.** La infraestructura de CRM crea el compensador de CRM y le pasa las notificaciones de resultados de la transacción y las entradas de registro escritas por el trabajador de CRM. Si el compensador de CRM devuelve un error o produce una excepción, la infraestructura de CRM lo detecta y provoca un error. Un mensaje en el registro de eventos indica que se recibió una excepción del compensador de CRM. Es posible forzar que estas excepciones se ignoren. (Vea [COM+ CRM Registry Configuración](com--crm-registry-settings.md)).) Las excepciones del compensador de CRM probablemente implican un problema en el componente de compensador de CRM específico y no en la propia infraestructura de CRM.

-   **Seguimiento de recuperación.** El seguimiento de recuperación puede ser muy útil para determinar los problemas durante la recuperación. Para obtener información sobre cómo habilitar el seguimiento de recuperación, [vea COM+ CRM Registry Configuración](com--crm-registry-settings.md).

-   **Intentando ejecutar con crm no habilitado.** No basta simplemente con colocar los componentes de CRM Worker y CRM Compensator en la aplicación de servidor COM+. La compatibilidad con CRM debe habilitarse específicamente para  la aplicación de servidor  COM+ específica mediante la opción Habilitar administradores de recursos de compensación en la pestaña Avanzadas de las páginas de propiedades de la aplicación COM+. (Consulte [Configuración de componentes de COM+ CRM](configuring-com--crm-components.md) para obtener más información). Si se intenta usar un CRM dentro de una aplicación de servidor que no tiene habilitado CRM, se devuelve un código de error al trabajo de CRM.

-   **Intentando ejecutar CRM en procesos de cliente.** Las CRM no se ejecutan en procesos de cliente; deben ejecutarse en un proceso de aplicación de servidor COM+. Los componentes de CRM se pueden colocar en un paquete de biblioteca para su uso en varias aplicaciones de servidor COM+, pero no están disponibles para su uso dentro de los procesos de cliente. Al intentar usar las interfaces de CRM dentro de un proceso de cliente, se devuelve un código de error al trabajo de CRM.

-   **Recuperación en curso.** La recuperación se inicia cuando se inicia una aplicación de servidor CRM. Sin embargo, la recuperación se produce en segundo plano durante el procesamiento normal de la aplicación de servidor CRM. El trabajo de CRM se puede crear antes de que se complete la recuperación. Las CRM no se pueden usar en un proceso de aplicación de servidor CRM hasta que la recuperación se haya completado correctamente. En este caso, el trabajador de CRM recibe un código de error de "recuperación en curso" al intentar registrar el compensador de CRM. El trabajo de CRM debe sondear o retrasarse de otro modo hasta que se haya completado la recuperación. El tiempo de recuperación es específico de un tipo determinado de CRM, y esto debe tenerse en cuenta al diseñar el CRM. Las recuperaciones de larga duración no son deseables.

-   **Seguridad en el archivo de registro de CRM.** Si se deniega el acceso al archivo de registro de CRM, consulte Consideraciones de seguridad de CRM de [COM+](com--crm-security-considerations.md) para obtener una descripción de cómo se establece la seguridad en el archivo de registro de CRM.

-   **Transacciones dudosas.** En raras ocasiones, una transacción DTC podría entrar en estado dudoso; es decir, el DTC no puede determinar el resultado de la transacción. En estos casos, durante la recuperación, CRM mantiene las entradas de registro de esa transacción en el archivo de registro de CRM. Cuando DTC ha resuelto la transacción dudosa, al realizar otra recuperación de CRM se completa la transacción.

-   **Creación y lanzamiento de CRM Compensator.** La primera vez que un trabajador de CRM registra un compensador de CRM, se crea mediante la infraestructura de CRM y se consulta para determinar cuál de las interfaces de compensador de CRM admite. A continuación, se libera inmediatamente. Los compensadores de CRM deben admitir la capacidad de crearse y liberarse sin haber tenido llamadas a métodos que intervendrán. Si crm Compensator no se puede crear correctamente, quizás debido a un registro COM incorrecto, o si no admite al menos una de las interfaces de compensador de CRM correctas, se devuelve un código de error al trabajo de CRM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



