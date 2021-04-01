---
description: KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de transacciones (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Máscaras de acceso del administrador de transacciones (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909185"
---
# <a name="transaction-manager-access-masks"></a>Máscaras de acceso del administrador de transacciones

KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de transacciones (TM).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_información de consulta de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



El autor de la llamada puede consultar información sobre este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_información del conjunto de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



El autor de la llamada puede establecer información sobre este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**recuperación de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



El autor de la llamada puede recuperar este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**\_cambiar nombre de TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



El autor de la llamada puede cambiar el nombre de una instancia de TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ crear \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



El autor de la llamada puede crear un administrador de recursos asociado a este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_transacción de enlace de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Este valor está reservado.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_lectura genérica de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **derechos estándar de \_ \_ lectura** e **\_ \_ información de consulta de TRANSACTIONMANAGER**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_escritura genérica de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



El autor de la llamada tiene los privilegios siguientes: **\_ \_ escritura de derechos estándar**, **información de \_ conjunto \_ de TransactionManager**, **\_ recuperación de TransactionManager**, **cambio de \_ nombre de TransactionManager** y **TransactionManager \_ Create \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_ejecución genérica de TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



El autor de la llamada tiene el siguiente privilegio: **permisos estándar de \_ \_ ejecución**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**destransactionmanager \_ todo el \_ acceso**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Este valor establece todos los bits válidos para un valor de acceso de TM.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




