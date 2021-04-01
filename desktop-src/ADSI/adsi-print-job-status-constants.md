---
title: Constantes de estado del trabajo de impresión ADSI (Adssts. h)
description: Las constantes siguientes se usan con la propiedad IADsPrintJobOperations. status para indicar el estado de un trabajo de impresión.
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
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996838"
---
# <a name="adsi-print-job-status-constants"></a>Constantes de estado del trabajo de impresión ADSI

Las constantes siguientes se usan con la propiedad [**IADsPrintJobOperations. status**](iadsprintjoboperations-property-methods.md) para indicar el estado de un trabajo de impresión.

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**trabajo de ADS en \_ \_ pausa**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



El trabajo de impresión está en pausa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_error de trabajo de ADS \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Se produjo un error.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_eliminación de trabajos de ADS \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Se está eliminando el trabajo de impresión.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_cola de trabajos de ADS \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



El trabajo de impresión se está poniendo en cola.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_impresión de trabajos de ADS \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Se está imprimiendo el trabajo de impresión.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**trabajo de ADS \_ \_ sin conexión**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



La impresora no está conectada.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**trabajo de ADS \_ \_ PAPEROUT**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



La impresora se ha quedado sin papel.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**trabajo de ADS \_ \_ impreso**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Se ha impreso el trabajo de impresión.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**trabajo de ADS \_ \_ eliminado**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Se ha eliminado el trabajo de impresión.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Adssts. h</dt> </dl> |



 

 





