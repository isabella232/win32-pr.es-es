---
title: Constantes de estado del trabajo de impresión ADSI (Adssts.h)
description: Las siguientes constantes se usan con la propiedad IADsPrintJobOperations.Status para indicar el estado de un trabajo de impresión.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33e2a5ae18ec65ea74bb9e2eed5f09d90fb86e05693008b830da6f95511eac0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180609"
---
# <a name="adsi-print-job-status-constants"></a>Constantes de estado del trabajo de impresión ADSI

Las siguientes constantes se usan con la propiedad [**IADsPrintJobOperations.Status**](iadsprintjoboperations-property-methods.md) para indicar el estado de un trabajo de impresión.

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**TRABAJO \_ DE ADS EN \_ PAUSA**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



El trabajo de impresión está en pausa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**ERROR DE \_ TRABAJO DE \_ ADS**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Se produjo un error.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**ELIMINACIÓN \_ \_ DE TRABAJOS DE ADS**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Se está eliminando el trabajo de impresión.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**COLA \_ DE TRABAJOS DE ADS \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



El trabajo de impresión se está colando.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**IMPRESIÓN \_ DE TRABAJOS DE \_ ADS**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Se está imprimendo el trabajo de impresión.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**TRABAJO DE ADS \_ SIN \_ CONEXIÓN**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



La impresora no está conectada.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**ADS \_ JOB \_ PAPEROUT**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



La impresora se ha quedado sin papel.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**ADS \_ JOB \_ PRINTED**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Se ha impreso el trabajo de impresión.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**TRABAJOS \_ DE ADS \_ ELIMINADOS**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Se ha eliminado el trabajo de impresión.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Adssts.h</dt> </dl> |



 

 





