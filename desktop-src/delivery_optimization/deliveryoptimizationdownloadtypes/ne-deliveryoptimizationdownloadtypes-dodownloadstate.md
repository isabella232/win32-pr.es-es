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
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566801"
---
# <a name="dodownloadstate-enumeration"></a>DODownloadState (enumeración)

La **enumeración DODownloadState** especifica el identificador del estado de descarga actual, que forma parte de la **DO_DOWNLOAD_STATUS** actual.

## <a name="syntax"></a>Sintaxis

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

| Requisito | Value |
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
