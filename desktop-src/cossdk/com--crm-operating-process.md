---
description: Proceso operativo de COM+ CRM
ms.assetid: be50912e-b9fd-4ef7-b81a-e37617a96955
title: Proceso operativo de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d294d60429faeaad7a4d58808760ecd327bcaff252f2b71070c6605f5327ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308134"
---
# <a name="com-crm-operating-process"></a>Proceso operativo de COM+ CRM

En funcionamiento normal, un componente de aplicación que se ejecuta en un proceso de aplicación de servidor usaría un CRM de COM+ mediante la creación de un trabajo de CRM. El trabajo de CRM implementa una interfaz COM específica de la tarea que está diseñada para realizar. El componente de aplicación debe ejecutarse en una transacción para que el trabajo de CRM herede la transacción del componente de aplicación. Los trabajadores de CRM siempre requieren una transacción.

Para acceder a COM+ CRM, el trabajo de CRM obtiene primero la interfaz [**ICrmLogControl,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) que permite al trabajador de CRM escribir registros en el registro duradero. El trabajo de CRM obtiene esta interfaz mediante la creación de un componente de vendedor de CRM.

A continuación, el trabajo de CRM debe decir al empleado de CRM el nombre del compensador de CRM que quiere usar. Para ello, llama al [**método ICrmLogControl::RegisterCompensator.**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-registercompensator) Después de llamar a este método, la infraestructura de CRM crea el compensador de CRM cuando se completa la transacción.

Después de que el trabajo de CRM haya registrado su compensador de CRM, puede escribir registros en el registro de CRM [**mediante ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). El trabajo de CRM debe *escribir por adelantado*; Es decir, debe escribir un registro en el registro que describa una acción antes de realizar realmente la acción, en caso de que se produzca un bloqueo inmediatamente después de completar la acción. Sin estas entradas de registro de escritura por adelantado, no hay ninguna manera de corregir la acción.

Además, la escritura previa significa que el compensador de CRM, que es el componente que recibe las entradas de registro durante la recuperación, debe tratar el caso en el que se escribieron las entradas de registro, pero la acción no se ha hecho. Las acciones del compensador de CRM deben *ser idempotentes;* es decir, deben ser capaces de realizarse más de una vez, pero deben conducir al mismo resultado. Por ejemplo, establecer un saldo de cuenta en el valor de 100 USD es una acción idempotente; Agregar 100 USD al saldo de la cuenta no es.

La [**interfaz ICrmLogControl proporciona**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol) los dos métodos siguientes para escribir registros:

-   [**WriteLogRecordVariants**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecordvariants) se usa para escribir una entrada de registro estructurada que se ha creado como una colección de variantes. Se usa principalmente al desarrollar CRMs en Microsoft Visual Basic.
-   [**WriteLogRecord**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-writelogrecord) se usa para escribir una entrada de registro no estructurada como BLOB de bytes. Se usa principalmente al desarrollar CRMs en Microsoft Visual C++. Dado que las estructuras de registros en C suelen estar configuradas por un conjunto de encabezados y campos que pueden estar dispersos en memoria, el método **WriteLogRecord** implementa una funcionalidad de recopilación que reduce la copia de datos.

> [!Note]  
> No debe usar tipos de puntero de usuario dentro de estructuras de datos en una entrada de registro. Los punteros ya no son válidos durante la fase de recuperación porque el compensador de CRM se ejecuta en un proceso diferente al del trabajo de CRM que escribió la entrada de registro. Incluir tipos de puntero en una entrada de registro podría provocar que una aplicación se bloqueara o se dañara durante la recuperación.

 

Ambos métodos de escritura escriben una entrada de registro en el disco, pero no garantizan la durabilidad del registro. Aunque permitir que las escrituras diferida se acumulen antes de forzar el disco puede mejorar el rendimiento, puede usar el método [**ICrmLogControl::ForceLog**](/windows/desktop/api/ComSvcs/nf-comsvcs-icrmlogcontrol-forcelog) en su lugar para garantizar que todas las escrituras realizadas por CRM sean duraderas en el disco, lo que es importante para la recuperación de errores.

Cuando el trabajo de CRM ha terminado con sus acciones y ha terminado de escribir y forzar registros en el registro, debe liberar [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol). Cuando se completa la transacción (normalmente debido al componente de aplicación que llama a [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**SetAbort),**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)la infraestructura de CRM crea el componente Compensator de CRM, que implementa la interfaz [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) o la interfaz [**ICrmCompensatorVariants.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) Estas interfaces se usan para pasar los registros no estructurados (Visual C++) o estructurados (Visual Basic) al compensador de CRM junto con las notificaciones de resultados de la transacción.

Crm Compensator se notifica primero de la fase de preparación de la finalización de la transacción y puede votar sí o no a la solicitud de preparación. Si el compensador de CRM vota no, no recibe ninguna notificación de anulación adicional. Si vota sí a la solicitud de preparación, recibe las notificaciones de confirmación o anulación. En el caso de una anulación de cliente, no se recibe ninguna notificación de preparación, solo notificaciones de anulación. Crm Compensator debe estar preparado para controlar todos estos casos y también debe controlar el caso en el que el trabajo de CRM no haya escrito correctamente ninguna entrada de registro. Crm Compensator no debe asumir que la misma instancia de CRM Compensator recibirá las notificaciones de fase 1 (preparación) y fase 2 (confirmación o anulación), ya que podrían interrumpirse mediante la recuperación.

Normalmente, un compensador de CRM usa la notificación de anulación para invertir la acción realizada por el trabajo de CRM. El trabajo de CRM podría dejar algún estado disponible en caso de que necesite invertir su acción. Ese estado puede estar totalmente contenido en las entradas del registro y, si no es así, crm Compensator debe limpiar ese estado si se confirma la transacción. Este es el motivo por el que CRM Compensator recibe la notificación de confirmación. Crm Compensator no se ejecuta en una transacción DTC.

Crm Compensator puede registrar nuevos registros si es necesario mediante [**ICrmLogControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol), que recibe cuando se crea. Tanto el trabajador de CRM como el compensador de CRM también pueden olvidar la última entrada de registro que escribieron, lo que podría ser necesario para evitar una recuperación innecesaria.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Inicio y recuperación de COM+ CRM](com--crm-startup-and-recovery.md)
</dt> </dl>

 

 



