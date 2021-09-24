---
title: DODownloadPropertyEx (enumeración)
description: Especifica el identificador de las propiedades extendidas para la Optimización de distribución de descarga.
keywords:
- Enumeración DODownloadPropertyEx, DODownloadPropertyEx
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
ms.openlocfilehash: c6a0f130aad68eab08a577b0153648cf17547189
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521007"
---
# <a name="dodownloadpropertyex-enumeration"></a>DODownloadPropertyEx (enumeración)

> [!IMPORTANT]
> La **enumeración DODownloadPropertyEx** está en desuso. En su lugar, use [la enumeración DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) [con IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) y [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).

La **enumeración DODownloadPropertyEx** especifica el identificador de las propiedades extendidas para la Optimización de distribución de descarga. La interfaz **IDODownloadInternal** usa esta enumeración y se usa un valor **VARIANT** para obtener y establecer el valor de propiedad.

## <a name="syntax"></a>Sintaxis

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
| DODownloadPropertyEx_CorrelationVector | Opcional. Establece un vector de correlación específico con fines de telemetría. El tipo VARIANT es VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Reservado. No utilizar. |
| DODownloadPropertyEx_IntegrityCheckInfo | Solo escritura opcional. Establece la ubicación del archivo hash de piezas (PHF), que usa Optimización de distribución para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. El tipo VARIANT es VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Opcional. Establece una marca booleana que indica si el uso del archivo hash de piezas (PHF) es obligatorio. Si VARIANT_TRUE, la descarga se anulará una vez que se haya fallado la comprobación de integridad. El tipo VARIANT es VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Reservado. No utilizar. |
| DODownloadPropertyEx_TempLocalFileUsage | Reservado. No utilizar. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | \[Windows 10, versión 1809 Solo aplicaciones Win32\] |
| **Servidor mínimo compatible** | Windows Servidor, versión 1809 \[ Solo aplicaciones Win32\] |
| **Header** | DODownloadInternal.h |
