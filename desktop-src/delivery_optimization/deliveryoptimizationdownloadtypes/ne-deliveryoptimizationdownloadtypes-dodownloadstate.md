---
title: Enumeración DODownloadState
description: Especifica el identificador del estado de descarga actual, que forma parte de la estructura de **DO_DOWNLOAD_STATUS** .
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534930"
---
# <a name="dodownloadstate-enumeration"></a>Enumeración DODownloadState

La enumeración **DODownloadState** especifica el identificador del estado de descarga actual, que forma parte de la estructura de **DO_DOWNLOAD_STATUS** .

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
| DODownloadState_Created | Se ha creado el objeto de descarga, pero aún no se ha iniciado. |
| DODownloadState_Transferring | La descarga está en curso. |
| DODownloadState_Transferred | La descarga se transfiere y puede volver a empezar descargando otra parte del archivo. |
| DODownloadState_Finalized | La descarga se ha finalizado y no se puede volver a iniciar. |
| DODownloadState_Aborted | Se anuló la descarga. |
| DODownloadState_Paused | La descarga se ha pausado a petición o debido a un error transitorio. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DeliveryOptimizationDownloadTypes. h |
