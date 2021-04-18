---
title: 'IDODownload:: Start (método)'
description: Inicia o reanuda una descarga.
keywords:
- 'IDODownload:: Start (método)'
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "105721403"
---
# <a name="idodownloadstart-method"></a>IDODownload:: Start (método)

Inicia o reanuda una descarga, pasando los intervalos opcionales como puntero a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) estructura.

## <a name="syntax"></a>Sintaxis

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a>Parámetros

`ranges`

Opcional. Puntero a una estructura de [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) (para descargar solo los intervalos concretos del archivo). Pass `nullptr` para descargar todo el archivo.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve **S_OK**. De lo contrario, devuelve un [código de error](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Solo aplicaciones Win32 de Windows 10, versión 1809 \[\] |
| **Servidor mínimo compatible** | Windows Server, versión 1809 \[ Win32 Applications Only\] |
| **Header** | Do. h |
