---
title: DODownloadState (enumeración)
description: Especifica el identificador del estado de descarga actual, que forma parte de la **DO_DOWNLOAD_STATUS** actual.
keywords:
- Enumeración DODownloadState, DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 5df8f7b20c8cff3b905acec9852b26c9a5ee360645fddb1bec22990a8bb9daba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047143"
---
# <a name="dodownloadstate-enumeration"></a>DODownloadState (enumeración)

La **enumeración DODownloadState** especifica el identificador del estado de descarga actual, que forma parte de la **DO_DOWNLOAD_STATUS** actual.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a>Constantes

| Requisito | Valor |
|-|-|
| DODownloadState_Created | El objeto de descarga se ha creado, pero aún no se ha iniciado. |
| DODownloadState_Transferring | La descarga está en curso. |
| DODownloadState_Transferred | La descarga se transfiere y se puede iniciar de nuevo mediante la descarga de otra parte del archivo. |
| DODownloadState_Finalized | La descarga se ha finalizado y no se puede iniciar de nuevo. |
| DODownloadState_Aborted | Se anuló la descarga. |
| DODownloadState_Paused | La descarga se ha pausado a petición o debido a un error transitorio. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DeliveryOptimizationDownloadTypes.h |
