---
description: Proporciona al sistema información sobre un documento cuando se sale de un destino de colocación.
title: Función DlpNotifyLeaveDropTarget (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyLeaveDropTarget
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: aac567843a88abb3355ab0b239c9ac0eca66bdfd240f2e6d82b3f8f91586c9a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976595"
---
# <a name="dlpnotifyleavedroptarget-function"></a>Función DlpNotifyLeaveDropTarget

Proporciona al sistema información sobre un documento cuando se sale de un destino de colocación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DocumentInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contiene información sobre el documento asociado a la operación de colocación.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ En\]
</dt> <dd>

Puntero a una [estructura](enpointdlp-dlp_postop_status.md) DLP_POSTOP_STATUS que contiene información de estado sobre la operación de salida de destino de colocación.

</dd> </dl>


## <a name="return-value"></a>Valor devuelto

Devuelve void.

## <a name="remarks"></a>Observaciones


## <a name="requirements"></a>Requisitos



| Requisito          |    Value                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1809 (10.0; Compilación 17763)           |
| Archivo DLL<br/>                      | EndpointDlp.dll |