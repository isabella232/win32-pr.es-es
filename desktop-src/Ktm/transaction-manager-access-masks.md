---
description: KTM define las siguientes máscaras de acceso de alta que se usarán al abrir un administrador de transacciones (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Máscaras de acceso del Administrador de transacciones (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160017"
---
# <a name="transaction-manager-access-masks"></a>Máscaras de acceso del Administrador de transacciones

KTM define las siguientes máscaras de acceso de alta que se usarán al abrir un administrador de transacciones (TM).

<dl> <dt>

<span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**INFORMACIÓN DE CONSULTA \_ DE \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



El autor de la llamada puede consultar información sobre este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER \_ SET \_ INFORMATION**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



El autor de la llamada puede establecer información sobre este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**RECUPERACIÓN DE \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



El autor de la llamada puede recuperar este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**CAMBIO DE NOMBRE DE TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



El autor de la llamada puede cambiar el nombre de una instancia de TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ CREATE \_ RM**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



El autor de la llamada puede crear un administrador de recursos asociado a este TM.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACCIÓN DE \_ ENLACE DE \_ TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

0x00020
</dt> <dt>



Este valor está reservado.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**LECTURA GENÉRICA DE TRANSACTIONMANAGER \_ \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ READ** y **TRANSACTIONMANAGER QUERY \_ \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**ESCRITURA GENÉRICA DE TRANSACTIONMANAGER \_ \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



El autor de la llamada tiene los privilegios siguientes: **STANDARD \_ RIGHTS \_ WRITE**, **TRANSACTIONMANAGER SET \_ \_ INFORMATION**, **TRANSACTIONMANAGER \_ RECOVER**, **TRANSACTIONMANAGER \_ RENAME** y **TRANSACTIONMANAGER CREATE \_ \_ RM**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x20000
</dt> <dt>



El autor de la llamada tiene el siguiente privilegio: **STANDARD \_ RIGHTS \_ EXECUTE**.


</dt> </dl> </dd> <dt>

<span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**ACCESO DE TRANSACTIONMANAGER \_ \_ ALL**
</dt> <dd> <dl> <dt>

0xF003F
</dt> <dt>



Este valor establece todos los bits válidos para un valor de acceso TM.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




