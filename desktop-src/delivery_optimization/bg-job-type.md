---
title: Enumeración BG_JOB_TYPE (Deliveryoptimization. h)
description: La enumeración BG_JOB_TYPE define valores constantes que especifican el tipo de trabajo de transferencia, como la descarga.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Enumeración BG_JOB_TYPE
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490066"
---
# <a name="bg_job_type-enumeration"></a>Enumeración BG_JOB_TYPE

La enumeración **BG_JOB_TYPE** define valores constantes que especifican el tipo de trabajo de transferencia, como la descarga.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**
</dt> <dd>

Especifica que el trabajo descarga archivos en el cliente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob:: GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





