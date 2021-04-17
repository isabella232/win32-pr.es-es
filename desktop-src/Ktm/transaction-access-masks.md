---
description: KTM define las siguientes máscaras de acceso a las transacciones que se van a usar al abrir una transacción.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Máscaras de acceso a transacciones (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677695"
---
# <a name="transaction-access-masks"></a>Máscaras de acceso a transacciones

KTM define las siguientes máscaras de acceso a las transacciones que se van a usar al abrir una transacción.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_información de consulta de transacción \_**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



El autor de la llamada puede consultar la información de la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_información del conjunto de transacciones \_**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



El autor de la llamada puede establecer la información de la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**inscripción de transacciones \_**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



El autor de la llamada puede darse de alta en esta transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**confirmación de transacción \_**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



El autor de la llamada puede confirmar esta transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**reversión de transacciones \_**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



El autor de la llamada puede revertir esta transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**propagación de transacciones \_**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



El autor de la llamada puede propagar esta transacción a un administrador de recursos superior, como el Coordinador de transacciones distribuidas (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_lectura genérica de transacción \_**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **\_ \_ lectura de derechos estándar**, **información de \_ consulta \_ de transacción** y **sincronización**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_escritura genérica de transacción \_**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



El autor de la llamada tiene los privilegios siguientes: **\_ \_ escritura de derechos estándar**, **información de \_ conjunto \_ de transacciones**, **\_ confirmación de transacciones**, **\_ inscripción de transacciones**, **\_ reversión de transacciones**, **\_ propagación de transacciones** y **sincronización**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_ejecución genérica de transacción \_**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **\_ permisos estándar \_ Execute**, **\_ COMMIT TRANSACTION**, **\_ ROLLBACK TRANSACTION** y **SYNCHRONIZE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_acceso a todas las transacciones \_**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



El autor de la llamada tiene el siguiente privilegio: **\_ derechos estándar \_ necesarios**, **\_ \_ lectura genérica de transacción**, **\_ \_ escritura genérica de transacción** y **\_ \_ ejecución genérica de transacción**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_derechos del \_ Administrador de recursos de transacciones \_**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **operación de \_ \_ lectura genérica de transacción**, **\_ \_ escritura de derechos estándar**, **\_ \_ información de conjunto de transacciones**, **\_ reversión de transacciones**, **\_ inscripción de transacciones**, **\_ propagación de transacciones** y **sincronización**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Se recomienda que los administradores de recursos, cuando se da de alta en una transacción, especifiquen derechos de administrador de recursos de transacciones al abrir una transacción. **\_ \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




