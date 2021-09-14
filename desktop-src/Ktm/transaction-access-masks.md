---
description: KTM define las siguientes máscaras de acceso a transacciones que se usarán al abrir una transacción.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Máscaras de acceso a transacciones (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160022"
---
# <a name="transaction-access-masks"></a>Máscaras de acceso a transacciones

KTM define las siguientes máscaras de acceso a transacciones que se usarán al abrir una transacción.

<dl> <dt>

<span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**INFORMACIÓN DE \_ CONSULTA DE \_ TRANSACCIONES**
</dt> <dd> <dl> <dt>

0x000001
</dt> <dt>



El autor de la llamada puede consultar la información de la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**INFORMACIÓN DEL \_ CONJUNTO \_ DE TRANSACCIONES**
</dt> <dd> <dl> <dt>

0x000002
</dt> <dt>



El autor de la llamada puede establecer la información de la transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION \_ ENLIST**
</dt> <dd> <dl> <dt>

0x000004
</dt> <dt>



El autor de la llamada puede alistarse en esta transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**CONFIRMACIÓN DE \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x000008
</dt> <dt>



El autor de la llamada puede confirmar esta transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**REVERSIÓN \_ DE TRANSACCIONES**
</dt> <dd> <dl> <dt>

0x000010
</dt> <dt>



El autor de la llamada puede revertir esta transacción.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**PROPAGACIÓN \_ DE TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x000020
</dt> <dt>



El autor de la llamada puede propagar esta transacción a un administrador de recursos superior, como Coordinador de transacciones distribuidas (DTC).


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**LECTURA \_ GENÉRICA DE \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x120001
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ READ,** **TRANSACTION QUERY \_ \_ INFORMATION** y **SYNCHRONIZE.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**ESCRITURA \_ GENÉRICA DE \_ TRANSACCIÓN**
</dt> <dd> <dl> <dt>

0x12003E
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ WRITE**, **TRANSACTION SET \_ \_ INFORMATION**, **TRANSACTION \_ COMMIT**, **TRANSACTION \_ ENLIST,** **TRANSACTION \_ ROLLBACK,** **TRANSACTION \_ PROPAGATE** y **SYNCHRONIZE.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x120018
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ EXECUTE,** **TRANSACTION \_ COMMIT,** **TRANSACTION \_ ROLLBACK** y **SYNCHRONIZE.**


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0x12003F
</dt> <dt>



El autor de la llamada tiene el privilegio siguiente: **STANDARD \_ RIGHTS \_ REQUIRED,** **TRANSACTION GENERIC \_ \_ READ,** **TRANSACTION GENERIC \_ \_ WRITE** y **TRANSACTION GENERIC \_ \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**DERECHOS DE \_ RESOURCE \_ MANAGER DE \_ TRANSACCIONES**
</dt> <dd> <dl> <dt>

0x120037
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **TRANSACTION \_ GENERIC \_ READ**, **STANDARD RIGHTS \_ \_ WRITE**, **TRANSACTION SET \_ \_ INFORMATION**, **TRANSACTION \_ ROLLBACK**, **TRANSACTION \_ ENLIST,** **TRANSACTION \_ PROPAGATE** y **SYNCHRONIZE**.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Se recomienda que los administradores de recursos, al realizar la alta en una transacción, **especifiquen TRANSACTION \_ RESOURCE MANAGER \_ \_ RIGHTS** al abrir una transacción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




