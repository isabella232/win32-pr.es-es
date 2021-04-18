---
description: El modelo de seguridad de Windows permite a los llamadores del administrador de transacciones de kernel (KTM) controlar el acceso a los objetos de transacción, administrador de transacciones, administrador de recursos y inscripción.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Derechos de acceso y seguridad de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688334"
---
# <a name="ktm-security-and-access-rights"></a>Derechos de acceso y seguridad de KTM

El modelo de seguridad de Windows permite a los llamadores del administrador de transacciones de kernel (KTM) controlar el acceso a los objetos de transacción, administrador de transacciones, administrador de recursos y inscripción. Para obtener más información, vea [modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model). En el caso de las aplicaciones que no están preocupadas por la seguridad, se pueden crear transacciones con listas de control de acceso (ACL) permisivas que permiten a cualquier administrador de recursos darse de alta en una transacción.

## <a name="transactions"></a>Transacciones

Cuando un cliente usa la función [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de transacción.

Los derechos de acceso válidos para los objetos de transacción incluyen la capacidad de consultar y establecer información, dar de alta y varias operaciones de transacción, así como [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). Las [**máscaras de acceso a transacciones**](transaction-access-masks.md) muestran los derechos de acceso específicos para una transacción.

Dado que las transacciones tienen un estado duradero, es fundamental que RMs y TMs que interactúen con el KTM cumplan sus obligaciones con respecto a la recuperación. Si no se cumplen estas obligaciones, pueden producirse pérdidas de recursos que no se limpian, incluso si se reinicia el sistema. Tenga en cuenta el efecto de una pérdida persistente o código malintencionado que hizo que el KTM consumiera recursos del kernel hasta que se produjera un error del sistema. después del reinicio resultante, el KTM podría leer su registro y volver a crear todos los objetos persistentes, lo que podría provocar que se repita el mismo error del sistema. La limitación basada en cuotas impedirá que el colapso de recursos persistentes no sea malintencionado o no tenga RM. Por último, deben crearse mecanismos administrativos que permitan la detección y corrección de dichas pérdidas persistentes.

## <a name="transaction-managers"></a>Administradores de transacciones

Cuando un cliente usa la función [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de Resource Manager.

Los derechos de acceso válidos para los objetos de administrador de transacciones incluyen la posibilidad de consultar y establecer información, de crear RMs y de recuperar y cambiar el nombre de las operaciones, así como de los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). [**Máscaras de acceso del administrador de transacciones**](transaction-manager-access-masks.md) muestra los derechos de acceso específicos para un administrador de transacciones.

Un administrador de recursos puede crear sus propios objetos de administrador de transacciones con ACL restrictivas para limitar los administradores de recursos que pueden participar en las transacciones que usan el registro de ese administrador de transacciones.

## <a name="resource-managers"></a>Administradores de recursos

Cuando un cliente usa la función [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de Resource Manager.

Los derechos de acceso válidos para los objetos de Resource Manager incluyen la posibilidad de consultar y establecer la información, la recuperación, la inscripción, las operaciones de registro y las operaciones de propagación y recuperación, así como los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). [**Administrador de recursos máscaras de acceso**](resource-manager-access-masks.md) muestra los derechos de acceso específicos para un administrador de recursos.

Un administrador de recursos puede crear sus propios objetos de Resource Manager con ACL restrictivas si desea evitar que el código malintencionado intercepte notificaciones o fuerce determinados resultados transaccionales.

## <a name="enlistments"></a>Inscripciones

Cuando un cliente usa la función [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) , el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de inscripción.

Los derechos de acceso válidos para los objetos de inscripción incluyen la capacidad de consultar y establecer la información, las operaciones de recuperación, así como los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). [**Máscaras de acceso de inscripción**](enlistment-access-masks.md) muestra los derechos de acceso específicos para una inscripción.

 

 
