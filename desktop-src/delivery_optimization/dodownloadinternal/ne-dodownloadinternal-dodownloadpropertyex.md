---
title: Enumeración DODownloadPropertyEx
description: Especifica el identificador de las propiedades extendidas para la operación de descarga.
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
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905316"
---
# <a name="dodownloadpropertyex-enumeration"></a>Enumeración DODownloadPropertyEx

> [!IMPORTANT]
> La enumeración **DODownloadPropertyEx** está en desuso. En su lugar, use la enumeración [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) con [IDODownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) y [IDODownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).

La enumeración **DODownloadPropertyEx** especifica el identificador de las propiedades extendidas para la operación de descarga. Esta enumeración la usa la interfaz **IDODownloadInternal** y se utiliza un valor **Variant** para obtener y establecer el valor de la propiedad.

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
| DODownloadPropertyEx_CorrelationVector | Opcional. Establece un vector de correlación específico para fines de telemetría. El tipo de variante es VT_BSTR. |
| DODownloadPropertyEx_DecryptionInfo | Reservado. No utilizar. |
| DODownloadPropertyEx_IntegrityCheckInfo | Opcional de solo escritura. Establece la ubicación del archivo hash de elemento (PHF), que se usa para realizar comprobaciones de integridad en tiempo de ejecución en el contenido descargado. El tipo de variante es VT_BSTR. |
| DODownloadPropertyEx_IntegrityCheckMandatory | Opcional. Establece una marca booleana que indica si el uso del archivo hash de la pieza (PHF) es obligatorio. Si VARIANT_TRUE, la descarga se anulará cuando se haya producido un error en la comprobación de integridad. El tipo de variante es VT_BOOL. |
| DODownloadPropertyEx_TotalSizeBytes | Reservado. No utilizar. |
| DODownloadPropertyEx_TempLocalFileUsage | Reservado. No utilizar. |

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | DODownloadInternal. h |
