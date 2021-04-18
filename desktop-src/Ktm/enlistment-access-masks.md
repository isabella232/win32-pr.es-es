---
description: KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir las inlistas.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Máscaras de acceso de inscripción (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688548"
---
# <a name="enlistment-access-masks"></a>Máscaras de acceso de inscripción

KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir las inlistas.

<dl> <dt>

<span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**información de la \_ consulta de inscripción \_**
</dt> <dd> <dl> <dt>

0x00001
</dt> <dt>



El autor de la llamada puede consultar el KTM para obtener información sobre la inscripción.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**información del conjunto de inscripción \_ \_**
</dt> <dd> <dl> <dt>

0x00002
</dt> <dt>



El autor de la llamada puede establecer información sobre la inscripción.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**recuperación de inscripción \_**
</dt> <dd> <dl> <dt>

0x00004
</dt> <dt>



El autor de la llamada puede recuperar una inscripción.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**\_derechos subordinados de \_ inscripción**
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

<span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_derechos superiores de inscripción \_**
</dt> <dd> <dl> <dt>

0x00010
</dt> <dt>



El autor de la llamada puede darse de alta en la transacción como un administrador de transacciones superior.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_lectura genérica de inscripción \_**
</dt> <dd> <dl> <dt>

0x20001
</dt> <dt>



El autor de la llamada tiene los privilegios siguientes: **\_ \_ información** de la consulta de inscripción y de **\_ \_ lectura de derechos estándar** .


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_escritura genérica de inscripción \_**
</dt> <dd> <dl> <dt>

0x2001E
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **\_ \_ escritura de derechos estándar**, **información de \_ conjunto \_ de inscripción** y **\_ recuperación de inscripción**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_ejecución genérica de inscripción \_**
</dt> <dd> <dl> <dt>

0x2001C
</dt> <dt>



El autor de la llamada tiene los siguientes privilegios: **derechos estándar de \_ \_ ejecución**, **\_ recuperación de alta** y **inscripción \_ subordinada \_**.


</dt> </dl> </dd> <dt>

<span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**DAR de alta \_ todo el \_ acceso**
</dt> <dd> <dl> <dt>

0xF001F
</dt> <dt>



Este valor establece todos los bits válidos para un valor de acceso de inscripción.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winnt. h</dt> </dl> |



 

 




