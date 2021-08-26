---
description: KTM define las siguientes máscaras de acceso de registro que se usarán al abrir las inscciones.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Enlistment Access Masks (WinNT.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f3d774c474c27896c16bba5c7552713f248519aa86ef56da0da5b704234b19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870115"
---
# <a name="enlistment-access-masks"></a>Enlistment Access Masks

KTM define las siguientes máscaras de acceso de registro que se usarán al abrir las inscciones.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**INFORMACIÓN DE CONSULTA \_ DE \_ ENLISTMENT**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



El autor de la llamada puede consultar KTM para obtener información sobre la alistación.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**INFORMACIÓN DEL CONJUNTO \_ DE \_ ALISTMENT**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



El autor de la llamada puede establecer información sobre la alta.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**RECUPERACIÓN DE LA \_ ALISTMENT**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



El autor de la llamada puede recuperar una alta.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**DERECHOS \_ SUBORDINADOS DE \_ ALISTMENT**
</dt> <dd> <dl> <dt>

0x00008
</dt> <dt>



El autor de la llamada puede completar las acciones que realiza un administrador de recursos en nombre de la transacción. A continuación se muestra una lista de acciones:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**DERECHOS SUPERIORES \_ DE \_ ALISTMENT**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



El autor de la llamada puede alistarse en la transacción como administrador de transacciones superior.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT \_ GENERIC \_ READ**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ READ** y **ENLISTMENT \_ QUERY \_ INFORMATION**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**REGISTRO DE ESCRITURA \_ \_ GENÉRICA**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ WRITE**, **ENLISTMENT \_ SET \_ INFORMATION** y **ENLISTMENT \_ RECOVER**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT \_ GENERIC \_ EXECUTE**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **STANDARD \_ RIGHTS \_ EXECUTE**, **ENLISTMENT \_ RECOVER** y **ENLISTMENT \_ SUBORDINATE \_ RIGHTS**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ALISTMENT \_ ALL \_ ACCESS**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Este valor establece todos los bits válidos para un valor de acceso de alta.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Header<br/>                   | <dl> <dt>WinNT.h</dt> </dl> |



 

 




