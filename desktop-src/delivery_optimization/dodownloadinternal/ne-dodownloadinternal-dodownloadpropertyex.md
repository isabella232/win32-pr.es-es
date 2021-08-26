---
title: ENUMERACIÓN DODownloadPropertyEx
description: Especifica el identificador de las propiedades extendidas para la operación de descarga de DO.
keywords:
- ENUMERACIÓN DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: f5ec26d845fd6df2bfe0e84fffed0979c39e1971244788c9dfe5ddd3a0c0beca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990385"
---
# <a name="dodownloadpropertyex-enumeration"></a>ENUMERACIÓN DODownloadPropertyEx

> [!IMPORTANT]
> La **enumeración DODownloadPropertyEx** está en desuso. En su lugar, use [la enumeración DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) [con IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) y [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).

La **enumeración DODownloadPropertyEx** especifica el identificador de las propiedades extendidas para la operación de descarga de DO. La interfaz **IDODownloadInternal** usa esta enumeración y se usa un valor **VARIANT** para obtener y establecer el valor de propiedad.

## <a name="syntax"></a>Syntax

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a>Constantes

| Requisito | Value |
|-|-|
| DODownloadPropertyEx_UpdateId | Reservado. No utilizar. |
| DODownloadPropertyEx_CorrelationVector | Opcional. Establece un vector de correlación específico para fines de telemetría. El tipo VARIANT VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Reservado. No utilizar. |
| DODownloadPropertyEx_IntegrityCheckInfo | Solo escritura opcional. Establece la ubicación del archivo hash por pieza (PHF), que usa do para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. El tipo VARIANT VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Opcional. Establece una marca booleana que indica si el uso del archivo hash de pieza (PHF) es obligatorio. Si VARIANT_TRUE, la descarga se anulará una vez que se haya fallado la comprobación de integridad. El tipo VARIANT VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Reservado. No utilizar. |
| DODownloadPropertyEx_TempLocalFileUsage | Reservado. No utilizar. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DODownloadInternal.h |
