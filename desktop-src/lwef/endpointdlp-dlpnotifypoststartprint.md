---
description: Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.
title: Función DlpNotifyPostStartPrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostOpenDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 23caba53e754c54bfd717274b5f889ad224a2dc80fbe54fb97f70125c0c74f23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976585"
---
# <a name="dlpnotifypoststartprint-function"></a>Función DlpNotifyPostStartPrint

Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de impresión.

</dd> </dl>

<dl> <dt>

*PrintInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contiene información sobre la operación de impresión.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |