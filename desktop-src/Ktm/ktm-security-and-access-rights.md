---
description: El Windows seguridad permite a los autores de llamadas de Kernel Transaction Manager (KTM) controlar el acceso a los objetos de transacción, administrador de transacciones, administrador de recursos y registro.
ms.assetid: c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae
title: Derechos de seguridad y acceso de KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4e42c9aaf8498ff16ebd1d32f539fef5b54b17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160030"
---
# <a name="ktm-security-and-access-rights"></a>Derechos de seguridad y acceso de KTM

El Windows seguridad permite a los autores de llamadas de Kernel Transaction Manager (KTM) controlar el acceso a los objetos de transacción, administrador de transacciones, administrador de recursos y registro. Para obtener más información, vea [Modelo de control de acceso](/windows/desktop/SecAuthZ/access-control-model). En el caso de las aplicaciones que no están interesadas en la seguridad, las transacciones se pueden crear con listas de control de acceso (ACL) permisivas que permiten a cualquier administrador de recursos dar de alta en una transacción.

## <a name="transactions"></a>Transacciones

Cuando un cliente usa la [**función OpenTransaction,**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad del objeto de transacción.

Los derechos de acceso válidos para los objetos de transacción incluyen la capacidad de consultar y establecer información, dar de alta y varias operaciones de transacción, así como derechos [de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). [**Máscaras de acceso a transacciones**](transaction-access-masks.md) enumera los derechos de acceso específicos para una transacción.

Dado que las transacciones tienen un estado duradero, es fundamental que los RM y los TMs que interactúan con la KTM cumplan sus obligaciones con respecto a la recuperación. Si no se cumplen estas obligaciones, se pueden producir pérdidas de recursos que no se limpian, incluso si se reinicia el sistema. Tenga en cuenta el efecto de una fuga persistente o código malintencionado que hizo que KTM consumiera recursos de kernel hasta que se produjera un error del sistema. Después del reinicio resultante, KTM leería su registro y volvería a crear todos los objetos persistentes, lo que podría provocar que se repita el mismo error del sistema. La limitación basada en la cuota evitará la escasez de recursos persistente de un rmn no fiable o con comportamientos mal comportamientos. Por último, se deben crear mecanismos administrativos que permitan la detección y corrección de dichas pérdidas persistentes.

## <a name="transaction-managers"></a>Administradores de transacciones

Cuando un cliente usa la [**función OpenTransactionManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de Resource Manager.

Los derechos de acceso válidos para los objetos del administrador de transacciones incluyen la capacidad de consultar y establecer información, crear RMs y recuperar y cambiar el nombre de las operaciones, así como los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). [**Máscaras de acceso del Administrador de transacciones**](transaction-manager-access-masks.md) enumera los derechos de acceso específicos para un administrador de transacciones.

Un administrador de recursos puede crear sus propios objetos de administrador de transacciones con ACL restrictivas para limitar qué administradores de recursos pueden participar en transacciones que usan el registro de ese administrador de transacciones.

## <a name="resource-managers"></a>Administradores de recursos

Cuando un cliente usa la [**función OpenResourceManager,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto del administrador de recursos.

Los derechos de acceso válidos para los objetos de Resource Manager incluyen la capacidad de consultar y establecer información, recuperar, dar de alta, operaciones de registro y operaciones de propagación y recuperación, así como derechos de [acceso estándar.](/windows/desktop/SecAuthZ/standard-access-rights) [**Resource Manager máscaras de acceso enumera**](resource-manager-access-masks.md) los derechos de acceso específicos para un administrador de recursos.

Un administrador de recursos puede crear sus propios objetos de Resource Manager con ACL restrictivas si desea evitar que el código malintencionado intercepte notificaciones o forza resultados transaccionales concretos.

## <a name="enlistments"></a>Alistamientos

Cuando un cliente usa la [**función OpenEnlistment,**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) el sistema comprueba los derechos de acceso solicitados con el descriptor de seguridad para el objeto de registro.

Los derechos de acceso válidos para los objetos de registro incluyen la capacidad de consultar y establecer información, las operaciones de recuperación, así como los [derechos de acceso estándar](/windows/desktop/SecAuthZ/standard-access-rights). [**EnListment Access Masks enumera**](enlistment-access-masks.md) los derechos de acceso específicos para una alta.

 

 
